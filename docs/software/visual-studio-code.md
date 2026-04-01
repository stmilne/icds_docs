# Visual Studio Code

Visual Studio Code (VS Code) is a popular code editor that can be used to edit files and run code on Roar Collab. While you can use the [VS Code Server via the Portal](../running-jobs/portal.md), many users prefer to run VS Code on their local machine and connect to Roar Collab using the "Remote - SSH" extension.

## Prerequisites

Before you begin, ensure you have:

1.  **Roar Collab Account**: An active account on Roar Collab.
2.  **Visual Studio Code**: Installed on your local machine ([Download here](https://code.visualstudio.com/)).
3.  **SSH Client**: An SSH client installed (Terminal on macOS/Linux, OpenSSH Client on Windows).

## Installation

1.  Open Visual Studio Code on your local machine.
2.  Go to the **Extensions** view by clicking on the square icon in the sidebar or pressing `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (macOS).
3.  Search for "Remote - SSH".
4.  Install the extension **Remote - SSH** by Microsoft.

## Configuration

To connect to Roar Collab easily, it is best to configure your SSH config file.

1.  In VS Code, press `F1` or `Ctrl+Shift+P` (Windows/Linux) / `Cmd+Shift+P` (macOS) to open the Command Palette.
2.  Type and select **Remote-SSH: Open Configuration File...**.
3.  Select your user config file (usually `~/.ssh/config` or `C:\Users\YourUser\.ssh\config`).
4.  Add the following host entry:

```ssh
Host roar
    HostName submit.hpc.psu.edu
    User <your-userid>
```

Replace `<your-userid>` with your actual Penn State Access ID (e.g., `xyz123`).

## Connecting

1.  Open the Command Palette (`F1` or `Ctrl+Shift+P` / `Cmd+Shift+P`).
2.  Type and select **Remote-SSH: Connect to Host...**.
3.  Select **roar** from the list (or whatever name you gave the `Host` in your config file).
4.  A new VS Code window will open. You will be prompted to enter your password.
    *   **Note**: You will also need to approve the Duo push or enter your MFA code. The prompt may appear at the top of the VS Code window.
5.  Once connected, you will see "SSH: roar" in the green bottom-left corner of the window.

## Usage Tips

-   **File Editing**: You can now open folders and files on Roar Collab directly from VS Code. Go to **File > Open Folder...** to navigate the remote file system.
-   **Terminal**: Open the integrated terminal (`Ctrl+` `) to run commands on Roar Collab just like you would in a standard SSH session.
-   **Extensions**: You can install extensions specifically for the remote environment (e.g., Python, C/C++). These will run on Roar Collab while the UI remains on your local machine.

!!! warning "Heavy Computations"
    Do not run heavy computational tasks on the login nodes (where you land by default). For intensive work, submit [batch jobs](../running-jobs/batch-jobs.md) or use an [interactive job](../running-jobs/interactive-jobs.md).
