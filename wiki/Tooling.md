## Formatters

I like to use standard formatters. This helps me keep this styleguide as short
as possible and avoid a lot of the minutia. Here's a list of some of the
formatters that I use and where I like to use them:

- **[Prettier]:** Used for everything web-related. JSON, JS, TS, HTML, CSS, and
  even Markdown. The only setting I twiddle with is `proseWrap: "always"` for
  Mardown.
- **[Clang-Format]:** I use this for anything C++ & C related. I don't override
  any of the defaults, which means I tend to get LLVM-styled C++ code.
  LLVM-styled code also happens to be the most popular on GitHub.
- **[cmake-format]:** For CMake code. No settings that I configure.
- **[shfmt]:** Makes Bash code prettier. Also doesn't have any settings I
  change.

As you may have noticed, I've learned to like the defaults of the tools I use.
It often means greater compatability and popularity.

<!-- prettier-ignore-start -->
[prettier]: https://prettier.io/
[clang-format]: https://clang.llvm.org/docs/ClangFormat.html
[cmake-format]: https://github.com/cheshirekow/cmake_format#readme
[shfmt]: https://github.com/mvdan/sh#shfmt
<!-- prettier-ignore-end -->
