---
layout: post
title: Git Branching Strategies
---

![branching](https://map-client.readthedocs.io/en/latest/_images/gitflow.png)
*Img credit: https://nvie.com/posts/a-successful-git-branching-model/*

The different types of branches we may use are:

**Feature branches**

Feature/Topic branches are often a branch of the origin/develop branch and used to work on features for the next or future releases. They only exist when the feature is under development and will be merged back intoGit Branching Strategies the origin/develop branch.

**Release branches**

These are usually a branch from a point-in-time of the origin/develop where it’s deemed ready for a release. It exists to facilitate a production release. Additional minor work may happen on a release branch before it’s merged into the origin/master and origin/develop.

**Hotfix branches**

Hotfixes generally indicate fixes for issues in production that are discovered post-release. Hotfix branches are create from the origin/master and the changes merged into both origin/develop and origin/master branches.
 
## Git Flow
 
Git Flow comes from the Atlassian family tree. Git Flow describes how feature branches, release branches, master or development branches, and hotfixes are interrelated. Git Flow is useful when you have well defined numbered releases. It’s also extremely handy for large teams building downloadable software, packages and libraries where multiple versions of the project/product may be in production simultaneously. But Git Flow is often considered overkill for smaller software teams and less complicated projects/products.
 
It is not supported by Azure Devops!
 
## GitHub Flow
 
GitHub Flow has it’s origins with the GitHub team. has some of the same elements as Git Flow, such as feature branches. But unlike Git Flow, GitHub Flow combines the master and release branches into a “master” and treats hotfixes just like feature branches. It is better suited to continuous delivery models where changes can be quickly made and easily deployed, sometimes multiple times a day.
 
## Release Flow

Release Flow, a trunk-based development branching, similar to GitHub Flow comes from Microsoft, the Azure DevOps (formerly VSTS) heavily makes use of this strategy – or at least did until recently. In this strategy, the teams do not continuously deploy master to production. Instead, they release the master branch every sprint by creating a branch for each release. When the teams need to bring hotfixes into production, they cherry-pick those changes from master into the release branch. This is a simple strategy that works well particularly for those people familiar with TFVC and prevents the “merge hell” scenario described earlier.

Links
-----

**Branching Strategy**

1. [Git Branching Strategies Which one should I pick](https://www.nebbiatech.com/2019/03/15/git-branching-strategies-which-one-should-i-pick/)
1. [Git Branching Guidance Azure Devops](https://docs.microsoft.com/en-us/azure/devops/repos/git/git-branching-guidance?view=azure-devops)
1. [Choose right git branching strategy](https://www.creativebloq.com/web-design/choose-right-git-branching-strategy-121518344)
1. [Git branching strategies](https://gitversion.readthedocs.io/en/latest/git-branching-strategies/)
1. [4 branching workflows for git](https://medium.com/@patrickporto/4-branching-workflows-for-git-30d0aaee7bf)
1. [Multiple Verzweigungen Git Branching Modelle im täglichen Einsatz](
https://www.informatik-aktuell.de/entwicklung/methoden/multiple-verzweigungen-git-branching-modelle-im-taeglichen-einsatz.html)

**GitFlow**

1. [Der Gitflow Workflow](https://m.infos.seibert-media.net/Productivity/Git-Workflows+-+Der+Gitflow-Workflow.html)
2. [GitFlow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
3. [Introducing GitFlow](https://datasift.github.io/gitflow/IntroducingGitFlow.html)
4. [How do i achieve setup gitflow in azure devops repos with pr branch policies](https://stackoverflow.com/questions/56108148/how-do-i-achieve-setup-gitflow-in-azuredevops-repos-with-pr-branch-policies-on-m)

**Github Flow**

1. [GitHub Flow - Introduction](https://guides.github.com/introduction/flow/)
1. [GitHub Flow - Overview](http://guides.github.com/overviews/flow/)
1. [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
1. [Tips to enhance your github flow](https://hackernoon.com/15-tips-to-enhance-your-github-flow-6af7ceb0d8a3)

**Release Flow**

1. [Release Flow](https://docs.microsoft.com/en-us/azure/devops/learn/devops-at-microsoft/release-flow)
1. [Release Flow - How do we do branching on the vsts team](https://devblogs.microsoft.com/devops/release-flow-how-we-do-branching-on-the-vsts-team/)

**Flow vs Flow**

1. [Git Flow vs. GitHub Flow](https://lucamezzalira.com/2014/03/10/git-flow-vs-github-flow/)
1. [Tunk based development vs git flow](https://codeburst.io/trunk-based-development-vs-git-flow-a0212a6cae64)