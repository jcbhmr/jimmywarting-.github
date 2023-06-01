[GitHub Actions] are great! Just try to make them _standard-ish_ so that you
don't have to re-learn YAML each time you try to understand what the `ci.yml`
does in your repository. 🤣

For instance, I like to create a separate workflow for each "end goal" that I
want to do. For a theoretical Docker-based GitHub Action with source code, docs,
a Docker image, a dev wiki, that means something like this:

```sh
.
└── .github/
    └── workflows/
        ├── test.yml
        ├── test.yml
        ├── preview-docs.yml
        ├── deploy-docs.yml
        ├── publish-docker.yml
        ├── publish-wiki.yml
        └── update-tags.yml
```

Note that `test.yml` and `deploy-docs.yml` are pretty _generic_ names. You'd be
right! Normally, you only have one `test.yml` per project, so it makes sense to
just name it `test.yml` instead of `test-action.yml` or something. You're
already in the context of a project, so you don't need the extra description of
_what you're testing_. Also this fits with the "end goal" idea: in this case,
the end goal is "to test" the current project.

For a Node.js library project, it looks remarkably similar!

```sh
.
└── .github/
    └── workflows/
        ├── test.yml
        ├── test.yml
        ├── preview-docs.yml
        ├── deploy-docs.yml
        ├── publish-npm.yml
        └── publish-wiki.yml
```

Here's another example for a very simple Node.js website that wouldn't have any
tests, docs, or other support. It's just a bunch of HTML+CSS+JS that gets run
through Vite and deployed.

```sh
.
└── .github/
    └── workflows/
        ├── preview.yml
        └── deploy.yml
```

~~Now if you look in the workflow templates folder, you'll see that some of the
templates have suffixes like `+js` or `+typedoc` or similar. Those are suffixes
that are only added when I want to **create a second `test.yml`** and the names
would conflict. Thus, I need to add a suffix. **Make sure you remove the
`+sub` suffix when instantiating the template!**~~

~~For instance, there's a `test.yml` for npm-based projects, and then there's a
`test+action.yml` for GitHub Actions-based projects. The `test.yml` is the
"default" name since it's used so often, and the `+action.yml` one is there
since I use it often enough to want a template, but I can spare the few seconds
to delete the `+action` suffix when instantiating it. 😊~~

[GitHub Actions]: https://github.com/features/actions
