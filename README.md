# GitHub Tutorial

_by Danny Wu_

---
## Git vs. GitHub
* **Github** is _-insert what github is in a nutshell-_
  * The code is stored in the cloud up high above.
  * It tracks any changes made and organizes it.
  * It allows for collaboration on files.
  * **IT REQUIRES GIT**
* **Git** is _-insert what git is in a nutshell-_
  * _insert some functions of git_ 
  * **IT DOESN'T REQUIRE GITHUB**

---
## Initial Setup
**needs some images, specifically for the settings tab and ssh key ex**
- In order to start using github to organize your stuff, you'll need a github account  
  1) Go over to <https://github.com/>
  2) Look around for the huge "sign up" tab in the center-right of the screen or the top right.
  3) Make your account and sign into it.
- Now that you have your account for github, you'll have to set-up a SSH key.
  1) On the top right next to the 'PLUS (+)' is your profile icon. Click that.
  2) It should bring out a list, you'll want to click the settings.
  3) Then on the left, click the tab that is called "SSH and GPG keys"
  4) Now you'll want to make a **NEW SSH KEY** not a GPG key.
     * It should have two empty boxes labelled title and key. Title it whatever makes most sense to you.
     * For the key, you'll need to head on over to <https://c9.io/>. You should have an account already and if not, make one.
       1) Now that you're on c9.io, find the gear icon on the top right and click that.
       2) You should be at a page that shows your account settings, find the one that is called **SSH Keys** and click that.
       3) There should be two large blocks of text, *(the text is like a password but it's so random no one would be able to figure it out)*, copy the entire block under the tab called "Connect to your private git repository".
  4) Now that you have the SSH key to connect github and c9, go back to github and dump that key into the box labelled "key".
  5) Finally, add the new SSH key. Bam, you're done setting up the connection between c9 and github!
  6) But wait, you need to authenticate your SSH key so you'll need to head into your c9 IDE (*Internal Development Environment*) and then enter this `ssh -T git@github.com`.
     * To make sure you got this right, you should see `Hi <your username>! You've successfully authenticated, but GitHub does not provide shell access._` in your command box (usually on the bottom tab called bash - "insert your username")

---
## Repository Setup
- 


---
## Workflow & Commands



---
## Rolling Back Changes