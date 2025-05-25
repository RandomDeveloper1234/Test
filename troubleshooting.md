# Troubleshooting
This guide will help you get started making automated UI tests for the app.
## Getting started
- Install **Node.js** because it's required for Appium.
- To install Appium open command prompt (cmd) and run: **npm install -g appium**
- Run also: **appium driver install uiautomator2**

## Create a test Class
All test classes need to have **[TestClass]** on top of them. They also need to inherit the class **BaseTest**. In the class constructor when also calling the base class constructor (like this: **public SomeTestClass(): base(...)**) there is parameters the base class takes in. Here is the list of them and their explanation:

- **reset**: It's of type bool, and it's obligatory to assign a value to it. Assign false to it if you want the app to fully close and then repopen. Assign true to it if you want the app to reset and reopen.
- **className**: It's of type string, and it's not obligatory to assign a value to it. Assign the class mame to it (like this: nameof(someClassName)) if you don't want the app to reset/close and reopen before every test method in the class. Assign an empty string to it or leave it to make the app reset/close and reopen before every test method in the class.
- **skipFirstTestForceReset**: It's of type bool, and it's obligatory to assign a value to it. The first test ignores the reset parameter and a reset happens forcefully. However if you assing true to this parameter, the first test force reset won't happen and the reset variable won't be ignored. Assign false to it or leave to not skip the first test force reset.
