## This is a private tutorial for github cli commands

============== From THE BEGINNING ==============

Install the git cli -> winget install --id GitHub.cli OR upgrade -> winget upgrade --id GitHub.cli

1. Authenticate the github cli with : `gh auth login`

    Use the https if you are going to perform all the operation using HTTPS url of repo
    Use the SSH if you are going to perform all the operation using ssh of repo


        ## Every repository has two types of modes to perform actions 
            1. HTTPS 2. SSH
            on Later step of adding remote repository, your choice will be needed...


    ONCE SET , IT CANNOT BE CHANGED WITHOUT RE-AUTHING IT.... 

2. create a repo from cli : `gh repo create <repo_name> --[flags]`
3. initialize the local directory with master branch : `git init -b master`
4. Add a remote repository : `git remote add origin git@github.com:<username>/<repo_name>.git`
    
    Here the git@... address is an SSH key, if you have chosen HTTPS then you command will look like

    `git remote add origin https://github.com/<username>/<repo_name>.git`

5. Add all the files : `git add .`
6. Commit the files : `git commit -m "<commit_message>"`
7. Push the files to origin : `git push -u origin master`

============== To create a new branch and push to that branch ==============

1. To create a new branch : `git branch <brnach_name>`
2. To switch to the branch : `git switch <branch_name>`
3. Add all the necessary files and then commit
4. to push to the new branch : `git push --set-upstream origin <branch_name>`
