[](https://github.com/pwa-builder/PWABuilder)

![PWABuilder Logo](https://docs.pwabuilder.com/#/home/pwa-introassets/icons/pwa-builder.png)

Home PWABuilder PWA Starter PWABuilder Studio

- **Home**
    - [About](#/ "PWABuilder Suite Documentation")
    - [PWA Overview](#/home/pwa-intro "Beginner's Guide to PWA")
        - [What Makes A PWA?](#/home/pwa-intro?id=what-makes-a-pwa "What Makes A PWA?")
        - [Installability](#/home/pwa-intro?id=installability "Installability")
        - [Design](#/home/pwa-intro?id=design "Design")
        - [Demo](#/home/pwa-intro?id=demo "Demo")
        - [Next Steps](#/home/pwa-intro?id=next-steps "Next Steps")
    - [Service Workers](#/home/sw-intro "Introduction to Service Workers")
    - [Adding Native Features](#/home/native-features "Adding Native Features to Your PWA")
    - [PWA Workshop](#/home/pwa-workshop "Progressive Web App Intro Workshop")
    - [Resources](#/home/resources "Resources")

### Free Microsoft Developer Account Promotion

PWABuilder is giving away free Microsoft Developer accounts (approximately $19 in value) to PWA developers. In order to qualify, you must have a PWA that meets the following requirements:

- own a PWA that is installable, contains all required manifest fields, and implements at least two desktop enhancements
- live in a country or region where the Windows program in Partner Center is offered.
- have a valid Microsoft Account to use to sign up for the Microsoft Store on Windows developer account
- not have an existing Microsoft Store on Windows individual developer/publisher account
- use the Store Token to create a Microsoft Store on Windows developer account within 30 calendar days of Microsoft sending you the token, using the same Microsoft Account you used to sign in here
- plan to publish an app in the store this calendar year (prior to 12/31/2023 midnight Pacific Standard Time)

**Publish your Progressive Web Apps to the Microsoft Store on Windows for Free**  
If you are an individual developer building a progressive web app, you might qualify for a free Microsoft Developer account (approximately $19 in value).  
Learn more. 

**Note** This article assumes a baseline understanding of web development. If you’re looking for resources to start your web dev journey, take a look [here.](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

# [Beginner’s Guide to Progressive Web Apps](#/home/pwa-intro?id=beginners-guide-to-progressive-web-apps)

Progressive Web Apps (often shortened to _PWA_) are web apps that use modern web technologies to create application experiences that don’t show many of the classic limitations of the web. In other words, they _progress beyond_ normal web apps, and mirror what would normally be expected of natively developed applications.

A good progressive web app can:

- Be locally installed on different devices
    
- Run smoothly in offline conditions
    
- Integrate with the user’s operating system and deliver advanced functionality
    

Progressive web apps are applications _first_, and separate themselves from websites and web apps through a combination of technology and design paradigms.

## [What Makes A PWA?](#/home/pwa-intro?id=what-makes-a-pwa)

From a technical perspective, a normal web app only needs a few extra pieces to become a progressive web app: a **_web app manifest_** and a **_service worker_**. It is also important to note that service workers require **_HTTPS_** to work properly, and progressive web apps must be served from a secure endpoint.

#### [Web App Manifests](#/home/pwa-intro?id=web-app-manifests)

A web app manifest (often shortened to web manifest, or even just _manifest_) is a `.json` file that tells the browser that your web app is a progressive web app, and is capable of being installed to the OS.

The manifest also contains other information about your app, such as the title, theme colors, and description. Your manifest can even enable certain native integrations, such as shortcuts and display modes.

Learn more [here.](https://developer.mozilla.org/en-US/docs/Web/Manifest)

#### [Service Workers](#/home/pwa-intro?id=service-workers)

Service workers are a type of [web worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers) that serve as a proxy to the network, intercepting any requests that your PWA may make. They are event-driven and operate in a separate thread from the rest of your application.

Service workers are how progressive web apps work offline: service workers can cache essential resources and handle requests when the network is down. Every request to and from a PWA goes through the service worker, and there are a ton of different strategies for how to cache and fetch necessary resources.

Learn more in the [Introduction to Service Workers](#/home/sw-intro)

Service workers only work with applications that are secured through `HTTPS`. Before you can add a service worker, make sure your app is secure.

## [Installability](#/home/pwa-intro?id=installability)

A web app that has a manifest and a service worker can be locally installed! _Installability_ is one of the key differences that separates classic web apps and their progressive counterparts.

Just like a native application, an installed PWA can be launched from the operating system, pinned to desktops and taskbars, and indexed by your device’s search software.

#### [Installing from the Browser](#/home/pwa-intro?id=installing-from-the-browser)

PWAs can be installed directly from both Google Chrome and Microsoft Edge.

Both browsers have an install button at the right end of the address bar that will appear if the current page is a PWA.

Here’s what the button and follow-up prompt look like for a PWA in Edge:

![An example PWA with the browser install prompt open](https://docs.pwabuilder.com/#/home/pwa-introassets/home/beginners/install-prompt.png)

Clicking install is all you need to access your PWA from the OS!

#### [Installing from App Stores](#/home/pwa-intro?id=installing-from-app-stores)

Depending on the platform, PWAs are now able to be installed from various app stores.

The Microsoft, Google Play, and Meta Quest stores all natively support PWAs, and the install process is the same as it would be for any app. Just search for it in the store of choice and click install.

Other platforms, such as iOS, don’t natively support PWAs, but PWAs can sometimes be wrapped in native frameworks to allow publishing to stores.

## [Design](#/home/pwa-intro?id=design)

Adding a manifest and service worker to your PWA and making it installable are just the tip of the iceberg for building quality progressive web apps.

PWAs are different than websites, and have a different standard when it comes to user experience.

A well-designed PWA will check a handful of boxes:

- Smooth, modern, and consistent UI and navigation experience (for example, the view shouldn’t refresh on navigation)
    
- Reliable offline experience. Even if your app is heavily network dependent, it should remain basically responsive when offline.
    
- Takes advantage (when appropriate) of modern web capabilities to deliver an integrated application experience.
    

In general, a good rule of thumb is that a progressive web app should feel more like an application than a website.

## [Demo](#/home/pwa-intro?id=demo)

This documentation is a PWA itself, and can be installed and used to explore some basic PWA features.

Make sure you are using Edge or Chrome before trying to install the PWA.

Here are some things to try:

#### [Install this PWA](#/home/pwa-intro?id=install-this-pwa)

Using the guidance from the _Installability_ section, install this PWA. The button is located on the far right of the address bar in either Chrome or Edge.

Once the PWA is installed, try launching it from the operating system. It should open in a standalone window without an address bar and with the PWA theme color.

#### [Use the app without connection](#/home/pwa-intro?id=use-the-app-without-connection)

Try turning on airplane mode or disconnecting from WiFi.

Navigating around the PWA should still work, and all the static content should still load. In this instance, the whole application is static, and should work entirely as expected.

**Note** Offline mode will only work if the PWA has been loaded once with a connection, which allows the service worker to precache any necessary assets.

#### [Shortcuts](#/home/pwa-intro?id=shortcuts)

Try right-clicking the PWA’s icon on your taskbar.

You’ll see shortcuts to take you directly to different parts of the documentation. Choose a shortcut to jump to documentation you’re interested in!

#### [Trigger a notification](#/home/pwa-intro?id=trigger-a-notification)

Lastly, let’s take a look at an example web capability: push notifications.

Before we can send notifications, we need to request permission from the user. This button will trigger the permission prompt:

Request Permission to Display Notifications

After permission is granted, trigger a notification:

Display a Notification

## [Next Steps](#/home/pwa-intro?id=next-steps)

If you’re ready to dive in with building your first PWA, the PWA Starter is a great place to get started.

The PWA Starter is a template that comes with a service worker and manifest built in, and allows you to jump right in with your first PWA.

Check out the Quick Start [here.](#/starter/quick-start)