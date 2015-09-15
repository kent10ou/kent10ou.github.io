---
layout: post
title: Intro to React Native!
---

<p>React Native is currently the new hotness right now for developing apps for mobile. It allows you to build native iOS and Android apps in Javascript and React. You can think of React as taking charge of the Views controller. There is no data binding and no event management. When the data changes, React will automatically change what the view should look. To get started, simply use Homebrew to install Node and watchman.</p>

{% highlight javascript %}
brew install node

brew install watchman
{% endhighlight %}

<p>Watchman is a filewatcher from Facebook, that will watch for code changes and rebuild. Next, install React Native CLI tool by typing: </p>

{% highlight javascript %}
npm install -g react-native-cli
{% endhighlight %}

<p>Go to the directory where you want to create a new react native project and run this command... where the ProjectName is whatever you want to call the project</p>

{% highlight javascript %}
react-native init ProjectName
{% endhighlight %}

<p>Once the process is done, head into the folder and open the Xcode project.
Then open the index.ios.js file and edit some lines. Hit ⌘-R to build and run the simulator in Xcode. Press ⌘-D to enable debugging in Chrome.</p>

##The different parts of the Index

<p>When I first tested out React Native, I was so surprised to see that the code was so simple. It seems that React is doing the majority of in the background.</p>

```
'use strict';

var React = require('react-native');
```








