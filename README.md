# Computer Setup

## Hardware (Computer) Requirements

You are required to supply your own laptop that meets the below requirements. Chromebooks are **not** suitable for this course, since you can’t directly control installed software. Many students use Macs. You are responsible for the upkeep and maintenance of your computer throughout the course. 

**At a minimum, your computer will need:**

* A 64-bit Operating System, like macOS, Ubuntu or Windows 10 Pro.
* To be fully up to date, with the latest version of its operating system and all security updates installed.
* At least 50GB of free space on the hard drive.
* At least 8GB of RAM. 16GB RAM strongly preferred.
* To be free of viruses, and in general working order.

## Windows Users

Before you begin check to make sure that you have the [most recent version of Windows 10](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update).


#### 1. Enable WSL Feature in Windows.

1. Right click on the start menu and click on Settings.
2. In the Search box, type `Turn Windows Features On Or Off` and click on the item that populates in the list.
3. A window will pop up with a list of folders with checkboxes next to them. Scroll down and check the box for `Windows Subsystem for Linux`.

This will install the needed files. Follow any directions that pop up and restart when asked. This page might not open after restart, so be sure to make note of the url or bookmark it.

#### 2. Install and setup the Ubuntu app from the Windows Store.

1. Click here to go to Microsoft store and install the [Ubuntu App](https://www.microsoft.com/en-us/store/p/ubuntu/9nblggh4msv6?activetab=pivot%3aoverviewtab)
1. Follow the on-screen prompts to install the app. 
1. When the app is ready, it will say Launch. Click Launch. This will start the Ubuntu installation.
1. It will ask you to enter a username. This will be the root / admin user for the Ubuntu FS. **A good user name is a single word (no spaces) and all lowercase**
1. It will then ask you to enter and confirm a password. Note that it will protect your password by not displaying it to the screen when you type, but it is registering your key strokes.
1. Finally, the prompt will change and you will be on a command line. Type `pwd` to see where you currently are in the FS, you should be at `/home/<your username>`. This is the root level of your Ubuntu user.


## All Users

### 1. App installation and terminal setup

* Open up Terminal (Mac)/Ubuntu App (Windows)
* Run this command to setup your system and install the default software utilities and applications
  * This process can take > 1 hour ...
    ```
    bash <(curl -s https://raw.githubusercontent.com/alchemycodelab/computer-setup-script/master/setup.sh)
    ```

### 2. Configure Git

Like artists, programmers sign their work. Let's configure Git to sign your commits with your name and email address.

Make sure you sign up for an account at Github <a href="https://github.com" target="_blank">here</a>.

**WARNING:** Before running the following commands, **replace `YOUR FULL NAME` and `YOUR EMAIL ADDRESS` with the name and email from <a href="https://github.com/settings/profile" target="_blank">your GitHub account</a>.**

```
git config --global user.name 'YOUR FULL NAME'
git config --global user.email 'YOUR EMAIL ADDRESS'
```

The terminal does not send success messages, in order to double check that you have successfully assigned your username and email:

```
git config --list
```

Your terminal should output the following lines (**but with your email address you used on GitHub and your full name!**):

```
user.email='YOUR EMAIL ADDRESS'
user.name='YOUR FULL NAME'
```

### 3. Install Visual Studio Code

VSCode is a code editor that comes with many helpful features to streamline your development process. It also comes with an integrated terminal, debugging capabilities, and a very helpful built-in source control UI.

VSCode is where you will doing the vast majority of your work. For Windows users, because VSCode relies on a GUI you will install it through Windows, not Ubuntu.

1. Vist [VSCode](https://code.visualstudio.com) to download VSCode.
1. Launch the installer and follow the onscreen prompts.
1. When you reach the section for `Additional tasks`, make sure every box is checked.
1. Click install and continue to follow and onscreen prompts.

#### Mac OSX Users Only

1. Launch (open) the VS Code app
2. Open the Command Palette by typing ⇧⌘P (SHIFT + COMMAND + P) and type 'shell command' to find, and then select, the "Shell Command: Install 'code' command in PATH" command.
    ![vs code](https://code.visualstudio.com/assets/docs/setup/mac/shell-command.png)
3. Quit VS Code

#### Windows Users Only

1. Launch (open) the VS Code app
2. Open the Command Palette by typing Ctrl+P
3. paste `ext install ms-vscode-remote.remote-wsl` into the input box
4. Exit VS Code

