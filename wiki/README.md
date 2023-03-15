This is a document that describes my own person stylistic preferences. Think of
it as a personal styleguide.

## Markdown

### Link style

When writing prose, I like to use the `[term]` external link definition pattern.
This approach offers the advantages of:

1. Not needing to define a link's href right away.
2. Not needing to think of a short ID like `[term][term-id]` since you are using
   `[term]` as its own ID.

But, it does offer one sole disadvantage (also shared with `[term][term-id]`):
Resolving `[term]` to an href takes longer than `[term](href)`

This particular style fits with the way I write Markdown. I write in prose for a
short sprint, and then come back with GitHub Copilot at the bottom of the file
to generate the `[term]: https://` prefixes that I need. Then, I just add in the
URLs and 💥 POW! I'm done!

This also lessens the `problem][with-long-tokens]` because that 👈 is
interpreted as one single "word" and will wrap as such:

```md
I hope that you have enjoyed this! Our [HTML
Specification-v2.0][whatwg-html-v2.0] is not yet ready for the prime time, so
try to be patient with us as we make sure that it meets all the necessary
```

🗣️ If you're interested in more debate about favorite link styles, check out
[spenserblack/spenserblack#42]

<!-- prettier-ignore-start -->
[spenserblack/spenserblack#42]: https://github.com/spenserblack/spenserblack/discussions/42
<!-- prettier-ignore-end -->
