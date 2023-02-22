---
title: Macros
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Macros

Rune has (experimental) support for macros. These are functions which expand
into code, and can be used by library writers to "extend the compiler".

For now, the following type of macros are support:
* Function-like macros expanding to items (functions, type declarations, ..).
* Function-like macros expanding to expression (statements, blocks, async blocks, ..).

Macros can currently only be defined natively. This is to get around the rather
tricky issue that the code of a macro has to be runnable during compilation.
Native modules have an edge here, because they have to be defined at a time when
they are definitely available to the compiler.

>>>>> Don't worry though, we will be playing around with `macro fn` as well, but at
>>>>> a later stage 😉 (See [issue #27]).

Native modules also means we can re-use all the existing compiler infrastructure
for Rune as a library for macro authors. Which is really nice!

[issue #27]: https://github.com/rune-rs/rune/issues/27

## Writing a native macro

The following is the definition of the `stringy_math!` macro. Which is a macro
that can be invoked on expressions.

This relies heavily on a Rune-specific [`quote!` macro]. Which is inspired by its
[famed counterpart in the Rust world]. A major difference with Rune `quote!` is
that we need to pass in the `MacroContext` when invoking it. This is a detail
which will be covered in one of the advanced sections.

```rust,noplaypen
use rune::ast;
use rune::ast::{Spanned, SpannedError};
use rune::macros::{quote, MacroContext, TokenStream};
use rune::parse::Parser;

/// Implementation for the `stringy_math!` macro.
pub(crate) fn stringy_math(
    ctx: &mut MacroContext<'_>,
    stream: &TokenStream,
) -> rune::Result<TokenStream> {
    let mut parser = Parser::from_token_stream(stream, ctx.stream_span());

    let mut output = quote!(0);

    while !parser.is_eof()? {
        let op = parser.parse::<ast::Ident>()?;
        let arg = parser.parse::<ast::Expr>()?;

        output = match ctx.resolve(op)? {
            "add" => quote!((#output) + #arg),
            "sub" => quote!((#output) - #arg),
            "div" => quote!((#output) / #arg),
            "mul" => quote!((#output) * #arg),
            _ => return Err(SpannedError::msg(op.span(), "unsupported operation").into()),
        }
    }

    parser.eof()?;
    Ok(output.into_token_stream(ctx))
}
```

A macro is added to a [`Module`] using the [`Module::macro_`] function.

```rust,noplaypen
pub fn module() -> Result<rune::Module, rune::ContextError> {
    let mut module = rune::Module::new(&["std", "experiments"]);
    module.macro_(&["stringy_math"], stringy_math_macro::stringy_math)?;
    Ok(module)
}
```

With this module installed, we can now take `stringy_math!` for a spin.

```rust
use ::std::experiments::stringy_math;

pub fn main() {
    let output = stringy_math!(add 10 sub 2 div 3 mul 100);
    println!("{}", output);
}
```

```bash
$> cargo run --bin rune -- run scripts/book/macros/stringy_math.rn -O macros=true --experimental
200
== () (2.9737ms)
```

To access the `std::experimental`, you have to specify the `--experimental`
option to the Rune CLI.

[`quote!` macro]: https://docs.rs/rune/0/rune/macro.quote.html
[famed counterpart in the Rust world]: https://docs.rs/quote/1/quote/
[`Module`]: https://docs.rs/rune/0/rune/module/struct.Module.html
[`Module::macro_`]: https://docs.rs/rune/0/rune/module/struct.Module.html#method.macro_
