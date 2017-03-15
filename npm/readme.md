# Install npm without Admin Rights
-------------------
Step 1: Get Node.exe

First you will need to download the Windows Binary. You can get it from Node.js download page or http://nodejs.org/dist/latest/. For x64, you will have to download from the appropriate folder. Move the executable to a local folder.

Step 2: Get NPM

NPM (Node Package Manager) is the package manager for Node.js and you will need this for your development. You can download NPM from https://github.com/npm/npm/releases and extract the zip file to a local folder.

Step 3: Configure the environment PATH variable.

You need to set up the PATH variable so that you can call node from anywhere in the system.

set PATH=%PATH%;D:\path-to-your-node;D:\path-to-your-npm

Mostly likely, the usual way of setting environment variables may not be accessible or not sufficient for you. instead you might want to hit Win + R (Open the Run dialog) and execute this:

rundll32 sysdm.cpl,EditEnvironmentVariables

This command will provide you with Environment Variables dialog box. You will be able to add/modify the PATH variable for the current user. Environment Variables dialog box

Step 4: Testing your Node.js installation

Quick way to test your Node.js installation is to get the version of Node.js that you are running by running the following command:

node --version
You should get something like this: Testing Nodejs installation

Extra: Setting up NPM to work behind a proxy

Apart from the hurdle of not having admin rights, one common issue is working behind the corporate proxy. Fire up your command line and type in the following:

npm config set proxy http://proxy:port
npm config set https-proxy https://proxy:port
If you need to specify the credentials, then use the following syntax:

npm config set proxy http://username:password@proxy:port
npm config set https-proxy https://username:password@proxy:port
Now you can get your hands dirty with Node.js. Happy programming! :)
