## Festival: React Native

![Screenshot](react-demo-app-screenshot.png)

This is a skeleton React Native App for Wagtail sites. It's based on an app by [Josh Barr](https://github.com/JoshBarr) from [Springload](http://www.springload.co.nz/) for [New Zealand Festival](http://www.festival.co.nz/). It speaks to the [API](http://www.festival.co.nz/public-api/v1/pages/) on the live festival website.

### Getting started

1. Follow the [React Native guide](https://facebook.github.io/react-native/docs/getting-started.html) to set up the tools you'll need in your developer environment.
2. ```bash
git clone git@github.com:tomdyson/react-native-example.git
cd react-native-example
```
3. Open ios/Festival.xcodeproj in Xcode

### Testing on a simulator:

To develop on the iOS simulator, the default settings in `AppDelegate.m` (xcode)
will be fine:

```
jsCodeLocation = [NSURL URLWithString:@"http://localhost:8081/index.ios.bundle?platform=ios&dev=true"];
```

For developing on a device rapidly, you can change `localhost` above to your machine's local IP address, eg:

```
jsCodeLocation = [NSURL URLWithString:@"http://10.0.0.96:8081/index.ios.bundle?platform=ios&dev=true"];
```

__note__: This will only work with real devices, not with builds targeting the iOS simulator.

When you want to develop/test on a real device, it's easiest to bundle the JS
with the app. You can do that by uncommenting this line:

```
//   jsCodeLocation = [[NSBundle mainBundle] URLForResource:@"main" withExtension:@"jsbundle"];
```

### Signing authorities:

To test on a real device, you'll need to have xCode signed in to the Apple Developer Programme.

There's details in the UPM. Look for `mobile@springload.co.nz`.
