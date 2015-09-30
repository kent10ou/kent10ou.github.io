---
layout: post
title: Ballers && Neo4j
header-img: "img/nba.jpg"
---

<p>We are now beginning our project phase and starting our first team project! My teammates and I decided to create a 6 degrees of separation with basketball players. We contemplated about where we were going to get this data as well as the method of storage. We found a website that specifically stores all NBA records, <a href='http://www.basketball-reference.com/'>basketball-reference</a>. Initially, we thought about using a relational database such as MySQL, but we decided to challenge ourselves and try Neo4j, a NoSQL database that we haven't used before. I'll admit, it was scary to use something that we have never learned before and having to learn it on our own.</p>

## How we're using Neo4j
<p>Neo4j is a graph database that allows you to create nodes and set relationships between the nodes. This style of storing data is perfect our project! By creating player nodes and team nodes, we are able to set relationships and connect the players to the teams that they play on. What's amazing about this graph database is that it includes a localhost browser that enables you to visualize your data as nodes and relationship. Another thing to note is that the syntax is somewhat similar to sql once you get used to it. The documentation for this database is well written and can be easily understood. They also provide excellent examples in their docs! One issue that we're running into is having to deal with duplicate players. For example, when a player is traded to a different team in the season. They show up in multiple teams and are not connecting. Another issue that we're running into is having to deal with the aspect of time. A player will stay with a team for multiple seasons and to overcome this we have to create the same team nodes for every season. Thereby creating too many team nodes.</p>

## How to get started
<p>All you need to do is type 'brew install neo4j' in the terminal. Once installation is complete type 'neo4j start'. Once the local instance is running, simply go to 'http://localhost:7474' on your browser to access the database GUI. Let me tell you, that GUI is amazing! It so much easier when you can visualize the data that you are working with.</p> 




## We're Finished!
<p>Check out our site! <a href='http://sixdribbles.com/'>SixDribbles!</a></p>