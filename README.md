## PS1 Linux/macOS Terminal Customization

![Screenshot](https://previews.dropbox.com/p/thumb/AB2mqLijuPXlzBdC66T5CKzGbEspj4MmPuKZ2Qe6vVw3_qmaCRqMrWkuhNUCcodco66VFTdzm4TnGdp9v7Orf2wlAGztEzKfg_V1Xk5wOS1ysC-FiAxiHJ5Xxh5bdYE6PnHwAVi5_AItNelfZqr2W5w-f5Ol-ZPeXXKfZjtILhI82Qgli2twBwZGDXN5RYqy13UoOtlzcExZ3GrHFm88KZxK0QXOz1miDYIoXbSF9UEvjNlciD_CVX5oWaJKitxguoudQCehCE2PxqH9tZC66NfY4Wz9xy-yGPNtvqD1MWpr270kekMLpxEb0xbl9mk1YSWtehakghHb0rUEF6VsYi1JsWuHtwK4KAVUyP__I8k2f3MxKqP8-1IZvCC2UVbWjLE/p.png)


```bash
mrzakaria at Documents $
```


If you're tired of the default, boring terminal prompt on your Linux or macOS system, you can customize it to be more visually appealing and informative. Here's how you can customize the PS1 prompt in different distros and color schemes.

Bashrc File Locations
The location of the bashrc file varies depending on the Linux distribution you're using. Here's a basic list for the system bashrc:

/etc/bashrc (Redhat, Fedora, etc)
/etc/bash.bashrc (Debian, Ubuntu, Linux Mint, Backtrack, Kali, etc)
/etc/bash.bashrc.local (Suse, OpenSuse, etc)

# Debian Black Terminal
Here's a PS1 prompt that looks great on a black terminal in a Debian-based system:

```bash
PS1='${debian_chroot:+($debian_chroot)} \[$(tput bold)\]\[\033[38;5;197m\]\u\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] at \[$(tput bold)\]\[$(tput sgr0)\]\[\033[38;5;191m\]\W\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput sgr0)\]\$ '

```


# macOS Black Terminal
If you're using a black terminal on macOS, you can customize your PS1 prompt by following these steps:

1- Switch to the bash shell by running the command:

```bash
chsh -s /bin/bash
```

2- For regular users, edit your ~/.bash_profile file and paste the following code:

```bash
export BASH_SILENCE_DEPRECATION_WARNING=1
export PS1="\[$(tput bold)\]\[\033[38;5;7m\][\[$(tput sgr0)\]\[\033[38;5;198m\]\u\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput bold)\]\[$(tput sgr0)\]\[\033[38;5;7m\]at\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput bold)\]\[$(tput sgr0)\]\[\033[38;5;39m\]\W\[$(tput sgr0)\]\[\033[38;5;7m\]]\\$\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput sgr0)\]"

```

3- For root users, edit your ~/.bashrc file and paste the following code:

```bash
export BASH_SILENCE_DEPRECATION_WARNING=1
export PS1="\[$(tput bold)\]\[\033[38;5;7m\][\[$(tput sgr0)\]\[\033[38;5;198m\]\u\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput bold)\]\[$(tput sgr0)\]\[\033[38;5;7m\]at\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput bold)\]\[$(tput sgr0)\]\[\033[38;5;39m\]\W\[$(tput sgr0)\]\[\033[38;5;7m\]]\\$\[$(tput sgr0)\]\[$(tput sgr0)\]\[\033[38;5;15m\] \[$(tput sgr0)\]"

```

Note that the BASH_SILENCE_DEPRECATION_WARNING variable is used to suppress a warning message that macOS displays when you launch a new Terminal window.

Customizing your PS1 prompt on macOS can make your Terminal experience more enjoyable and efficient, especially if you spend a lot of time working in the command line.

