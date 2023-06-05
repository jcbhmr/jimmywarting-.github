Certain tools that GitHub offers seem to fit into certain "ideal usecases" in my
brain. 🧠 Here's a rundown of how I like to use the various GitHub tools:

- Use Discussions for discussing ideas, polls, or unrelated topics.
- Use Issues as a todo list. Discuss things related to solving the todo.
- Use PRs for documenting the _code & review_ of a thing. Often tied to Issues.

## Stacking PRs

There are occasions where I want to stack one thing on-to of another. For
example, if I'm migrating some `.js` files to `.ts` with types, I might do one
PR for the source code, and then one PR for the test code. But the test code
relies on the source code... So how do you do them "in sequence"?

You can use PRs that target _the branch of the prerequisite feature_! And guess
what? If that prerequisite feature gets merged and the branch gets removed, your
PR will _automatically_ target the `main` branch!

I got this idea from [LogRocket]'s blog post about it: [Using stacked pull
requests in GitHub] by [Simohamed Marhraoui].

<div align="center">

![](https://blog.logrocket.com/wp-content/uploads/2021/04/ts-setup-present.png)

![](https://blog.logrocket.com/wp-content/uploads/2021/04/migrate-components-ts.png)

![](https://blog.logrocket.com/wp-content/uploads/2021/04/base-automatically-changed.png)

</div>

💡 Make sure that your `test.yml` or other GitHub Actions run even when the PR
doesn't actually target `main`! Sure, _eventually_ `my-subsequent-feature` will
target `main`, but it's nice to run tests for those PRs even while they target
prerequisite branches.

```yml
# Prefer this!
on:
  pull_request:
    paths: ...
# ...instead of this:
on:
  pull_request:
    branches: main
    paths: ...
```

<!-- prettier-ignore-start -->
[LogRocket]: https://blog.logrocket.com/
[Using stacked pull requests in GitHub]: https://blog.logrocket.com/using-stacked-pull-requests-in-github/
[Simohamed Marhraoui]: https://blog.logrocket.com/author/simohamedmarhraoui/
<!-- prettier-ignore-end -->
