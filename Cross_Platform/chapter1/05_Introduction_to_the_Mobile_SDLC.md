#移动应用开发生命周期简介
**开发移动应用程序时的注意事项**

本文讨论了关于移动应用软件开发的生命周期, 并讨论了一些当构建移动应用项目时需要考虑的事项。要是开发人员想要尽快开始构建,可以跳过本指南，阅读后面更完整的移动开发的内容。


##概述
构建移动应用程序可以像打开你的IDE一样简单, 塞点东西, 做一点快速测试, 并提交到一个App商店 – 所有工作在一个下午完成。或者它可以是一个非常复杂的过程，包括严格的预先设计, 可用性测试, 成千上万的设备上的QA测试, 一个完整的beta生命周期, 然后是许多的部署方式。

在本文档, 我们将要全面介绍如何构建一个Xamarin移动应用程序, 包括：

1. **过程** – 软件开发过程叫软件开发生命周期 (SDLC)。We’ll examine all phases of the SDLC with respect to mobile application development, including: Inspiration, Design, Development, Stabilization, Deployment, and Maintenance.
2. **注意事项** – There are a number of considerations when building mobile applications, especially in contrast to traditional web or desktop applications. We’ll examine these considerations and how they affect mobile development.

This document is intended to answer fundamental questions about mobile app development, for new and experienced application developers alike. It takes a fairly comprehensive approach to introducing most of the concepts you’ll run into during the entire Software Development Lifecycle (SDLC). However, this document may not be for everyone, if you’re itching to just start building applications, we recommend jumping ahead to either the [Introduction to Mobile Development](http://developer.xamarin.com/guides/android/getting_started/introduction_to_mobile_development), [Hello, Android](http://developer.xamarin.com/guides/android/getting_started/hello%2c_world) or [Hello, iPhone](http://developer.xamarin.com/guides/ios/getting_started/hello%2c_world) tutorials, and then coming back to this document later.


##手机应用开发 SDLC
The lifecycle of mobile development is largely no different than the SDLC for web or desktop applications. As with those, there are usually 5 major portions of the process:

1. **Inception** – All apps start with an idea. That idea is usually refined into a solid basis for an application.
2. **Design** – The design phase consists of defining the app’s User Experience (UX) such as what the general layout is, how it works, etc., as well as turning that UX into a proper User Interface (UI) design, usually with the help of a graphic designer.
3. **Development** – Usually the most resource intensive phase, this is the actual building of the application.
4. **Stabilization** – When development is far enough along, QA usually begins to test the application and bugs are fixed. Often times an application will go into a limited beta phase in which a wider user audience is given a chance to use it and provide feedback and inform changes.
5. **Deployment**

Often many of these pieces are overlapped, for example, it’s common for development to be going on while the UI is being finalized, and it may even inform the UI design. Additionally, an application may be going into a stabilization phase at the same that new features are being added to a new version.

Furthermore, these phases can be used in any number of SDLC methodologies such as Agile, Spiral, Waterfall, etc.

Let’s cover how each of these phases play a part in Mobile Development.


###Inception
The ubiquity and level of interaction people have with mobile devices means that nearly everyone has an idea for a mobile app. Mobile devices open up a whole new way to interact with computing, the web, and even corporate infrastructure.

The inception stage is all about defining and refining the idea for an app. In order to create a successful app, it’s important to ask some fundamental questions. For example, if you’re developing an app for distribution in a public app store, some considerations are:

* **Competitive Advantage** – Are there similar apps out there already? If so, how does this application differentiate from others?

If you’re intending for the app to be distributed in the enterprise:

* **Infrastructure Integration** – What existing infrastructure will it integrate with or extend?

Additionally, you should evaluate the usage of the app in a mobile form factor:

* **Value** – What value does this app bring users? How will they use it?
* **Form/Mobility** – How will this app work in a mobile form factor? How can I add value using mobile technologies such as location awareness, the camera, etc.?

To help with designing the functionality of an app, it can be useful to define Actors and [Use Cases](http://en.wikipedia.org/wiki/Use_case). Actors are roles within an application and are often users. Use cases are typically actions or intents.

For instance, if you’re building a task tracking application, you might have two Actors: `User` and `Friend`. A User might `Create a Task`, and `Share a Task` with a Friend. In this case, creating a task and sharing a task are two distinct use cases that, in tandem with the Actors, will inform what screens you’ll need to build, as well as what business entities and logic will need to be developed.

If you’ve captured the appropriate use cases and actors, it’s much easier to begin designing an application because you know exactly what you need to design, so the question becomes, how to design it, rather than what to design.


###Designing Mobile Applications
Once you have a good idea of what it is you want to design, the next step is start trying to solve the User Experience or UX.


####UX Design
UX is usually done via wireframes or mockups using tools such as [Balsamiq](http://www.balsamiq.com/), [Mockingbird](https://gomockingbird.com/), [Visio](http://office.microsoft.com/en-us/visio/), or just plain ol’ pen and paper. UX Mockups allow you to quickly design UX without having to worry about the actual UI design:

![Balsamiq](05-Balsamiq.png)

When creating UX Mockups, it’s important to consider the Interface Guidelines for the various platforms that you’re designing for. By adhering to platform-specific guidelines, you can ensure that your apps feel at home on each platform. You can find each guide as follows:

1. Apple - [Human Interface Guidelines](http://developer.apple.com/library/ios/#DOCUMENTATION/UserExperience/Conceptual/MobileHIG/Introduction/Introduction.html)
2. Android – [Design Guidelines](http://developer.android.com/design/index.html)
3. Windows Phone – [Design library for Windows Phone](http://msdn.microsoft.com/en-US/library/windowsphone/design/fa00461b-abe1-41d1-be87-0b0fe3d3389d(v=vs.105).aspx)

For example, each app has a metaphor for switching between sections in an application. iOS uses a tabbar at the bottom of the screen, Android uses a tabbar at the top of the screen, and Windows Phone uses the Panorama view:

![x](05-38.png)

Additionally, the hardware itself also dictates UX decisions. For example, iOS devices have no physical `back` button, and therefore introduce the Navigation Controller metaphor:

![Navigation_Controller](05-01_-_Navigation_Controller.png)

Furthermore, form factor also influences UX decisions. A tablet has far more real estate, so you can fit more information, and often what needs multiple screens on a phone is compressed into one for a tablet:

![iPhone_vs_iPad](05-iPhone_vs_iPad.png)

And due to the myriad of form factors out there, there are often mid-size form factors (somewhere between a phone and a tablet) that you may also want to target.

####User Interface (UI) Design
Once you’ve nailed down the UX in your application, the next step is to create the UI design. While UX is typically just black and white mockups, the UI Design phase is where colors, graphics, etc., are introduced and finalized. Spending time on good UI design is important and generally, the most popular apps have a professional design.

As with UX, it’s important to understand that each platform has it’s own design language, so a well-designed application may still look different on each platform:

![](05-multiplatform-1.png) 

For good UI design inspiration, check out some of the following sites:

1. [pttrns.com](http://pttrns.com/) – (iOS only)
2. [androidpttrns.com](http://androidpttrns.com/) - (Android only)
3. [lovelyui.com](http://lovelyui.com/) – (iOS, Android, and Windows Phone)
4. [mobiledesignpatterngallery.com](http://mobiledesignpatterngallery.com/) – (iOS, Android, and Windows Phone)

Additionally, you can find graphic designer portfolios at sites such as [Behance.com](http://behance.com/) and [Dribbble.com](http://dribbble.com/). Designers from all over the world can be found there, often times in places where the exchange rate is favorable, so good graphic design doesn’t necessarily have to cost a lot.


###Development
The development phase usually starts very early. In fact, once an idea has some maturation in the conceptual/inspiration phase, often a working prototype is developed that validates functionality, assumptions, and helps to give an understanding of the scope of the work.

In the rest of the tutorials, we’ll focus largely on the development phase.


###Stabilization
Stabilization is the process of working out the bugs in your app. Not just from a functional standpoint, e.g.: "It crashes when I click this button,” but also Usability and Performance. It’s best to start stabilization very early within the development process so that course corrections can occur before they become costly. Typically, applications go into `Prototype`, `Alpha`, `Beta`, and `Release Candidate` stages. Different people define these differently, but they generally follow the following pattern:

1. **Prototype** – The app is still in proof-of-concept phase and only core functionality, or specific parts of the application are working. Major bugs are present.
2. **Alpha** – Core functionality is generally code-complete (built, but not fully tested). Major bugs are still present, outlying functionality may still not be present.
3. **Beta** – Most functionality is now complete and has had at least light testing and bug fixing. Major known issues may still be present.
4. **Release Candidate** – All functionality is complete and tested. Barring new bugs, the app is a candidate for release to the wild.

It’s never too early to begin testing an application. For example, if a major issue is found in the prototype stage, the UX of the app can still be modified to accommodate it. If a performance issue is found in the alpha stage, it’s early enough to modify the architecture before a lot of code has been built on top of false assumptions.

Typically, as an application moves further along in the lifecycle, it’s opened to more people to try it out, test it, provide feedback, etc. For instance, prototype applications may only be shown or made available to key stakeholders, whereas release candidate applications may be distributed to customers that sign up for early access.

For early testing and deployment to relatively few devices, usually deploying straight from a development machine is sufficient. However, as the audience widens, this can quickly become cumbersome. As such, there are a number of test deployment options out there that make this process much easier by allowing you to invite people to a testing pool, release builds over the web, and provide tools that allow for user feedback.

Some of the most popular ones are:

1. **Testflight (testflightapp.com)** – This is an iOS product that allows you to distribute apps for testing as well as receive crash reports and usage information from your customers.
2. **LaunchPad (launchpadapp.com)** – Designed for Android, this service is very similar to TestFlight.
3. **Vessel (vessel.io)** – A service for iOS and Android that lets you monitor usage, track customers and even do A/B testing from inside your app.

4. **hockeyapp.com**

provides a similar service for iOS, Android and Windows Phone.

###Distribution
Once you’ve stabilized your application, it’s time to get it out into the wild. There are a number of different distribution options, depending on the platform.

Xamarin.iOS and Objective-C apps are distributed in exactly the same way:

1. **Apple App Store** – Apple’s App Store is a globally available online application repository that is built into Mac OS X via iTunes. It’s by far the most popular distribution method for applications and it allows developers to market and distribute their apps online with very little effort.
2. **Enterprise Deployment** – Enterprise deployment is meant for internal distribution of corporate applications that aren’t available publicly via the App Store.
3. **Ad-Hoc Deployment** – Ad-hoc deployment is intended primarily for development and testing and allows you to deploy to a limited number of properly provisioned devices. When you deploy to a device via Xcode or Xamarin Studio, it is known as ad-hoc deployment.

####Android
All Android applications must be signed before being distributed. Developers sign their applications by using their own certificate protected by a private key. This certificate can provide a chain of authenticity that ties an application developer to the applications that developer has built and released. It must be noted that while a development certificate for Android can be signed by a recognized certificate authority, most developers do not opt to utilize these services, and self-sign their certificates. The main purpose for certificates is to differentiate between different developers and applications. Android uses this information to assist with enforcement of delegation of permissions between applications and components running within the Android OS.

Unlike other popular mobile platforms, Android takes a very open approach to app distribution. Devices are not locked to a single, approved app store. Instead, anyone is free to create an app store, and most Android phones allow apps to be installed from these third party stores.

This allows developers a potentially larger yet more complex distribution channel for their applications. [Google Play](https://play.google.com/store?hl=en) is Google’s official app store, but there are many others. A few popular ones are:

1. [AppBrain](http://www.appbrain.com/)
2. [Amazon App Store for Android](http://www.amazon.com/mobile-apps/b?ie=UTF8&node=2350149011)
3. [Handango](http://www.handango.com/)
4. [GetJar](http://www.getjar.com/)

###Windows Phone
Windows Phone applications are distributed to users via the Windows Store. Developers submit their apps to the [Windows Phone Dev Center](https://dev.windowsphone.com/) for approval, after which they appear in the Store.

Microsoft provides detailed instructinos for [deploying Windows Phone apps](http://msdn.microsoft.com/en-us/library/windowsphone/develop/ff402565(v=vs.105).aspx) during development.

Follow [these steps](http://dev.windowsphone.com/en-us/publish) to publish apps for beta testing and release to the store. Developers can submit their apps and then provide an install link to testers, before the app is reviewed and published.


##Mobile Development Considerations
While developing mobile applications isn’t fundamentally different that traditional web/desktop development in terms of process or architecture, there are some considerations to be aware of.

Let’s take a look at common considerations and then we’ll examine platform specific considerations.


###Common Considerations

####Multitasking
There are two significant challenges to multitasking (having multiple applications running at once) on a mobile device. First, given the limited screen real estate, it is difficult to display multiple applications simultaneously. Therefore, on mobile devices only one app can be in the foreground at one time. Second, having multiple applications open and performing tasks can quickly eat battery power.

Each platform handles multitasking differently, which we’ll explore in a bit.


####Form Factor
Mobile devices generally fall into two categories, phones and tablets, with a few crossover devices in between. Developing for these form factors is generally very similar, however, designing applications for them can be very different. Phones have very limited screen space, and tablets, while bigger, are still mobile devices with less screen space than even most laptops. Because of this, mobile platform UI controls have been designed specifically to be effective on smaller form factors.


####Device and OS Fragmentation
It’s important to take into account different devices throughout the entire software development lifecycle:

1. **Conceptualization and Planning** – Because different devices can have different hardware and device features, you must keep in mind that an application that relies on certain features may not work properly on certain devices. For example, not all devices have cameras, so if you’re building a video messaging application, some devices may be able to play videos, but not take them.
2. **Design** – When designing an application’s User Experience (UX), different screen ratios and sizes should be kept in mind. Additionally, when designing an application’s User Interface (UI), different screen resolutions should be considered.
3. **Development** – When using a feature from code, the presence of that feature should always be tested first. For example, before using a device feature, such as a camera, always query the OS for the presence of that feature first. Then, when initializing the feature/device, make sure to request currently supported from the OS about that device and then use those configuration settings.
4. **Testing** – It’s incredibly important to test your application early and often on actual devices. Even devices with the same hardware specs can vary widely in their behavior.

####Limited Resources
Mobile devices get more and more powerful all the time, but they are still mobile devices that have limited capabilities in comparison to desktop or notebook computers. For instance, desktop developers generally don’t worry about memory capacities; they’re used to having both physical and virtual memory in copious quantities, whereas on mobile devices you can quickly consume all available memory just by loading a handful of high-quality pictures.

Additionally, processor-intensive applications such as games or text recognition can really tax the mobile CPU and adversely affect device performance.

Because of considerations like these, it’s important to code smartly and to deploy early and often to actual devices in order to validate responsiveness.


###iOS Considerations

####Multitasking
Multitasking is very tightly controlled in iOS, and there are a number of rules and behaviors that your application must conform to when another application comes to the foreground, otherwise your application will be terminated by iOS.


####Device-Specific Resources
Within a particular form factor, hardware can vary greatly between different models. For instance, some devices have a rear-facing camera, some also have a front-facing camera, and some have none.

Some older devices (iPhone 3G and older) don’t even allow multitasking.

Because of these differences between device models, it’s important to check for the presence of a feature before attempting to use it.


####OS Specific Constraints
In order to make sure that applications are responsive and secure, iOS enforces a number of rules that applications must abide by. In addition to the rules regarding multitasking, there are a number of event methods out of which your app must return in a certain amount of time, otherwise it will get terminated by iOS.

Also worth noting, apps run in what’s known as a Sandbox, an environment that enforces security constraints that restrict what your app can access. For instance, an app can read from and write to its own directory, but if it attempts to write to another app directory, it will be terminated.


###Android Considerations

####Multitasking
Multitasking in Android has two components; the first is the activity lifecycle. Each screen in an Android application is represented by an Activity, and there is a specific set of events that occur when an application is placed in the background or comes to the foreground. Applications must adhere to this lifecycle in order to create responsive, well-behaved applications. For more information, see the [Activity Lifecycle](http://developer.xamarin.com/guides/android/application_fundamentals/activity_lifecycle) guide.

The second component to multitasking in Android is the use of Services. Services are long-running processes that exist independent of an application and are used to execute processes while the application is in the background. For more information see the [Creating Services](http://developer.xamarin.com/guides/android/application_fundamentals/services) guide.


####Many Devices & Many Form Factors
Unlike iOS, which has a small set of devices, or even Windows Phone, which only runs on approved devices that meet a minimum set of platform requirements, Google doesn’t impose any limits on which devices can run the Android OS. This open paradigm results in a product environment populated by a myriad of different devices with very different hardware, screen resolutions and ratios, device features, and capabilities.

Because of the extreme fragmentation of Android devices, most people choose the most popular 5 or 6 devices to design and test for, and prioritize those.


####Security Considerations
Applications in the Android OS all run under a distinct, isolated identity with limited permissions. By default, applications can do very little. For example, without special permissions, an application cannot send a text message, determine the phone state, or even access the Internet! In order to access these features, applications must specify in their application manifest file which permissions they would like, and when they’re being installed; the OS reads those permissions, notifies the user that the application is requesting those permissions, and then allows the user to continue or cancel the installation. This is an essential step in the Android distribution model, because of the open application store model, since applications are not curated the way they are for iOS, for instance. For a list of application permissions, see the [Manifest Permissions](http://developer.android.com/reference/android/Manifest.permission.html) reference article in the Android Documentation.


###Windows Phone Considerations

####Multitasking
Multitasking in Windows Phone also has two parts: the lifecycle for pages and applications, and background processes. Each screen in an application is an instance of a Page class, which has events associated with being made active or inactive (with special rules for handling the inactive state, or being "tombstoned”). For more information see the [Execution Model Overview for Windows Phone](http://msdn.microsoft.com/en-us/library/windowsphone/develop/ff817008(v=vs.92).aspx) documentation.

The second part is providing background agents for processing tasks even when the application is not running in the foreground. More information on scheduling periodic tasks or creating resource intensive background tasks can be found in the [Background Agents Overview](http://msdn.microsoft.com/en-us/library/windowsphone/develop/hh202942(v=vs.92).aspx).


####DEVICE Capabilities
Although Windows Phone hardware is fairly homogeneous due to the strict guidelines provided by Microsoft, there are still components that are optional and therefore require special considering while coding. Optional hardware capabilities include the camera, compass and gyroscope. There is also a special class of low-memory (256MB) that requires special consideration, or developers can opt-out of low-memory support.


####Database
Both iOS and Android include the SQLite database engine that allows for sophisticated data storage that also works cross-platform. Windows Phone 7 did not include a database, while Windows Phone 7.1 and 8 include a [local database engine](http://msdn.microsoft.com/en-us/library/windowsphone/develop/hh202860(v=vs.105).aspx) that can only be queried with LINQ to SQL and does not support Transact-SQL queries. There is an [open-source port of SQLite](http://code.google.com/p/csharp-sqlite/) available that can be added to Windows Phone applications to provide familiar Transact-SQL support and cross-platform compatibility.


####Security Considerations
Windows Phone applications are run with a restricted set of permissions that isolates them from one another and limits the operations they can perform. Network access must be performed via specific APIs and inter-application communication can only be done via controlled mechanisms. Access to the file-system is also restricted; the Isolated Storage API provides key-value pair storage and the ability to create files and folders in a controlled fashion (refer to the [Isolated Storage Overview](http://msdn.microsoft.com/en-us/library/ff402541(v=vs.92).aspx) for more information).

An application’s access to hardware and operating system features is controlled by the capabilities listed in its manifest file (similar to Android). The manifest must declare the features required by the application, so that users can see and agree to those permissions and also so that the operating system allows access to the APIs. Applications must request access to features like the contacts or appointments data, camera, location, media library and more. See Microsoft’s [Application Manifest](http://msdn.microsoft.com/en-us/library/windowsphone/develop/ff769509(v=vs.92).aspx) File documentation for additional information.


##Summary
This guide gave an introduction to the SDLC as it relates to mobile development. It introduced general considerations for building mobile applications and examined a number of platform-specific considerations including design, testing, and deployment.