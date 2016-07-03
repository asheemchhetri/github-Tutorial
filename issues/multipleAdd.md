<!--
==============================================================================
 @Author             : Asheem Chhetri <asheem>
 @Date               : Sunday, July 3rd 2016, 12:56:08 am
 @Email              : achhetri@purdue.edu
 @Project Name       :  
 @Last modified by   : asheem
 @Last modified time : Sunday, July 3rd 2016, 12:44:40 am
==============================================================================
-->

# Issue 3: How to un-stage multiple files.

This issue arises, when we developer by mistake initiate this command:
* git add *
So what if we modified files at different locations in our repository, which has different meaning based on file to file. We definitely do not want all those changes to have same commit memo.

---

eg:
* I modified three files: f1.c, f2.c, f3.
* I initiate the command: *git add **
  * * is a wild card, that says add all changes made so far.
* I realize that I dont want to commit all files under **one** commit memo.

---

* Initiate this command: _git reset HEAD_
* Run _git status_ to make sure you see all modified files again as "Changes not staged for commit."
* Once that is confirmed, go back to your terminal and individually add, commit and the push.
---
eg:
* git commit f**1**.c
* git commit -m"Modified f**1**.c, related to program ABC"
* git push

---

* git commit f**2**.c
* git commit -m"Modified f**2**.c, related to program XYZ"
* git push

Rest you get the idea.

[Source](http://stackoverflow.com/questions/6919121/why-are-there-2-ways-to-unstage-a-file-in-git)
