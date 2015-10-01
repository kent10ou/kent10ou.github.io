---
layout: post
title: "Understanding Git Workflow"
subtitle: "Git Merge && Git Rebase"
---

<p>While working on our Neo4j project, my team and I encountered a bunch of Git issues. This being my first project work, it felt like I was being thrown into the deep end of the pool. There were many merge conflicts and rebase issues caused by multiple people working on the same file or feature. When we couldn't figure it out... we would have to delete our entire repo and refork and clone. This process is not ideal, but it worked for us for a while... until we finally were fed up with it and decided to learn what rebase actually does. For our next project together, I was elected to be the scrum master. The scrum master is in charge facilitating the project, making sure the team is on schedule and guiding the team. We also created our issues workflow with waffle.io, which helps us visualize the status of each feature in our project. The task I had the most trouble with was maintaining the git issues and merge conflicts. After reading more blogs regarding git merge and rebase, I think I have a better understanding of it now and I'll try my best to explain here.</p>

## Git Rebase and Merge
<p>Note! One thing to keep in mind... Git rebase & Git merge essentially do the same thing!!!
They take changes from one branch and combine it with another branch, but they do it very differently. 

Git Merge will 
