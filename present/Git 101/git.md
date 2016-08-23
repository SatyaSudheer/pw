## Agenda
1. Introduction
1. What is a Distributed Version Control System?
1. TFS vs Git (CVS vs DVS)
1. How Git works? (Nuts & Bolts)
1. Git Basics
1. Git in Visual Studio
1. Basic Git Workflows

---
## Deep Dive into Git

1. What is a Distributed Version Control System?
1. The Git Repository
1. History
1. Commits
1. How Objects, Branches are Stored!
1. Merging, Fast-Forward Merges, Rebase. 

---

## Introduction
![](assets/intro.jpg)
---
1. What happens when you run $ git init
 
--

## Contents of .git folder

1. Blob — A blob object is used for storing the contents of a single file.
1. Tree — A tree object contains references to other blobs or subtrees.
1. Commit — A commit object contains the reference to another tree object and some other information(author, committer etc.)
1. Tag — A tag or a tag object is just another reference to a commit object and just makes for easier referencing.

---

# Q&A
## Thank You :)