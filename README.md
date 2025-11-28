Git basic commands
1.	$ git -v -> To check the version of git 
2.	$ git config -> To set and manage git setting such as your username, email, default editor and other preferences, these setting apply globally (for all projects) & locally (for one project).
    $ Git config user.name “Payalchouhan”
    $ Git config user.email “payalchouhan89@gmail.com”
    $ git config --list -> To show all the Git settings that are currently applied on your system.

Create repository on git or commit message - 
1.  $ ls –l -> check file in directory
2.  $ git init –> this command is used to crete a repository and whenever you do git init the default branch that will git created master branch “
    $ git init –initial branch = main –> to create specific branch
3.  $ ls –al -> To check all files in directory 
4.  $ git status –> to check the current state of your working file in directory 

     Ways of git status command –
•	$ git status –v ->verbose mode it show detaile information of what change were made inside the file 
•	$ git status –s -> Shows a short, clean, compact summary of file changes.
 
    Warning  of git status is – 
•	 Red -> your file is not tracked by git is in non-staging area so add this file .
•	 Green-> your file is in staging area .
    “by default your file is in non staging area “
6. $ git add -> git add is used to move your changed files into the staging area, so they are ready to be committed. 
	 $ git  add file_name -> individual add file one by one by file_name .
	 $ git add . -> all file are added .
	 $ rm --cached file1_name file2_name -> To undo of git staging area to non staging area .
 
6. $ git commit ->it use to save your staged changes permanently in the repository with a message.  
	 $ git commit -m "Your message here" -> Create a commit with a message. To save changes with a clear message — without opening the editor.
	 $ git commit –a –m “your message hear” ->Commit all modified (already-tracked) files automatically. To avoid running  git add every time.
	 $ git commit --amend -> To use modified your last commit instead of creating a new one. It is used when to fix a wrong commit message , to add a file you forgot , to update or improve the previous commit . 
	 $ git commit --amend--no-edit -> Fix or update your last commit. Use when wrote wrong commit message , forgot files , want to improve the last commit.
	   git commit --amend --no-edit ->Update the last commit but keep the same message .
	 $ git commit -s -m “commit message” -> Add a Signed-off-by line to the commit.
	 $ git commit --allow-empty –m “dummy msg” ->Create a commit even when there are zero changes.
7. $ git log -> git log is used to see the history of all commits in your project.
	 $ git log –n <number> -> Shows only the last given number of commits.
	 $ git log –p -> Shows commits with patch means actual code changes (seen what line you changed and removed).
	 $ git log --pretty=short ->Shows commits in short format header or short message .
	 $ git log --pretty=full ->Shows- Author name + email , Committer name + email, Full commit message.
	 $ git log --pretty=fuller ->Shows even more detail author date or commiter date .
	 $ git log --pretty=oneline -> Shows each commit in one single line.
	 $ git log --pretty=format:”%h” ->Shows only short hash of each commit.
	 $ git log --pretty=format:”%h %S” -> show short hash or commit message .
	 $ git log --pretty=format:”%h %s %an” -> show short hash , commit message or author name .
	 $ git log –pretty=format:”%h % s % ae” -> show short hash , commit message , author name or  author email.
	 $ git log --since=”1 week ago ” ->This command shows only the commits made in the last 1 week.
	 $ git log –since=”2024-04-05” –until=”2025-11-25”
	 $ git log --author=”muskan”
	 $ git log --grap=”modified”

Reset or revert your commit 
Reset -> git reset is used to move your HEAD and branch pointer backward to commit.            
It do unstaged the file/changes , undo the commits , discard commit.

Three modes of git reset -
	$ git reset --soft Head_1 -> staged to commits
	$ git reset --mixed head_2 -> non staged to commit 
	$ git reset --hard head_3 -> delete the commit completely.
     Revert -> create a new commit that undoes a previous commit . when use revert it is safe not delete history old commits stays , a new commit is added .” $ git revert head_value”

Git diff command –
    Git diff is used to compare difference between files , branches , commits . it showa what lines were added or removed . 
	$ git diff --staged -> Shows staged changes . use before git commit , to confirm what will include .
	$ git diff <file> -> Shows diff for one specific file.
	$ git diff –name-only -> show only file name that changes  not content 
	$ git diff commit1 commit2 -> compare two commit.

Git branches –
	$ git checkout file_name -> to switch last commit with hash value  , to swith last branch like master – main  . 
	$ git branch -> to show the existing branch , it is give you information of local branch .
	$ git branch branch_name -> to create new branch 
	$ git branch –d branch_name -> to use for delete the branch 
	$ git switch branch_name ->by the use of this command we go to another branch
	$git merge branch_name -> it use to combine the changes from one branch to another branch .# hotwax1
