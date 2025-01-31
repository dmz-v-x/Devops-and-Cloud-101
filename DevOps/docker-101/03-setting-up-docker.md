# How to Install Docker on Different Environments

Docker is a powerful tool that allows developers to create, deploy, and run applications in containers. This guide covers step-by-step instructions to install Docker on various environments.

## Table of Contents

- [How to Install Docker on Different Environments](#how-to-install-docker-on-different-environments)
  - [Table of Contents](#table-of-contents)
  - [Installing Docker on Windows](#installing-docker-on-windows)
    - [Prerequisites:](#prerequisites)
    - [Steps:](#steps)
  - [Installing Docker on macOS](#installing-docker-on-macos)
    - [Prerequisites:](#prerequisites-1)
    - [Steps:](#steps-1)
  - [Installing Docker on Ubuntu](#installing-docker-on-ubuntu)
    - [Prerequisites:](#prerequisites-2)
    - [Steps:](#steps-2)
  - [Installing Docker on CentOS](#installing-docker-on-centos)
    - [Prerequisites:](#prerequisites-3)
    - [Steps:](#steps-3)
  - [Installing Docker on Debian](#installing-docker-on-debian)
    - [Prerequisites:](#prerequisites-4)
    - [Steps:](#steps-4)
  - [Verifying Docker Installation](#verifying-docker-installation)

## Installing Docker on Windows

### Prerequisites:
- Windows 10 64-bit: Pro, Enterprise, or Education (2004+)
- Windows Subsystem for Linux (WSL 2) enabled
- Virtualization enabled in BIOS

### Steps:
1. Download [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop) from the official website.
2. Run the installer and follow the setup instructions.
3. Ensure WSL 2 is enabled by running:
   ```powershell
   wsl --list --verbose
   ```
4. Restart your system.
5. Open a terminal and run `docker version` to verify installation.

## Installing Docker on macOS

### Prerequisites:
- macOS 10.15 or later
- Apple Silicon or Intel-based Mac

### Steps:
1. Download [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop) from the official website.
2. Open the downloaded `.dmg` file and drag Docker to the Applications folder.
3. Launch Docker from Applications.
4. Follow the setup wizard and grant necessary permissions.
5. Run `docker --version` in the terminal to confirm installation.

## Installing Docker on Ubuntu

### Prerequisites:
- Ubuntu 20.04+ (Recommended)
- Sudo privileges

### Steps:
1. Update system packages:
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
2. Install required dependencies:
   ```sh
   sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
   ```
3. Add Docker’s official GPG key:
   ```sh
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   ```
4. Add the Docker repository:
   ```sh
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```
5. Install Docker:
   ```sh
   sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io
   ```
6. Start and enable Docker:
   ```sh
   sudo systemctl enable --now docker
   ```
7. Verify installation:
   ```sh
   docker --version
   ```

## Installing Docker on CentOS

### Prerequisites:
- CentOS 7 or 8
- Sudo privileges

### Steps:
1. Remove old versions (if any):
   ```sh
   sudo yum remove docker docker-common docker-selinux docker-engine
   ```
2. Install required packages:
   ```sh
   sudo yum install -y yum-utils device-mapper-persistent-data lvm2
   ```
3. Add Docker repository:
   ```sh
   sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
   ```
4. Install Docker:
   ```sh
   sudo yum install -y docker-ce docker-ce-cli containerd.io
   ```
5. Start and enable Docker:
   ```sh
   sudo systemctl enable --now docker
   ```
6. Verify installation:
   ```sh
   docker --version
   ```

## Installing Docker on Debian

### Prerequisites:
- Debian 10 or later
- Sudo privileges

### Steps:
1. Update existing packages:
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
2. Install dependencies:
   ```sh
   sudo apt install -y apt-transport-https ca-certificates curl gnupg lsb-release
   ```
3. Add Docker’s official GPG key:
   ```sh
   curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   ```
4. Set up the stable repository:
   ```sh
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```
5. Install Docker:
   ```sh
   sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io
   ```
6. Start and enable Docker:
   ```sh
   sudo systemctl enable --now docker
   ```
7. Verify installation:
   ```sh
   docker --version
   ```

## Verifying Docker Installation

After installing Docker, verify it is running correctly:

1. Check the Docker version:
   ```sh
   docker --version
   ```
2. Run a test container:
   ```sh
   sudo docker run hello-world
   ```
   If Docker is installed correctly, you should see a message confirming that the installation is successful.

---

Now that you have Docker installed, you can start using containers to simplify your development workflow!

---