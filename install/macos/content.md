# macOS: Installing

To develop web apps you need some tools on you laptop. This guide helps you with installing al these tools.


## Step 1: Command Line Tools

Open the Terminal app (press `⌘Space`, type terminal and press enter).

Run

    xcode-select --install

and click "Install".

## Step 2: Brew

Installing programs can be done via a package manage. macOS does not come with one out of the box, installing one is very easy!

Open the terminal app (press `⌘Space` and type terminal and press enter).

Run

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

to install [brew](https://brew.sh/)

## Step 3: Python and Sass

Open the Terminal app (press `⌘Space` and type terminal and press enter).

Run

    brew install python sass/sass/sass

to install [Python 3.7](https://python.org) and [Sass](https://sass-lang.com/).

## Step 4: A Text-editor

Those of you who have taken CS50 are used to working from within the IDE. In this course, we remove those training wheels. This means you have to download and install a text editor on your own computer. Free code editors are [Visual Studio Code](https://code.visualstudio.com/), [Atom](https://atom.io/) or [Sublime Text](https://www.sublimetext.com/). We would recommend Visual Studio Code, but you are free to choose another editor if you like.

Once again, these can be installed very easy using the terminal:

    brew cask install visual-studio-code

or 

    brew cask install atom 

or 
    
    brew cask install sublime-text

## Troubleshooting
Ran into trouble? Contact the staff! It’s important to get started quickly. You only have to do the above once, so get help now and you’ll be set for the remainder of the course!
