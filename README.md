# ☕ gemini-cli-extension [WIP]

Brew up some amazing Product Requirements Documents (PRDs) with these custom commands for Gemini CLI.

## ♨️ Prerequisites

First, make sure you have the [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed and ready to go.

## 🛠️ Extension Installation

Get your coffee machine ready! ☕ From your command line, run:

```bash
gemini extensions install <TODO: Add the correct URL for this extension's repository>
```

## ⚙️ Extension management

Think of this as managing the tools in your coffee shop. Here's how you handle your extensions:

We offer a suite of extension management tools using `gemini extensions` commands.

Note that these commands are not supported from within the CLI, although you can list installed extensions using the `/extensions list` subcommand.

Note that all of these commands will only be reflected in active CLI sessions on restart.

### Installing an extension

You can install an extension using `gemini extensions install` with either a GitHub URL or a local path.

Note that we create a copy of the installed extension, so you will need to run `gemini extensions update` to pull in changes from both locally-defined extensions and those on GitHub.

**NOTE**: If you are installing an extension from GitHub, you’ll need to have `git` installed on your machine. See [git installation instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for help.

### Uninstalling an extension

To uninstall, run `gemini extensions uninstall extension-name`, so, in the case of the install example:

```
gemini extensions uninstall gemini-cli-security
```

### Disabling an extension

Extensions are, by default, enabled across all workspaces. You can disable an extension entirely or for specific workspace.

For example, `gemini extensions disable extension-name` will disable the extension at the user level, so it will be disabled everywhere. `gemini extensions disable extension-name --scope=workspace` will only disable the extension in the current workspace.

### Enabling an extension

You can enable extensions using `gemini extensions enable extension-name`. You can also enable an extension for a specific workspace using `gemini extensions enable extension-name --scope=workspace` from within that workspace.

This is useful if you have an extension disabled at the top-level and only enabled in specific places.

### Updating an extension

For extensions installed from a local path or a git repository, you can explicitly update to the latest version (as reflected in the `gemini-extension.json` version field) with `gemini extensions update extension-name`.

You can update all extensions with:

```
gemini extensions update --all
```

## 📜 Slash Commands

Here's our menu of special coffee commands:

| Command | Sub Command | Description | Inspired by |
|---|---|---|---|
| /prd | review | Guides the LLM to review an existing Product Requirements Document. | Cymbal Coffee Standard PRD Blueprint |
| /prd | create | Guides the LLM to create a new Product Requirements Document from raw notes. | Cymbal Coffee Standard PRD Blueprint & PR/FAQ |
| /plan  |   |   | **Credits**: [@dandobrin](https://github.com/ddobrin), this work was copied from Dan's [production serverless repository](https://github.com/GoogleCloudPlatform/serverless-production-readiness-java-gcp/tree/main/genai/quotes-llm/.gemini/commands) |

## 🙏 Credits

A big coffee-cup tip to ☕ [@dandobrin](https://github.com/ddobrin), this work was copied from Dan's [production serverless repository](https://github.com/GoogleCloudPlatform/serverless-production-readiness-java-gcp/tree/main/genai/quotes-llm/.gemini/commands) and broken into separate repository for easy installation.

## 📚 See Also

For further reading while you sip your coffee ☕, **see** [Gemini CLI Extensions](https://github.com/google-gemini/gemini-cli/blob/main/docs/extensions/index.md) for more details.
