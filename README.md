# Accedia git workshop intermediate

## Commands reference.
```
git clone <repository-URL-address>
git checkout -b <new-branch-name>
git add <filename>
git commit -m <commit-message>
git checkout <branch-name>
git merge <branch-name>
git push
git merge <branch-name>
git add <filename>
git commit -m <commit_message>
git push
```

```
git checkout <microsoft>
git rebase <branch-name>
git add <file-name>
git rebase --continue
git push --force
git checkout <branch-name>
git pul
```

```
git checkout <branch-name>
git rebase -i <branch-name>
```

## DAY 2, TASK 1:
- Open a browser of your choice and log into your github account. Navigate to https://github.com/Jessie365/accedia-git-workshop-intermediate/ and fork the **accedia-git-workshop-intermediate** repository.
- Clone the forked repo **accedia-git-workshop-intermediate** locally
- :warning: (Windows users only) To avoid entering your credentials every time you are executing remote commands, please issue the following command `git config --local credential.helper wincred`. Your credentials will be stored securely by the Windows Credential Manager.
- Create new branch and name it **change-quote**.
- Open **linus.txt** file and remove the last quote – the line starting with “Microsoft …”. Save the file.
- Commit the changes, use 'Remove last quote' for commit message.
- Merge the newly created branch **change-quote** into the **master** branch. To do that, you need to checkout **master** and then execute the merge command.
- Push the changes made on **master**. If you are using Windows, a pop-up should appear asking for your github account. Enter your credentials.
- Execute merge command to merge branch **microsoft** into the **master** branch. A message, saying that there are merge conflicts in the **linus.txt** file, should be displayed.
- Open **linus.txt** file and resolve the merge conflicts by accepting the changes made by both branches. You need to delete the extra lines starting with ```<<<<<<<```, ```=======``` and ```>>>>>>>```. Save and close the file.
- Complete the merge by staging the changes and committing them. Please name your commit 'Merge microsoft branch'.
- Push your changes.

Your log should look like that: 
![Task expected result](https://raw.githubusercontent.com/Jessie365/accedia-git-workshop-intermediate/images/images/image-task1-1.jpg)
<br />
The comparison between master and change-quote branches should look like:
![Task expected result](https://raw.githubusercontent.com/Jessie365/accedia-git-workshop-intermediate/images/images/image-task1-2.jpg)

## DAY 2, TASK 2:
- Checkout branch **microsoft** and execute rebase command to rebase the current branch on the **microsoft-software** branch. Again, message should appear, saying that there are merge conflicts in **linus.txt**.
- Open **linus.txt** file and resolve the merge conflicts by accepting the changes made by both branches. You need to delete the extra lines starting with ```<<<<<<<```, ```=======``` and ```>>>>>>>```. Save and close the file.
- Finish the rebase process by staging the changes and executing command to continue with the rebase.
- Push the changes made on the **microsoft** branch. You would need to include the force switch when executing the push command because we have changed the git history.
- Submit a pull request to merge **microsoft** branch to **microsoft-software** branch. To submit the pull request, you need to open your browser and navigate to [https://github.com/<github-account\>/accedia-git-workshop-intermediate/pulls] - replace '<github-account\>' with the name of your github account. Click on the 'New pull request' button and change the value of the first dropdown – `base fork: Jessie365/acedia-git-workshop-intermediate` to your own repo - `<github-account>/acedia-git-workshop-intermediate`. If you leave that option, you would end up submitting a pull request to the original repo, which we have forked, and this is not what we want here. Select **microsoft-software** for the base branch and set the compare branch to **microsoft**. Click on the 'Create pull request' button and then confirm the merge.
- Let’s imagine that someone from your team has reviewed your pull request and you are notified that it can be completed, because everything looks good. To complete the pull request, you need to click on the 'Merge pull request' button. If you have closed the browser window you can find that button here: [https://github.com/<github-account\>/accedia-git-workshop-intermediate/pull/1]
- After you have completed the pull request, checkout to **microsoft-software** branch and issue the pull command.

After pulling branch **microsoft-software**, your log should look like that:
![Task expected result](https://raw.githubusercontent.com/Jessie365/accedia-git-workshop-intermediate/images/images/image-task2-1.jpg)

DAY 2, TASK 3:
- Checkout branch **bugfix/extract-quotes** and execute command for interactive rebase on branch **feature/add-accedia-logo**. After executing the command, your default text editor would pop-up, listing 5 commits.
- You need to squash the trivial commits by changing the **'pick'** keyword to **'fixup'** (please read the description for **'fixup'** in the opened text editor). Do that for every commit that begins with 'Bugfix …'.
- Replace the **'pick'** keyword for the top commit in the list with **'reword'** to change the commit message. Save and close the file. New text file should be displayed containing the commit message that we want to change. Replace the commit message 'Add quotes text file' to 'Reworded commit message', save and close the file.
- After saving the last file, the interactive rebase should be completed.

Your log should look like: 
![Task expected result](https://raw.githubusercontent.com/Jessie365/accedia-git-workshop-intermediate/images/images/image-task3-1.jpg)
