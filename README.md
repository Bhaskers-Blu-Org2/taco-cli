> Note: If you're looking for the `remotebuild` components, they have been moved to a new repo at https://github.com/Microsoft/remotebuild.

# What is TACO?

The Tools for Apache Cordova – "TACO" for short – provide a set of command line utilities that make hybrid app development easier, friendlier, and faster. 

For developers new to Cordova, TACO makes it crazy-easy to setup your dev environment so you can begin coding immediately. The install-reqs utility downloads, installs and configures all the build tools you need for each mobile platform. Once you’ve started coding, TACO makes life a little sweeter by providing a gentle nudge toward the most likely “next steps” and best practices. If you’re looking for a safety blanket, TACO has one of those, too. “TACO Kits” provide a set of validated open source components (e.g. platforms, build tools and plugins) so you don’t have to wade through the morass of download stats, star ratings and open issues to know which components are both stable and compatible with your app. Since building for iOS platform requires a Mac, TACO also provides a utility to connect to a [remotebuild](http://taco.tools/docs/remote-build.html) server, so that you can build iOS projects from your Windows machine.  

Faster setup. Friendlier command line. Validated quality at run-time. TACO is your friend.

## Quick Start

Using TACO, start building awesome Apache Cordova apps really quickly by following these steps:

**1. Install the tools:**

Make sure you have [Node.js](https://nodejs.org/en/download/) installed. **Note:** Latest version of NodeJS has [issues with iOS build](https://github.com/Microsoft/cordova-docs/blob/master/known-issues/known-issues-ios.md#building-for-ios-hangs-when-nodejs-v40-is-installed)  

Run the following command to install the latest version of TACO:

```
npm install -g taco-cli
```

**Note:** On OSX and Linux, you may need to prefix this command with `sudo` 

**2. Create a new app:**

```
taco create myAwesomeApp
```

**3. Navigate to the directory of your new project:**

```
cd myAwesomeApp
```

**4. Add the Android platform:**

```
taco platform add android
```

**5. (Optional) Check for any missing Android dependencies:**

```
taco install-reqs android
```

**6. Build for Android:**

```
taco build android
```

**7. Run the app on the Android emulator:**

```
taco emulate android
```

After a few moments, your app will be running inside the Android emulator in all its awesomeness. The steps to build for Windows and iOS are very similar, but this should help you get started.

Remember, when in doubt, just type:

```
taco help
```

## Community

* Have a question that's not a feature request or bug report? [Discuss on Stack Overflow](https://stackoverflow.com/questions/tagged/taco)
* Read our [Blog](http://taco.tools/blog/index.html)
* Have a feature request or find a bug? [Submit an issue](https://github.com/microsoft/taco/issues)
* [Contribute](https://github.com/Microsoft/TACO/blob/master/CONTRIBUTING.md) to TACO source
 

## Development

In order to build the TACO packages, ensure that you have [Git](http://git-scm.com/downloads) and [Node.js](http://nodejs.org/) installed.

Clone a copy of the repo:
```
git clone https://github.com/Microsoft/TACO.git
```

Change to TACO directory:
```
cd TACO
```
Install dev dependencies
```
npm install
```

#### Building TACO
TACO uses gulp based build system. To build TACO packages, simply run following command from root folder 
```
gulp
```
Above command will build and install TACO packages.
It will also create a globally-installed symbolic link (["npm link"](https://docs.npmjs.com/cli/link)) to TACO packages

#### Running TACO
Once TACO has been built and linked properly, you can use TACO packages from globally-installed symbolic link
* To run taco-cli run 
```
taco
```
* Similarly to run remotebuild run
```
remotebuild
```
#### Running tests

Please run following to make sure all tests are passing
```
gulp run-tests
```

#### Getting tests coverage

To check test coverage, please run following command
```
gulp coverage
```

#### Coding guidelines
TACO uses tslint rules specified in [tslint.json](https://github.com/Microsoft/TACO/blob/master/tools/tslint.json). Run following command to make sure code is tslint clean
```
gulp tslint
```

## LICENSE

TACO is licensed under the MIT Open Source license.

## Code of conduct
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
