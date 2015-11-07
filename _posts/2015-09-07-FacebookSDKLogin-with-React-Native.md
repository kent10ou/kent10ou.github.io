---
layout: post
title: FacebookSDKLogin with React Native
---

<p>Facebook recently released their SDK for React Native and since I have never worked with React Native or Xcode, I had a difficult time installing their login button. Eventually, I reached out to the issues log and other engineers that were successful at this. Finally, after three days... I was able to display the login button and discovered that it was due to an issue with linking the libraries and frameworks. I will now attempt to guide you through this process...</p> 

<p>Before we start, make sure you have successfully created a new React Native project. Next, take a look at this getting started guide and the repo for downloading and installing Facebook SDK frameworks for iOS - <a href="https://developers.facebook.com/docs/ios/getting-started">getting started guide</a> and <a href="https://github.com/facebook/react-native-fbsdk/">Github repo</a>.</p>

<p>Next, follow the instructions in the getting started guide to create a new Facebook app and adding their SDK to your project.</p>

<p>This is the format that my project manager follows in XCode.</p>
<img src="{{ site.baseurl }}/img/rctfbsdk_01.png" alt="fbsdk_link">

