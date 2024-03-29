﻿# Master Chef
 
 Master Chef is a recipe recommendation system. It provides a platform for users to explore, upload recipes and interact with each other.

## Frontend Setup

### Step 1.1: Web Browser

Programs have been tested on the following two browser:

- Locally, Google Chrome (various operating systems) - make sure is latest version.

If you don't already have it installed, recommend you download:
- [Google Chrome](https://www.google.com/intl/en_au/chrome/) (browser)

### Step 2.1: Install Node (includes NPM)

NodeJS can be installed on **Windows**, **MacOS**, and **Linux** by downloading it via the [NodeJS website](https://nodejs.org/en/download/). NPM is automatically installed alongside NodeJS.

However, because you're a computer scientist, we'd recommend you install it via command line to get comfortable with the process. The results are virtually the same:

#### **Windows** command-line install

Whilst you can install NodeJS onto Windows natively, we recommend installing it via the Windows Subsystem for Linux. Simply open up a WSL terminal and run the following commands:

    sudo apt update

    sudo apt install nodejs

If you haven't installed WSL or haven't heard of it before: WSL is a way to install a linux command prompt on windows, open that command prompt like a program, and interact with it the exact same way you would if you were on a linux machine. It's a very helpful tool for windows-based unix developers.

[This guide by Microsoft](https://docs.microsoft.com/en-us/windows/wsl/install) shows you how to install WSL, and we would recommend choosing Ubuntu 20.04 as the version of linux you install with. Once it's installed you can interact with it in a very similar way to what you would with a command line on vlab. 

#### **MacOS** command-line install

1. If you haven't already, install [homebrew](https://brew.sh/).

2. Open a terminal, and run

    brew install node

#### **Linux** command-line install

1. Open a terminal, and run

    sudo apt update

    sudo apt install nodejs

### Step 2.2: Install Yarn

In the world of Javascript development, an alternative to NPM called **yarn** is sometimes used.

To install **yarn** on Windows (WSL) or Linux, open a terminal and run:

    sudo npm i -g yarn

To install **yarn** on MacOS, open a terminal and run:

    brew install yarn

### Step 3.1 Start Run Frontend Server

1. Navigate to the `frontend` folder.

2. Install all of the dependencies necessary to run the ReactJS app and start the app, open a terminal and run:

        yarn install

3. After yarn install successfully in the `frontend` folder, run: 

        yarn start

If you failed to start the ReactJS app, in `frontend` folder and open a terminal to run following:

    yarn upgrade

    yarn add yarn

    yarn start

#### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000/](http://localhost:3000/) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.


## Backend Setup

### Step 1.1: Install Python

1. You can simply download Python through this link: [https://www.python.org/downloads/](https://www.python.org/downloads/).

2. Make sure you download the lastest version of Python and for the correct OS (Windows, MacOS, Linux).

### Step 2.1: Install MongoDB

**Windows**

1. Head over the link and download MongoDB MSI Installer Package (Make sure you select MSI): [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community)

2. Install MongoDB with the Installation Wizard

3. In the installation process, you can decide whether or not to download Mongo Compass for observing your own data.

**MacOS**

1. You can download mongodb using brew on MacOS. Open your terminal and run:

    brew install mongodb-community

2. Create a database folder for your computer

    sudo mkdir -p /System/Volumes/Data/data/db

After you pressed enter, input your computer password

3. Give permission to use the database folder. Run:

    sudo chown -R `id -un` /System/Volumes/Data/data/db

4. Start your MongoDB server by adding your database path. Run: 

    sudo mongod --dbpath /System/Volumes/Data/data/db

5. Create alias for the previous command to start MongoDB easier. Terminate MongoDB and run:

    alias mongd='sudo mongod --dbpath /System/Volumes/Data/data/db'

6. Start MongoDB again by simply run:

    mongod

The following video shows the steps as above of installing MongoDB on MacOS: [https://www.youtube.com/watch?v=4crXgQZG4W8&t=380s](https://www.youtube.com/watch?v=4crXgQZG4W8&t=380s)

**Linux**

1. Open terminal, download MongoDB by running:

    sudo apt install mongodb

### Step 3.1: Start running backend server

1. Navigate to the `backend` folder.

2. Install all the dependencies of python modules via pip to be able to run the backend server, open terminal in the current directory and run:

**MacOS** and **Linux**

    pip3 install -r requirements.txt

**Windows** 

    pip install -r requirements.txt

3. Run the backend server via terminal:

**MacOS** and **Linux**

    python3 server.py

**Windows** 

    python server.py
