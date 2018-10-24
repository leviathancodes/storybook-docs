# Polymer Storybook SDK Documentation

Polymer Storybook is a tool that allows users to detects component bugs far upstream in the development process, when you first code your components. This prevents bugs from appearing downstream in applications, when they’re harder to diagnose.  Previously, Storybook was only available for React, Due and Angular, but Applitools has listened to customer feedback and created a version for the popular Polymer library  I will take you through a step-by-step guide on how to use this set up, install, and begin using this innovative testing tool within the Universal Web Client.

Pre-requisuites:

* Applitools account:  If you do not have one set up, follow the steps for here.
* Node.js
* Polymer CLI
* NPM
* Bower

## Installing Universal Web Client Repository

First, you will need to clone the repo by running the following command in the terminal.  Be sure that you are located in the place you want the repository to be cloned.

`git clone https://github.com/GannettDigital/universal-web-client.git`

Afterwards, change into the project's directory

`cd universal-web-client`

## Install the Project and JavaScript Dependencies

Run the following command(s) to complete your set up:

`npm install && npm run install-local-globals && npm run install-third-parties`

Bob's your uncle!

**note** Please make sure that you are using Java Version 8 and not Java Version 11.  Version 11 has been known to cause issues with Selenium and Polymer Storybook

## Install wct-eyes

Install wct-eyes as dependencies using one of the following options.

`npm install wct-eyes --save-dev`

OR 

`npm install -g wct-eyes`

## Enable wct-eyes

Now that that's done, go ahead and locate the wct.conf.json file.  Open it, navigate to the plugins property and insert the following object:

`"eyes": {
	"disabled": false
	"serverURL": "https://gannetteyes.applitools.com/"
}`

## Refactoring Web Component Tests

Implementing Polymer Storybook support for pre-existing tests is a simple process, and should take you no longer than ten minutes on your first attempt.  I will be refactoring a test to implement support below.

We will use the _ test as an example.

