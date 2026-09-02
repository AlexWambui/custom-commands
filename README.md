# Custom Commands

Adds custom commands to the terminal.

## Setup

### Add the commands folder to path in `.bashrc` file

```bash
# Add custom commands to PATH
export PATH="$PATH:/c/Aaqil/Development/custom_commands"
export PATH="$PATH:/c/Aaqil/Development/custom_commands/docs"
export PATH="$PATH:/c/Aaqil/Development/custom_commands/ssh"
export PATH="$PATH:/c/Aaqil/Development/custom_commands/navigation"
export PATH="$PATH:/c/Aaqil/Development/custom_commands/laravel"
```

### Make the Commands executable

```bash
chmod +x /c/Aaqil/Development/custom_commands/**/*
```

To make the scripts executable individually

```bash
find /c/Aaqil/Development/custom_commands -type f -name "*" -exec chmod +x {} \;
```

Note: Note: The find command is recommended because it recursively finds all files inside the custom_commands directory and its subdirectories.

### Using the Commands

Once the directory containing your custom commands has been added to your PATH, the commands can be run directly from Git Bash.

For example:

```bash
ssh-start-aaqil
```

Commands that modify the current shell.

To run commands that require ssh, like the ones for git start with source:

Use source whenever the script needs to change the current shell's environment, such as setting environment variables, changing directories, defining functions, aliases, or starting an SSH agent.

```bash
source ssh-start-aaqil
```
