CONFIGURING REMOTE SERVERS ON VMWARE OR VIRTUALBOX

VMWARE
sudo apt update && sudo apt install open-vm-tools-desktop       .... ON YOUR TERMINAL
sudo reboot & shut down the server 

 VM > Settings > Options tab > Enabled > Guest Isolation (Check the copy/Paste and Drag/Drop))

IF SSH IS NOT WORKING 
sudo apt-get remove --purge openssh-server
sudo apt-get update
sudo apt-get install openssh-server
VIRTUALBOX


Step 1:    Install git and check if it is properly installed ........ git --version
step 2:    configure git with vsc to set up your identity for commits  
< git config --global user.name "Your Name" >
< git config --global user.email "your.email@example.com" >
< git config --global core.editor code        # use VS Code as editor > ex: .....      code . 
< git config --global init.defaultBranch main # new repos start with “main” >
< git config --list >

step 3:     cd /path/to/project
git clone an existing repo  

step 4: create a new feature branch 

step 4:    Setup host/local computer to ESTABLISHING A CONNECTION TO THE GITHUB REMOTE SERVER​
Sign into your github/gitlab account and Click your profile photo → Settings → SSH and GPG keys. Click New SSH key (or Add SSH key).
Give it a Title (e.g. “host computer por distro name if using linux servers”) and paste the public‑key text into the “Key” box.
 ssh-keygen ​    .... on your terminal
 cd .ssh​
 cat id_rsa.pub​ 
Copy the public keys and paste on the github – setting – SSH and click on "add new key"​
Paste and save 
Click Add SSH key and if prompted, enter your GitHub password. 

Step 6:   ssh -T git@github.com      .... Trys to connect      ....... Optional

DEFINING BRANCHING RULE 

git commands 
git status ----- Views the status of your changes in your local working directory.​

  git log ---- Shows commit history​

  git show <commitID> ---- gets the commits using git commit log​

  git   log –oneline ----  shows all the activities in one line​

  git ls-files -----  Shows all files in your working directory​

  git diff ----   Shows any changes between commits and branches​

  git diff –staged ----  shows the difference between files​

Stashing changes of files  ​

gggit reset HEAD <filename>​

    git stash ---- save temporary files that are not for commit​

     git stash apply ---- applies the most current stash​

Deleting files and Branches ​

  git rm <filename>  ----  Removes files from local working Directory only​

  git rm --cached <d <fileName> ---- Removes from local repo ONLY​

  git branch –d  <branch-name> or git branch –-delete <branch-name> ----Deletes a branch name​

  git  branch –D <remote-branch-name>   ---- Deletes a remote branch​

  git branch –M main/master     -------    Switches from main branch to master branch and vice versa​


Daily task command 
git checkout -b <featureBranchName>
git status 
git add fileName(s)
git commit -m "message"
git push -u origin <featureBranchName>  ..... do this only once in the repo 
git push  ......... going forward until you are no longer working with the repo
