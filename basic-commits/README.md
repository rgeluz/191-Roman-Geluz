# Git Kata: Basic Commits
This kata will introduce you to the `git add` and `git commit` commands.

This is a very introductory kata. if you have used `git status`, `git log --oneline --graph`, `git add` and `git commit` extensively you should probably skip it.

You can look at the bottom of this file, if you have not yet done basic git configuration.

## Setup:

1. Run `. setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

1. Use `git status` to see which branch you are on.
2. What does `git log` look like?

commit f8712d5c4df74fa0d49c8cc9ba3b1a5b2c571072
Author: Frank Theile <ftheile@grundfos.com>
Date:   Mon Dec 9 10:30:13 2019 +0100

    Add missing shebang in squashing/setup.sh

    `setup.sh` should be executable according to the instructions given in README.md

commit e060df632bf4799da9aa1c0092640563acf84588
Author: Adam Matan <adamatan@users.noreply.github.com>
Date:   Wed Dec 4 07:46:31 2019 +0200

    Word ordering

commit 6ccb85882dc12fb0b26acd65bead2fc7da57a187
Author: Frank Theile <ftheile@grundfos.com>
Date:   Wed Nov 27 08:24:29 2019 +0100

    Mention `less` in SHELL-BASICS.md


3. Create a file
4. What does the output from `git status` look like now?
5. `add` the file to the staging area
6. How does `git status` look now?


git status
On branch greeting
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   ../3-way-merge/README.md
	modified:   ../images/quickstart.gif

no changes added to commit (use "git add" and/or "git commit -a")


7. `commit` the file to the repository
8. How does `git status` look now?

git status
On branch greeting
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   ../3-way-merge/README.md
	modified:   ../images/quickstart.gif

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	newfile.txt

no changes added to commit (use "git add" and/or "git commit -a")


9. Change the content of the file you created earlier
10. What does `git status` look like now?

git status
On branch greeting
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   newfile.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   ../3-way-merge/README.md
	modified:   ../images/quickstart.gif

11. `add` the file change
12. What does `git status` look like now?
@geluzfamily  git status
On branch greeting
Changes to be committed:
(use "git reset HEAD <file>..." to unstage)

modified:   newfile.txt

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

modified:   ../3-way-merge/README.md
modified:   ../images/quickstart.gif
13. Change the file again
14. Make a `commit`
15. What does the `status` look like now? The `log`?

sion/Disussion_01242020_virtual/Activity1_GitGithubPractice/git-katas/basic-commits   greeting 2●1± ⚑ 
commit 1e7095c55c7119afb234663933e79ea03dfc130a
Author: Roman <rgeluz22@yahoo.com>
Date:   Fri Jan 24 18:36:19 2020 -0800

    added text to newfile.xt

commit 5a0f023172bfe74049f8ea0ee3b07a65678876ee
Author: Roman <rgeluz22@yahoo.com>
Date:   Fri Jan 24 18:34:30 2020 -0800

    added newfile.txt

commit f8712d5c4df74fa0d49c8cc9ba3b1a5b2c571072
Author: Frank Theile <ftheile@grundfos.com>
Date:   Mon Dec 9 10:30:13 2019 +0100

    Add missing shebang in squashing/setup.sh

    `setup.sh` should be executable according to the instructions given in README.md

:

16. Commit the newest change

## Useful commands
- `git add`
- `git commit`
- `git commit -m "My commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` to create a file (or `sc filename ''` in PowerShell)
- `echo content > file` to overwrite file with content (or `sc filename 'content'` in PowerShell)
- `echo content >> file` to append file with content (or `ac filename 'content'` in PowerShell)


## Git Initial Configuration
1. `git config --global user.name "John Doe"`
1. `git config --global user.email "johndoe@example.com`

For the vim scared:
- `git config --global core.editor nano`

For the windows peeps:
- `git config --global core.editor notepad`

Other editor options:
- `git config --global core.editor "atom --wait"`
- `git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst"`
