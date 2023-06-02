# Apps Tools

## Android

### gw

Replacement for [gw](https://github.com/gdubw/gng) that supports switching to a specific JVM version.

#### Installation

Install **gw** via Homebrew:

    brew tap gdubw/gng && brew install gng

Unlink it, so that we can replace its executable with our own:

    brew unlink gng

Create a link to our gw in a directory within the PATH, for example:

    cd ~/bin
    ln -s ~/git/apps-tools/android/gw

#### Usage

By default, the system JVM will be used.

To switch to a specific JVM for a specific project, create a file named `.jvmversion` in the project dir (same dir containing the `gradlew` executable), containing the version of the JVM you want, for example `17`:

    echo "17" > .jvmversion
