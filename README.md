# AI Shell

A CLI that converts natural language to shell commands.

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/844291/230181339-e7898e42-7bf0-4c14-9d2d-64de691522c6.gif)

Inspired by [Github Copilot X CLI](https://githubnext.com/projects/copilot-cli/), but open source for everyone.

## Setup

> The minimum supported version of Node.js is v14

1. Install _ai shell_:

   ```sh
   npm install -g @builder.io/ai-shell
   ```

2. Retrieve your API key from [OpenAI](https://platform.openai.com/account/api-keys)

   > Note: If you haven't already, you'll have to create an account and set up billing.

3. Set the key so ai-shell can use it:

   ```sh
   ai-shell config set OPENAI_KEY=<your token>
   ```

   This will create a `.ai-shell` file in your home directory.

## Usage

```bash
ai <prompt>
```

For example:

```bash
ai list all log files
```

Then you will get an output like this, where you can choose to run the suggested command, revise the command via a prompt, or cancel:

```bash
◇  Your script:
│
│  find . -name "*.log"
│
◇  Explanation:
│
│  1. Searches for all files with the extension ".log" in the current directory and any subdirectories.
│
◆  Run this script?
│  ● ✅ Yes (Lets go!)
│  ○ 📝 Revise
│  ○ ❌ Cancel
└
```

### Upgrading

Check the installed version with:

```bash
ai-shell --version
```

If it's not the [latest version](https://github.com/BuilderIO/ai-shell/tags), run:

```bash
npm update -g @builder.io/ai-shell
```

## Motivation

I am not a bash wizard, and am dying for access to the copilot CLI, and got impactient.

## TODO

- Support more shells and operating systems (e.g. windows)

## Credit

- Thanks to Github Copilot for their amazing tools and the idea for this
- Thanks to Hassan and his work on [aicommits](https://github.com/Nutlope/aicommits) which inspired the workflow and some parts of the code and flows
