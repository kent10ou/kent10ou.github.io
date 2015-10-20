---
layout: post
title: "Understanding Git Workflow"
subtitle: "Git Merge && Git Rebase"
---

##Background
<p>While working on our Neo4j project, my team and I encountered a bunch of Git issues. This being my first project work, it felt like I was being thrown into the deep end of the pool. There were many merge conflicts and rebase issues caused by multiple people working on the same file or feature. When we couldn't figure it out... we would have to delete our entire repo, refork, and clone.</p>

<p>After reading more blogs regarding git merge and rebase, I think I have a better understanding of it now and I'll try my best to explain here.</p>

## Git Rebase and Merge
<p>Note!!! One thing to keep in mind... Git rebase & Git merge essentially do the same thing!!!</p>

<p>They take changes from one branch and combine it with another branch, but they do it very differently.</p>

<p>For example, if you start working on a new feature in a branch, and another teammate updates the master branch with new commits. This results in a forked history.</p>

<img src="{{ site.baseurl }}/img/git-merge-01.jpg" alt="fork">

<p>So now we have two options to merge the changes. Merging or Rebasing.</p>

##Git Merge
<p>The simplest way is to merge the master branch into the feature branch using the command:</p>

{% highlight javascript %}
git checkout feature
git merge master
{% endhighlight %}

Or, you can write it in one line with:
{% highlight javascript %}
git merge master feature
{% endhighlight %}

<p>This will create a new merge commit in the feature branch that brings together the history of both branches.</p>

<img src="{{ site.baseurl }}/img/git-merge-02.jpg" alt="merge">

<p>Merging is also a non-destructive operation. Meaning the existing branches are not changed and avoids the downfalls of rebasing.</p>

<p>However, this means that the feature branch is littered with extra merge commits every time you need to add upstream changes. If your master branch is very active, this can pollute your feature branch's history and make it difficult to understand.</p>

##Git Rebase
<p>You can rebase the feature branch onto master by using these commands:
{% highlight javascript %}
git checkout feature
git rebase master
{% endhighlight %}

This moves the entire feature branch in front of the master branch. Rebase rewrites the history by creating new commits for each commitin the original branch.</p>

<img src="{{ site.baseurl }}/img/git-merge-03.jpg" alt="rebase">

<p>Rebasing creates a much cleaner project history. It eliminates unnecessary merge commits required by git merge. In addition, it also creates a linear project history, making it easier to navigate your project.</p>

##The Golden Rule of Rebasing
<p>The golden rule of git rebase is to never use it on public branches. For example, what would happen if you rebased master onto your feature branch?</p>

<p>The rebase will move all of the commits in master onto the tip of the feature branch. However, all of this will only happen in your repository, while everyone else is still on the original master.</p>

<p>Please refer to this link for a more in depth look at git merge and git rebase. <a href="https://www.atlassian.com/git/tutorials/merging-vs-rebasing/workflow-walkthrough">Click Here!</a></p>


