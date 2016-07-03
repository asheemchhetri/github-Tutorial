<!--
==============================================================================
 @Author             : Asheem Chhetri <asheem>
 @Date               : Sunday, July 3rd 2016, 12:36:56 am
 @Email              : achhetri@purdue.edu
 @Project Name       :  
 @Last modified by   : asheem
 @Last modified time : Sunday, July 3rd 2016, 12:44:40 am
==============================================================================
-->

# Issue 2: Corrupt Loose Object

***

This issue happens, when we have a corrupt tree.

![error example](picture/issue2.png)

**Solution:** We have to re-clone the remote repository form the github, or if some one else has a non corrupted version, then the corrupted ones can be replaced but it is very unlikely.

---

**Commands:**

* rm -fr .git

* git init

* git remote add origin [your-git-remote-url]

* git fetch

* git reset --mixed origin/master

* git branch --set-upstream-to=origin/master master

[Source](http://stackoverflow.com/questions/4254389/git-corrupt-loose-object)
