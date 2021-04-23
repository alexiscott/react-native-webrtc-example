- [Preliminary steps.](#orgd1aa54c)
- [Setup for a Mac and a real iphone](#org6d5c336)
  - [Reality check. Running **any** Native App on an IOS Device](#org11210c1)
  - [Running **this** app on an IOS device.](#org2150da1)
  - [Open a simulator for a different app using Android](#org523979c)

<https://github.com/alexiscott/wacuri> <https://github.com/alexiscott/wacuri-api>


<a id="orgd1aa54c"></a>

# Preliminary steps.

1.  Setup the backend over <https://github.com/alexiscott/wacuri-api> - This process basically involves creating a broker and having it available on a public URL. It's important that this happens before you

2.  Now add the uri to the broker's public URL in this repo in the App.js file.


<a id="org6d5c336"></a>

# Setup for a Mac and a real iphone


<a id="org11210c1"></a>

## Reality check. Running **any** Native App on an IOS Device

First checkout this YouTube video

[014 Running our React Native App on an iOS Device - YouTube](https://www.youtube.com/watch?v=Ya3VCVNrEmU)

In order to keep things as simple as possible, I did this with the default react-native app that you get when you run `npx react-native init`

The Steps include:

-   Plug in iPhone to USB.
-   Open ios/xcodeworkspace
-   Sign your app . You need a dev account for this.


<a id="org2150da1"></a>

## Running **this** app on an IOS device.

Run initial tasks

```shell
npm install
cd ios
pod install
```

1.  Open the workspace file in `Xcode` `basicwebrtcexample.xcworkspace` . You will need to have configured `Xcode` to work with the frontend app, to work with your App and to open in an iphone. TODO Add LINK. Now, Build the APP via Xcode.

1.  Trust the app on the real iphone under Settings/General/Profiles and device management/
2.  Open the app. You might get a message about the app not being on the same network. I unplugged the USB socket and then the app opened with the camera steam working.


<a id="org523979c"></a>

## Open a simulator for a different app using Android

This is where you will be able to start using the message broker for the two apps to talk to one another, and for sharing audio and video streams of course.

I did this on Linux. You will need to have setup Android Studio so as to give you access to simulators - I don't have access to an actual Android device.

Add the broker's public URL to App.js

```shell
npm start
npm run android
```

You should see the connections number on the NGROK page increase.
