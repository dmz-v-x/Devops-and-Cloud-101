# Settting Up Git

## Table of Contents

- [Settting Up Git](#settting-up-git)
  - [Table of Contents](#table-of-contents)
  - [Setting Up Git](#setting-up-git)
  - [Installing Git on Different Platforms](#installing-git-on-different-platforms)
    - [Windows](#windows)
    - [macOS](#macos)
    - [Linux](#linux)
  - [Configuring Git for the First Time](#configuring-git-for-the-first-time)
    - [Setting Up Global Username and Email](#setting-up-global-username-and-email)
    - [Configuring Default Editor](#configuring-default-editor)
    - [Verifying Installation](#verifying-installation)
  - [Conclusion](#conclusion)

## Setting Up Git

## Installing Git on Different Platforms

### Windows

1. Download the latest version of Git from the official Git website: [https://git-scm.com/](https://git-scm.com/).
2. Run the installer and follow the instructions.
3. During installation, make sure to select the options to include Git Bash and Git GUI in the PATH.
4. Once installed, you can open Git Bash from the Start menu.

### macOS

1. Open the Terminal.
2. Install Git using Homebrew (if Homebrew is not installed, visit [https://brew.sh/](https://brew.sh/) for installation instructions):

   ```bash
   brew install git
   ```
3. Verify the installation by running:
   ```bash
   git --version
   ```

### Linux
For most Linux distributions, Git is available in the default package manager.

**Ubuntu/Debian-based distributions:**
```bash
sudo apt update
sudo apt install git
```

**CentOS/RHEL-based distributions:**
```bash
sudo yum install git
```
**Fedora:**
```bash
sudo dnf install git
```
After installation, verify the installation by running:
```bash
git --version
```

## Configuring Git for the First Time
After installing Git, it's essential to configure it before using it for version control.

### Setting Up Global Username and Email
Git uses your name and email to track who makes changes to a repository. Set these up globally for all repositories:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

To Check if your settings are correct, use:
```bash
git config --global --list
```
### Configuring Default Editor
Git allows you to specify which text editor it will use for commit messages and other tasks. The default is often Vim, but you can set it to any editor you prefer.

To set the default editor to Visual Studio Code:
```bash
git config --global core.editor "code --wait"
```
For other editors like Sublime Text or Atom, replace "code --wait" with the respective editor's command.

### Verifying Installation
To verify that Git is installed correctly and that your configuration is set, use the following command:

```bash
git --version
```

This will display the installed version of Git. You can also check your configuration settings:

```bash
git config --global --list
```

This will list all your global settings, including the username and email you set earlier.

## Conclusion
By following these steps, you've successfully installed and configured Git on your platform of choice. You can now begin using Git for version control and collaboration on software development projects!

