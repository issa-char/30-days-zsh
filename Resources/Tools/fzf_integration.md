# FZF Integration with Oh-My-Zsh

[FZF](https://github.com/junegunn/fzf) is a powerful command-line fuzzy finder, and integrating it with Oh-My-Zsh enhances your Zsh experience by providing efficient and interactive search capabilities. This guide will walk you through the steps to integrate FZF with Oh-My-Zsh and showcase some useful configurations.

## Table of Contents

1. [Installation](#installation)
2. [Basic Usage](#basic-usage)
3. [Key Bindings](#key-bindings)
4. [FZF Options](#fzf-options)
5. [Custom Commands](#custom-commands)
6. [FZF with Git](#fzf-with-git)
7. [Additional Resources](#additional-resources)

## 1. Installation

Before integrating FZF with Oh-My-Zsh, ensure you have FZF installed. You can install it using a package manager, such as Homebrew or by following the instructions on the [FZF GitHub repository](https://github.com/junegunn/fzf).

Once FZF is installed, you can enable it in Oh-My-Zsh.

```zsh
# In your ~/.zshrc file
plugins=(fzf)
```

Then, restart your Zsh session or run `source ~/.zshrc` to apply the changes.

## 2. Basic Usage

FZF enhances your Zsh workflow by providing interactive, fuzzy search capabilities. Some basic examples include:

- **Ctrl-R:** Search and execute a command from your command history.
- **Ctrl-T:** Fuzzy search for files and directories.

Experiment with these basic commands to get a feel for FZF's capabilities.

## 3. Key Bindings

FZF comes with various key bindings that you can customize to suit your preferences. Some common key bindings include:

- **Alt-C:** Change to a subdirectory.
- **Ctrl-G:** Search and jump to a specific line in a file.

Customize key bindings in your `~/.zshrc` file:

```zsh
# Example: Change Alt-C binding to Ctrl-O
bindkey '^O' fzf-cd
```

## 4. FZF Options

FZF provides various options that you can configure to tailor its behavior. These options include the preview window, layout, and search filters. Refer to the [FZF GitHub repository](https://github.com/junegunn/fzf) for a comprehensive list of options.

Customize FZF options in your `~/.zshrc` file:

```zsh
# Example: Set FZF default command to use ripgrep
export FZF_DEFAULT_COMMAND='rg --files'
```

## 5. Custom Commands

Integrate FZF into custom commands to streamline your workflow. For example, create a custom alias for searching through your Git repositories:

```zsh
# In your ~/.zshrc file
alias gsf='git ls-files | fzf'
```

## 6. FZF with Git

FZF integrates seamlessly with Git, providing a more interactive and efficient Git experience. Some examples include:

- **Ctrl-G:** Fuzzy search for Git files.
- **Ctrl-B:** Fuzzy search for Git branches.

Enable FZF with Git in your `~/.zshrc` file:

```zsh
# In your ~/.zshrc file
export FZF_DEFAULT_COMMAND='(git ls-tree -r --name-only HEAD || find * -type f)'
```

## 7. Additional Resources

- [FZF GitHub Repository](https://github.com/junegunn/fzf)
- [FZF Wiki](https://github.com/junegunn/fzf/wiki)
- [Oh-My-Zsh Plugins Wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins#fzf)

Explore the various features and options provided by FZF to enhance your Zsh experience. Customizing FZF integration with Oh-My-Zsh can significantly boost your productivity and efficiency on the command line.
