I sort of have three audiences in mind when writing READMEs, wiki docs, or just
documentation in general:

- **Users:** Users just want to use the thing. They like examples, docs, etc.
  The "Installation" and "Usage" sections of a readme are for them. If there's a
  GitHub Pages site, then it's usually designed for users.

- **Tinkerers:** Tinkerers are people who want to see how the thing works, and
  probably want to build it themselves. But they don't _necessarily_ want to
  contribute changes back. They like outline documents, build instructions, code
  comments, etc. The "Development" section of the readme and a developer GitHub
  wiki are what I usually write with them in mind.

- **Contributors:** These are people who want to suggest ideas, write code, or
  help the project. They like conventions, walkthroughs, pointers to ask
  questions, styleguides, encouraging language, etc. This is who I usually write
  CONTRIBUTING.md with in mind. This group is a subset of the Tinkerers group,
  so they also use the developer wiki/"Development" section of the readme.

## What's the deal with the GitHub wiki?

The GitHub wiki is sort of like a halfway point between browsing in-source
Markdown files and viewing a full-fat website. This is great for the usecase
of providing documentation for developers to answer questions about more
complicated projects like:

- Why is the project structured this way?
- Why are we using this particular toolchain instead of _my favorite tool_?
- What's in-scope and what's out-of-scope?
- What's the governance model?
- How does this project get deployed to become a live website?
- Is there a reason we are using C++ instead of Rust?
- What code patterns are used throughout the codebase?
- What's the project styleguide?

⚠️ More user-focused documentation should probably go in the readme
(for everyone) or in a documentation website (if you have one). Things like
"how do I use this with _another app_?" are good examples of user-docs.
