This repository comes equipped with a devcontainer configuration. That means
you're ready to get started in a few clicks with a pre-made development
environment using VS Code or GitHub Codespaces. Click one of the buttons below
to get started!

[![Open in Codespaces](https://img.shields.io/static/v1?style=for-the-badge&message=Open+in+Codespaces&color=181717&logo=GitHub&logoColor=FFFFFF&label=)][open in codespaces]
[![Open in VS Code](https://img.shields.io/static/v1?style=for-the-badge&message=Open+in+VS+Code&color=007ACC&logo=Visual+Studio+Code&logoColor=FFFFFF&label=)][open in vs code]

📚 Further reading: [Quickstart for GitHub Codespaces] \
📚 Further reading: [Developing inside a Container] (VS Code)

If you don't want to use the devcontainer, that's OK too! Just make sure that
your local environment has the dependencies specified in the
[`.devcontainer/devcontainer.json`] file.

After starting up your dev env and cloning the project, you can run
`tools/dev.sh` to spin up the backend watcher, frontend watcher, and fetch
external assets from AWS. You can find more commands in [`.vscode/tasks.json`].

<!-- prettier-ignore-start -->
[open in codespaces]: https://github.com/codespaces/new?hide_repo_select=true&ref=master&repo=1000
[open in vs code]: https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/user/repo
[quickstart for github codespaces]: https://docs.github.com/en/codespaces/getting-started/quickstart
[developing inside a container]: https://code.visualstudio.com/docs/devcontainers/containers
[`.devcontainer/devcontainer.json`]: https://github.com/user/repo/blob/main/.devcontainer/devcontainer.json
[`.vscode/tasks.json`]: https://github.com/user/repo/blob/main/.vscode/tasks.json
<!-- prettier-ignore-end -->
