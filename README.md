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

* After you have set up your SSH keys and everything else, you'll want to have a directory or a place where you want to tinker around.
   1) First things first, make your directory and in the command box labelled "bash - your username", type in `git init`.
      * What `git init` does will initialize your directory and turn it into a local repository. You'll know when you see (master) right next to the directory name you're in. Ex: `/workspace/insert-directory (master) $`.
* Now that you have made your local repository, you're free to tinker and code as you like.
  1) If you're satisfied with whatever changes or files you made, you need to add them to the staging area. Do this by typing in `git add` in the command box. Keep this in mind, there are different types commands to add, `git add filename`, `git add .`, and `git add --all`.
     * `git add filename` will add the file you specified with changes made and only that file to the stage.
     * `git add .` will add all current files within the directory that has changes to them to the stage
     * `git add --all` will add all files with changes in them, including deleted files, to the stage.
  2) After you've added your changes to the staging area, you can commit them. Whenever you commit, it's necessary to add a message of what you've done in between your previous and current commit. If it's the first commit, add a message of what you've done so far. Do this by entering `git commit -m "insert message"` into the command box.
  3) Alright! You have your commit now, but what do you do? You need to send it off to a remote repository using `git push`.
     1) Head on over back to the github website and find the PLUS (+) symbol to the left of your profile icon on the top right.
     2) Click it and then a list should appear, click the one that says "New repository".
     3) Name the new repository the **EXACT SAME** as your directory name.
        * If you don't, the next steps will not work for you. _So make sure you have it the exact same!_
     4) Leave everything as is unless you know what you're doing or you've been instructed to change it and create the new repository.
     5) You'll be brought to a new tab where it explains to you what you should to in order to push to this repository on github, **MAKE SURE YOU HAVE THE SSH SELECTED!!**
        * After you select SSH (if you haven't done so already), find the strips of code underneath "…or push an existing repository from the command line" since we've made the local repository earlier.
           1)  You'll want to copy the first strip that is `git remote add origin git@github.com:your-username/repo-name.git` and paste it into your c9 command box. What this does is creates a connection between your local repository which is the one in c9 to the one you made on github which is the remote repository.
           2) Now'll you'll want to copy the second strip of code underneath the first one which is `git push -u origin master`. What this will does is it make the remote repository you've connected to the default repository for commits to be pushed into and only for that directory.
     6) Excellent, you have your connection between the local and remote repository now! You'll want to push your commits so that it stays in the remote for your future use or anyone else to use. Type in `git push` in bash and note, **it will only push COMMITS.** You won't need to specify where you want to push it to every single time because of you already set a default repository to push everything to.
     7) If you want to check your connection, you type in `git remote -v`. 

---
## Workflow & Commands
  * Usually, after setting up your local and remote repository AND the connection between both, you're free to do whatever you want for your code now. There are, however, some habits you should pick up for whenever you begin coding.
  1) The first habit and the most necessary is to use `git status` almost every single time you enter your local repository and whenever you make some changes. What `git status` does is that it shows you if changes has been made to a file and if it has to be staged first. If it needs to be sent to the stage, the text should appear in red as "modified: insert-filename.md". If not, you should appear as green


---
## Rolling Back Changes