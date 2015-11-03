---
layout: post
title: Intro to React Native!
---

##React Native!
<p>React Native is currently the new hotness right now for developing apps for mobile. It allows you to build native iOS and Android apps in Javascript and React. You can think of React as taking charge of the Views controller in a MVC framework. There is no data binding and no event management! When the data changes, React will automatically change what the view should look. To get started, simply use Homebrew to install Node and watchman.</p>

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

##The Basics
<p>When I first tested out React Native, I was surprised to see such a simple codebase. It seems that React is doing the majority of the work in the background.</p>

{% highlight javascript %}
'use strict';
var React = require('react-native');
{% endhighlight %}

<p>All files in React Native will consist of a few basic parts. It uses strict mode to enable better error handling. The second line is what loads the react-native modules.</p>

<p>The next component that we will often see is called the destructuring assignment. We set all the elements that are needed to the variable 'React'. This will simplify the code later so we won't have to type 'React.element' everytime.</p>

{% highlight javascript %}
var {
	AppRegistry,
  StyleSheet,
  Text,
  View,
  TouchableHighlight,
  Component,
  AlertIOS
}
{% endhighlight %}

##Styling
<p>How we're styling the app is with the Stylesheet. It uses CSS like styling for our view components. Not all CSS attributes are available, but it's enough to create a good looking view. What's great is we can put the stylesheet right into the js file we're working on. Here's an example:</p>

{% highlight javascript %}
var styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#FFFFFF'
  },
  buttonText: {
    fontSize: 18,
    color: 'white',
    alignSelf: 'center'
  },
  button: {
    height: 44,
    flexDirection: 'row',
    backgroundColor: '#48BBEC',
    alignSelf: 'stretch',
    justifyContent: 'center'
  }
});
{% endhighlight %}

T








