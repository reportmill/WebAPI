
# WebAPI

## Overview

This project is a Java bridge to the JavaScript WebAPIs in the browser and on the desktop.

## Leapfrog beyond Swing and JavaFX with Web APIs

The perfect Java UI framework would ideally include these features:

    - Runs in browser and desktop
    - Leverages the familiarity and ubiqity of browser programming paradigms
    - Supports advanced features like modern graphics, audio, video, animation and 3D
    - Is interoperable with most other end user technologies and services
    - Leverages the skills most end-user developers have and want

If you accept any of that, then it follows that Java UI should fundamentally be built on Web API. There is no need to
rewrite this vast functionality, Web APIs are readily available everywhere: in the browser and on the desktop (via Chrome
packaging). Web APIs are the new "AWT" - and Java doesn't have to play an impossible game of catch up.

Here are some demos of Java Web API in action, running in a Java IDE [(SnapCode)](https://reportmill.com/SnapCode) that
is itself running on WebAPI:

- Browser DOM Demos: [https://reportmill.com/SnapCode/app/#sample:DOMTests.zip](https://reportmill.com/SnapCode/app/#sample:DOMTests.zip)

<img width="569" height="480" alt="DomSamples" src="https://github.com/user-attachments/assets/3b8b1790-7b6d-4039-9479-42dad2d33bef" />

And to see a preliminary demo of SnapCode running on the desktop and using Chrome as the windowing, rendering and
runtime, [download jbang](https://www.jbang.dev/download/) and run SnapCode with this simple command:

- Desktop app: ```jbang snapcodejx@reportmill```

<img width="640" height="400" alt="SnapCode_JxBrowser" src="https://github.com/user-attachments/assets/18447094-d328-4544-b6d2-bf07e2a7983a" />

This uses the JxBrowser to easily interface with Chrome. There has only been about a week of development on this and our
evaluation license runs out soon. But we hope to add polish and figure out a JxBrowser licensing solution once the project
generates more interest.

## How to use

Since the WebAPI framework is a wrapper, it needs access to a real WebAPI implementation. On the desktop, this can be done
with the [JxBrowser](https://teamdev.com/jxbrowser) library. In the browser, this can be done with [CheerpJ](https://cheerpj.com).
This project contains an adapter for each of those environments.

# Use with CheerpJ

To run this library in the browser with CheerpJ, follow these steps:

    - ./gradlew build
    - Copy cjdom.js and cjdom.html to build/libs dir
    - Run some http-server in that directory
    - Go to http://localhost:8080/cjdom.html in your browser

# Use with JxBrowser

To use this library on the desktop with JxBrowser:

    - Edit build.gradle
    - Uncomment jxbrowser dependency for platform
        - This is one of: mac, win, mac-arm, win-arm or linux

You will also need to get a JxBrowser key from the JxBrowser people by clicking on the
["Try for free"](https://teamdev.com/jxbrowser/#evaluate) link.
