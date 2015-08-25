---
layout: post
title: Understanding Git Workflow
---

While working on our neo4j project, we encountered a bunch of git issues. This being my first project work, it felt like I was being thrown into the deep end of the pool. There were many merge conflicts and rebase issues caused by multiple people working on the same file or feature. When we couldn't figure it out... we would have to delete our entire repo and refork and clone. This process is not ideal, but it worked... For our next project together, I chose to be the scrum master, who is in charge of the project process. We set up our issues workflow with waffle.io which helps us visualize the status of each feature in our project. I would also maintain the git issues and merge conflicts. I'll try to explain my understanding of git merge and rebase here

## Git Rebase and Merge
One thing to keep in mind.. git rebase & git merge essentially do the same thing. They take changes from one branch and combine it with another branch, but they do it very differently. 
