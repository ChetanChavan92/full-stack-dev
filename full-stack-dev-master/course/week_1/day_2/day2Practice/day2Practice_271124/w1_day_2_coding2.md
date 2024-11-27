# Week 1 - Day 2

#### Coding Session 2

**Introduction to git (Part 2)**

**NOTE:** Follow the instructions carefully and follow coding discipline

### FSD.W1.2.2_1

- Go to your home directory `cd ~` and create a folder called `repos`
- Create a folder called `test` inside `repos` folder
- Navigate to `test` folder
- Initialise `test` folder with an empty repository  


test@LAPTOP-LLCMMN9C:~$ mkdir repos
test@LAPTOP-LLCMMN9C:~$ cd r
repos/ rk/
test@LAPTOP-LLCMMN9C:~$ cd repos/
test@LAPTOP-LLCMMN9C:~/repos$ mkdir test
test@LAPTOP-LLCMMN9C:~/repos$ cd test/
test@LAPTOP-LLCMMN9C:~/repos/test$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/test/repos/test/.git/
test@LAPTOP-LLCMMN9C:~/repos/test$



### FSD.W1.2.2_2

- Create a file called `start`  inside `test` folder with the current `date` (HINT:  `date > start`)
- Add the file `start` to `git` (HINT: use `git add` command)
- Check the status of the `start` file using `git status` command
- Commit the changes to `git` with the message "Start Time" (HINT: use `git commit` command)



test@LAPTOP-LLCMMN9C:~/repos/test$ date > start
test@LAPTOP-LLCMMN9C:~/repos/test$ ls
start
test@LAPTOP-LLCMMN9C:~/repos/test$ git add start
test@LAPTOP-LLCMMN9C:~/repos/test$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   start

test@LAPTOP-LLCMMN9C:~/repos/test$ git commit -m "start time"
[master (root-commit) eb607f4] start time
 1 file changed, 1 insertion(+)
 create mode 100644 start
test@LAPTOP-LLCMMN9C:~/repos/test$ git status
On branch master
nothing to commit, working tree clean
test@LAPTOP-LLCMMN9C:~/repos/test$ ls
start
test@LAPTOP-LLCMMN9C:~/repos/test$




### FSD.W1.2.2_3

- Go to http://github.com and create a new repository called `test` (**NOTE**: Don't tick the option Initialize this repository with a README)
- Add the newly created repository as remote to git repo in `test` folder (HINT: use `git remote` command)
- Sync the local commit to the remote repo (HINT: use `git push` command)
- Go to the repo page on http://github.com and see if you can see the start file in the repository


test@LAPTOP-LLCMMN9C:~/repos/test$ ls
start
test@LAPTOP-LLCMMN9C:~/repos/test$ git remote add origin https://github.com/your-username/test.git
test@LAPTOP-LLCMMN9C:~/repos/test$ ls
start
test@LAPTOP-LLCMMN9C:~/repos/test$ git remote add origin https://github.com/ChetanChavan92/test.git
error: remote origin already exists.
test@LAPTOP-LLCMMN9C:~/repos/test$ git push -u origin master
Username for 'https://github.com': ChetanChavan92
Password for 'https://ChetanChavan92@github.com':
remote: Repository not found.
fatal: repository 'https://github.com/your-username/test.git/' not found
test@LAPTOP-LLCMMN9C:~/repos/test$ ls
start
test@LAPTOP-LLCMMN9C:~/repos/test$



### FSD.W1.2.2_4

Create a new file in the repo page with the name `profile.md` put your name as the contents of the file and commit the new file with the message "Online Commit"







### FSD.W1.2.2_5

- Download and unzip the file https://github.com/masai-school/assignments-data/raw/master/downloads/course.zip in the `test` repo folder (TIP : use`wget` and `unzip`)
- After unzipping you should in the `all` folder there is a file called `overall.txt` sync that file to the remote repo with the message "First File" (TIP: use the flow `add` `commit` `push`)

### FSD.W1.2.2_6

- Sync the folder `week_1` to the remote repo with the message "Week1 Course" (HINT: use the `git status` command to make sure only `week_1` folder is getting synced)
- Sync the folder `week2/day_5` to the remote repo with the message "W2 D5"
- Check if the online created file is now present in the `test` folder and see if the history of commits (HINT: use `git log`)

### FSD.W1.2.2_7

Create a new file called `complete` in the `test` folder and sync it to the online repo 

### FSD.W1.2.2_8

- Go to your home directory `cd ~`

- Navigate to the `repo` directory

- Clone the repo <https://github.com/masai-school/cohort_1> 

### FSD.W1.2.2_9

- There is folder called `attendance` inside the `cohort_1` repo
- Navigate to `attendance` folder
- Copy the `template.md` file with the name `firstname_lastname.md`
- Sync back the newly created file `firstname_lastname.md` to the remote repo