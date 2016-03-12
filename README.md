[![WTM](http://www.wtm-montreal.com/assets/images/logo-gdg.png)](http://www.wtm-montreal.com) 
##Codelab: iOS Application Development with Swift

Apple released Swift to public in 2014 and made it open source a year later. Nowadays, Swift is one of the most popular open source project on GitHub and developers utilize Swift to develop:

- iOS, 
- MacOS, 
- WatchOS and 
- tvOS 

applications on Mac and Web applications on Linux. Swift has a modern syntax that makes programming fun and applications fast and robust. Swift combines object-oriented programming with functional programming and protocol oriented programming paradigms. Since Swift is so new and still developing, there are not a lot of expert Swift developers in the field yet. Learning Swift in these early stages can help to get ahead of competition, therefore, this codelab aims to be an accelerator for getting started with Swift programming and iOS application development. 

Codelab will start by introducing Swift related programming language paradigms and will continue by developing a simple iOS application that provides some of the essentinal mobile application capabilities such as dependency management, back-end web service integration, JSON parsing and mapping, on device data storage, navigation, listing received items and presenting views to the users.

###Prerequisites (or just come and watch):###
Some experience with programming.

####Recommended reading:
[Swift Programming Language Basics] (https://developer.apple.com/library/prerelease/mac/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html)

####Please install the following to be able to follow the codelab:
- [Xcode] (https://developer.apple.com/xcode/) + an iOS Simulator
- [Cocoapods] (https://cocoapods.org) (Dependency manager for Swift and Objective-C Cocoa projects)

####Dependencies (Included in this repo)
- [Alamofire] (https://github.com/Alamofire/Alamofire) (Elegant HTTP Networking in Swift)
- [ObjectMapper] (https://github.com/Hearst-DD/ObjectMapper) (Simple JSON Object mapping written in Swift)
- [AlamofireObjectMapper] (https://github.com/tristanhimmelman/AlamofireObjectMapper) (An Alamofire extension which converts JSON response data into swift objects using ObjectMapper)
- [Realm] (https://realm.io/docs/swift/latest/) (A mobile database)
- [fabric] (https://get.fabric.io) (Crash reporting, application distribution and analytics platform by Twitter)
- [Eureka] (https://github.com/xmartlabs/Eureka) (Elegant iOS form builder in Swift)
- [PKHUD] (https://github.com/pkluz/PKHUD) (A Swift based reimplementation of the Apple HUD) 

##Simple Backend with Kitura
Please install [Kitura] (https://github.com/IBM-Swift/Kitura) (A Swift Web Framework and HTTP Server) following steps:

1. Install [Homebrew](http://brew.sh/) (if you don't already have it installed):

 `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

2. Install the necessary dependencies:

 `brew install http-parser curl hiredis`

3. Download and install the [supported Swift compiler](#swift-version).

 After installing it, make sure you update your PATH environment variable as described in the installation instructions (e.g. export PATH=/Library/Developer/Toolchains/swift-latest.xctoolchain/usr/bin:$PATH)

4. Now you are ready to develop your first Kitura App. Check [WTM-Montreal-Backend-Kitura] (https://github.com/swift-mtl/WTM-Montreal-Backend-Kitura) 

5. Compile [WTM-Montreal-Backend-Kitura] (https://github.com/swift-mtl/WTM-Montreal-Backend-Kitura) application:

  - Mac OS X: `swift build -Xcc -fblocks -Xswiftc -I/usr/local/include -Xlinker -L/usr/local/lib`

  Or copy [Makefile and build scripts](https://github.com/IBM-Swift/Kitura-CI/blob/master/build) to your project directory and run `make build`. You may want to customize this Makefile and use it for building, testing and running your application. For example, you can clean your build directory, refetch all the dependencies, build, test and run your application by running `make clean refetch test run`.

6. Now run your new web application:

  ```
  .build/debug/wtmapp
  ```

