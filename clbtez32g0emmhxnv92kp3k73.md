# Git And GitHub Basics

Imagine that you have a project and you want to collaborate with other people or you have your own application and it works correctly and then you modify it or add a new feature then it breaks or work improperly.

**Git** is here to solve all that, you can build one application with many people without copying and paste of code, however, you can also have the history of your project saved on the git repository/repo whereby you can return to back codebase  where your application was working correctly if it breaks after adding a new feature

### **Basic CLI Commands To Know When Using Git**

1.  To list all files or folders in a folder
    
    `ls`
    
2.  Make a new folder
    
    `mkdir folder_name`
    
3.  Go inside a folder
    
    `cd folder_name`
    
4.  To delete a whole non-empty directory/folder
    
    `rm directory_name -rf`
    
5.  Copy + Paste in CLI
    
    1.  Ctrl + Insert to copy
        
    2.  Shisft + Insert to paste
        
    3.  Or Highlight and right-click to see options
        

### **Basic Git Commands**

1.  To check if git is installed in your PC
    
    `git`
    
2.  To make a history of a project you are working with, you need to initialize an empty repository. This will provide a repository(folder) to store your history of the project to see which files were added/deleted/modified and when was changes made to a project.
    
    To initialize an empty Git repository in your folder
    
    `git init`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671363273655/K9gg0RyNx.PNG align="center")
    
3.  To see what is inside git folder
    
    `ls .git`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671363210199/cbi9LVv5D.PNG align="center")
    
4.  Now we are able to maintain every change in this folder so we can add new file inside project1 folder with this command `touch name.txt`
    
    To view the changes or the untracked files in the project that's not been saved yet git status
    
    `git status`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671363881820/92-q_HO_G.PNG align="center")
    
    **N.B.** After adding a file to your folder no one will be able to see that you have added a file write now meaning this change has not yet maintain in git repository
    
5.  To place the files that are untracked to the stage whereby they are now ready to be stored in history (Staging the files)
    
    `git add file_name` or `git add .` (to stage everything in the current folder)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671364351466/vdxzl2mI1.PNG align="center")
    
    Now the files will be on a staging area and will be now written in green color while they were written in red color before being added to the staging area. To check them run this command again `git status`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671364581896/hAzuNvgSZ.PNG align="center")
    
6.  To save changes we made to our project we need to commit this file and provide a message
    
    `git commit -m "Provide a message"`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671364935783/hXx5ggN-D.PNG align="center")
    
    The above picture shows that there is 1 file added/change with 0 insertions and 0 deletions hence we haven't added anything to this file
    
7.  To view the entire history of the project as we added the file to project1 folder
    
    `git log`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671365722148/vjgrLtnVC.PNG align="center")
    
    This will show the name of the person who made changes, when changes were made and the massage provided when committing
    

*Now lets edit this file by just adding two lines in it and see what changes it will give us*

8.  To write in a file using git bash
    
    `vim file-name`
    
    After this command click the **insert** button to enable writing and after writing click **escape** button to unable writing then write `:x` to go back
    
9.  To see what is there inside a file we just added 2 lines
    
    `cat filename`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671366639316/4wrqOWFk7.PNG align="center")
    
    To save these changes again follow the steps above which are `git add .` and commit changes with `git commit -m "provide message"`
    
    After committing you can see the history of a project again with `git log` to see how many commit you have and when you committed
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671367315179/Mea-FDcfn.PNG align="center")
    
10.  To unstage or remove a file from the staging level
    
    `git restore --stage filename`
    
    You can use this command if you make changes to a file and then you staged it by mistake/ not yet ready to be committed, the file will return to unstaging area and won't be committed.
    
11.  To remove history/commit you made on project folders
    
    `git reset insert_commit_hash_id_to_which_you_want_to_go_back_to_here`
    
    **N.B.** *All the commits or changes before this will go back to the unstaged area now you can’t remove the middle commit and leave the above one hence each commit has an interlink hash id which is connected to each other*
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671368167460/_1cJKHxvM.PNG align="center")
    
    Now are back to where name.txt was not modified that is why when we log history again we no longer have *the "name modified"* commit
    
    **N.B.** The changes that you modified are not deleted, they are back on unstaged area, this means that you can commit them again, check them `git status`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671368589778/jhSiuxZlw.PNG align="center")
    
12.  After you stage a few files but then you want to have a clean codebase or reuse those files later, we can stash those changes to go back to the commit before they were staged
    
    `git stash`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671369123586/eM17VxQIW.png align="center")
    
    You will be now working on the clean tree whereby no changes to commit but those changes are not deleted permanently, but are saved somewhere else
    
13.  To bring back those changes or pop them from the stash
    
    `git stash pop`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671369498784/IYyPpG61I.PNG align="center")
    
    Now they are back you can commit them again
    
14.  To clear the changes or files in your stash (Now they will be permanently deleted you won't get them back again )
    
    `git stash clear`
    

**The next article will be how git works with GitHub hope you enyoyed it.**