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
