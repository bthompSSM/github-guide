# Installing Git

## Installing on Windows

The most official build is available on the [Git website](https://git-scm.com/downloads/win).
Download the installer and run it.  The default options are more than sufficient for most users.

You can also install [Git via Chocolatey](https://chocolatey.org/packages/git).  If you have
Chocolatey installed, you can install Git with the following command:

```bash
choco install git
```

## Installing on macOS

If you are a macOS user, Git may already be installed.  You can check if Git is installed by running
the following command:

```bash
git --version
```

There are several ways to install Git on macOS.  The easiest way is to install the XCode Command Line
Tools.

```bash
xcode-select --install
```

You can also install Git using [Homebrew](https://brew.sh/).  If you have Homebrew installed, you
can install Git with the following command:

```bash
brew install git
```
