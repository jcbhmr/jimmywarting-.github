## `README.md`

<details>
  <summary>Code to copy</summary>

````md
# Greeter for Node.js

👋 Says hello to you in the console

<div align="center">

![](https://source.unsplash.com/random/600x400)

</div>

🧠 Knows who you are using `$USER` \
🎨 Uses ANSI colors \
🌎 Supports multiple languages \
🕒 Uses time-appropriate messages

## Installation

![npm](https://img.shields.io/static/v1?style=for-the-badge&message=npm&color=CB3837&logo=npm&logoColor=FFFFFF&label=)

You can install this package from npm, or run it without installing using npx.
This is a CLI-only package, so it doesn't export anything useful for a
JavaScript app to use.

```sh
npm install --global greet
```

```sh
npx greet
```

## Usage

![Windows Terminal](https://img.shields.io/static/v1?style=for-the-badge&message=Windows+Terminal&color=4D4D4D&logo=Windows+Terminal&logoColor=FFFFFF&label=)
![GNOME Terminal](https://img.shields.io/static/v1?style=for-the-badge&message=GNOME+Terminal&color=241F31&logo=GNOME+Terminal&logoColor=FFFFFF&label=)
![iTerm2](https://img.shields.io/static/v1?style=for-the-badge&message=iTerm2&color=000000&logo=iTerm2&logoColor=FFFFFF&label=)
![Hyper](https://img.shields.io/static/v1?style=for-the-badge&message=Hyper&color=000000&logo=Hyper&logoColor=FFFFFF&label=)

```sh
greet [options] [name]
```

### Examples

```sh
greet
greet Jacob
greet -t 12:00
greet --language fr
greet --no-color
```

### Option flags

#### `--language`, `--lang`, `-l`

Sets the language to use for the output. must be a valid BCP 47 language tag.
Examples: en, en-US, fr, en-GB, es. By default this is determined by `$LC_ALL`.

#### `--time`, `-t`

Emulate a particular time of the day. This affects what salutation is used.
Format is hH:MM:ss.ii or ISO-8601. Examples: 12:04, 18:45, 23:04:13,
15:25:56.284Z. Uses the current time by default.

#### `--color`, `--no-color`

Enable or disable color output.

### Environment variables

#### `$USER`

Used to determine the username to say hello to if no name argument is provided.

#### `$LC_ALL`

Used to determine what language should be used for output. Can be overridden by
the `--language` flag.

#### `$TERM`

Used to determine color format.

#### `$COLOR`, `$NO_COLOR`

`$COLOR` can be set to a false-y value to disable color, or to a truth-y value
to enable color. This is overruled by the presence of --color, --no-color, or
NO_COLOR. `$NO_COLOR` can be set to true to turn off color. Overrides the COLOR
var, but not the --color flag.

## Development

![Node.js](https://img.shields.io/static/v1?style=for-the-badge&message=Node.js&color=339933&logo=Node.js&logoColor=FFFFFF&label=)
![Docker](https://img.shields.io/static/v1?style=for-the-badge&message=Docker&color=2496ED&logo=Docker&logoColor=FFFFFF&label=)

This project uses Node.js and devcontainers to setup the development
environment. After you've launched a devcontainer, you can run `npm start` to
spin up the test watcher. Here's a summary of all the development commands:

- **`npm start`:** Starts the dev test watcher.
- **`npm test`:** Run the test suite once & lint the project.
- **`npm pack`:** Build the project. You can add `--dry-run` if you don't want a
  tarball.
````

</details>

## `wiki/Getting-started.md`

<details>
  <summary>Code to copy</summary>

````md
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
````

</details>

## `CONTRIBUTING.md`

<details>
  <summary>Code to copy</summary>

````md
**First off, thanks for taking the time to contribute! ❤️**

All types of contributions are encouraged and valued, no matter if it's a bug
report 🐛, a feature request 💡, or a Pull Request 🚀.

<!-- prettier-ignore -->
- **❓ I have a question:** Open an Issue
- **🐛 I found a bug:** Open an Issue
- **💡 I have an idea:** Open an Issue
- **💻 I want to write code:** [See below](#writing-code)

If you like the project, but just don't have time to contribute, that's OK too!
You can also star the project ⭐, rave about it online 💬, or add a link to us
🔗 in your project's readme.

⚠️ You must never report security 🔒 related issues, vulnerabilities or bugs
including sensitive information to the issue tracker, or elsewhere in public.
Instead sensitive bugs must be sent by email to jcbhmr@outlook.com.

👩‍⚖️ When contributing to this project, you must agree that you have authored 100%
of the content, that you have the necessary rights to the content and that the
content you contribute may be provided under the project license.

## Writing code

1. 🔀 Fork the repo
2. 💻 Open the repo in your editor
3. 👨‍💻 Add your changes to your workspace
4. ✨ Run the tests to make sure everything works
5. 🔖 Commit & push your changes
6. 🔁 Open a PR to get your changes merged
7. 🚀 Profit!
````

</details>
