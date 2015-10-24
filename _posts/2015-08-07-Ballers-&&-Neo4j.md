---
layout: post
title: Ballers && Neo4j
header-img: "img/nba.jpg"
---

<p>We are now beginning our project phase and starting our first team project! My teammates and I decided to create a 6 degrees of separation with basketball players. We contemplated about where we were going to get this data as well as the method of storage. We found a website that specifically stores all NBA records, <a href='http://www.basketball-reference.com/'>basketball-reference</a>. Initially, we thought about using a relational database such as MySQL, but we decided to challenge ourselves and try Neo4j, a NoSQL graph database that we haven't used before. I'll admit, it was scary to use something that we have never learned before and having to learn it on our own.</p>

## How we're using Neo4j
<p>Neo4j is a graph database that allows you to create nodes and set relationships between the nodes. This style of storing data is perfect our project! By creating player nodes and team nodes, we are able to set relationships and connect the players to the teams that they play on. What's amazing about this graph database is that it includes a localhost browser that enables you to visualize your data as nodes and relationship.</p>

<p>Another thing to note is that the syntax for Cypher Query Language is somewhat similar to sql queries once you get used to it. The documentation for this database is well written and can be easily understood. They also provide excellent examples in their docs!</p>

## How to get started
<p>First, you need Homebrew installed. Then, all you need to do is type 'brew install neo4j' in the terminal. Once installation is complete type 'neo4j start'. Once the local instance is running, simply go to 'http://localhost:7474' on your browser to access the database GUI. Let me tell you, that GUI is amazing! It so much easier when you can visualize the data that you are working with.</p> 

## Basic Commands
<p>Use the "CREATE" command to create a node. In the example below, I've created a node with a label 'Person' and with properties 'name' and 'from'.</p>

{% highlight javascript %}
CREATE (n:Person { name: "Kent", from: "Oakland, CA" })
RETURN n
{% endhighlight %}

<p>Use the "MATCH" command to search for nodes.</p>

{% highlight javascript %}
MATCH (n)
RETURN n
{% endhighlight %}

<p>create relationships by using the "CREATE" command and the arrow with relationship type in between.</p>

{% highlight javascript%}
MATCH (a:Person),(b:Person)
WHERE a.name = 'Kent' AND b.name = 'John'
CREATE (a)-[r:IS_FRIENDS_WITH]->(b)
RETURN r
{% endhighlight %}

<img src="{{ site.baseurl }}/img/neo4j_01.jpg" alt="friends">

## 

<p>One issue that we ran into while working on our project is having to deal with duplicate players. For example, when a player is traded to a different team in the season. They show up in multiple teams and are not connecting. Another issue that we're running into is having to deal with the aspect of time. A player will stay with a team for multiple seasons and to overcome this we have to create the same team nodes for every season. Thereby creating too many team nodes.</p>



<p>Please refer to the Neo4j Documentation for other query commands <a href='http://neo4j.com/docs/'>HERE</a>




## We're Finished!
<p>Check out our site! <a href='http://sixdribbles.com/'>SixDribbles!</a></p>