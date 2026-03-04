Step 1:    Install git and check if it is properly installed ........ git --version
step 2:    configure git with vsc to set up your identity for commits  
< git config --global user.name "Your Name" >
< git config --global user.email "your.email@example.com" >
< git config --global core.editor code        # use VS Code as editor >
< git config --global init.defaultBranch main # new repos start with “main” >
step 3:     cd /path/to/project
git init            # or clone an existing repo
code .  
step 4:    Setup host/local computer to ssh with your remote server
< ssh-keygen -t ............... This adds to GitHub/GitLab if you want to  push over SSH > and accept all the fault settings
< ~/.ssh/id_of_the_key.pub >
< cat ~/.ssh/id_of_the_key.pub  >  ...... and copy the whole line
Step 5:    Sign into your github/gitlab account and Click your profile photo → Settings → SSH and GPG keys. Click New SSH key (or Add SSH key).
Give it a Title (e.g. “host computer por distro name if using linux servers”) and paste the public‑key text into the “Key” box.
Click Add SSH key and if prompted, enter your GitHub password. 
Step 6:   ssh -T git@github.com      .... Trys to connect


