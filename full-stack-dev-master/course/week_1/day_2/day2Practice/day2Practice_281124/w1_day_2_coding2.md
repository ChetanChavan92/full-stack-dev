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



test@LAPTOP-LLCMMN9C:~/repos$ wget https://github.com/masai-school/assignments-data/raw/master/downloads/course.zip
--2024-11-26 13:35:23--  https://github.com/masai-school/assignments-data/raw/master/downloads/course.zip
Resolving github.com (github.com)... 20.207.73.82, 64:ff9b::14cf:4952
Connecting to github.com (github.com)|20.207.73.82|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://raw.githubusercontent.com/masai-school/assignments-data/master/downloads/course.zip [following]
--2024-11-26 13:35:24--  https://raw.githubusercontent.com/masai-school/assignments-data/master/downloads/course.zip
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.109.133, 185.199.110.133, 185.199.111.133, ...
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.109.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10164 (9.9K) [application/zip]
Saving to: ‘course.zip’

course.zip                             100%[============================================================================>]   9.93K  --.-KB/s    in 0s

2024-11-26 13:35:24 (26.7 MB/s) - ‘course.zip’ saved [10164/10164]

test@LAPTOP-LLCMMN9C:~/repos$ ls
course.zip  test
test@LAPTOP-LLCMMN9C:~/repos$ unzip course.zip
Archive:  course.zip
   creating: course/
   creating: course/week_2/
   creating: course/week_2/day_3/
 extracting: course/week_2/day_3/w3_d3_s2.txt
 extracting: course/week_2/day_3/w3_d3_s1.txt
   creating: course/week_2/day_5/
 extracting: course/week_2/day_5/w2_d5_s1.txt
 extracting: course/week_2/day_5/w2_d5_s2.txt
   creating: course/week_2/day_2/
 extracting: course/week_2/day_2/w2_d2_s1.txt
 extracting: course/week_2/day_2/w2_d2_s2.txt
   creating: course/week_2/day-4/
 extracting: course/week_2/day-4/w2_d4_s2.txt
 extracting: course/week_2/day-4/w2_d4_s1.txt
   creating: course/week_2/day_1/
 extracting: course/week_2/day_1/w2_d1_s1.txt
 extracting: course/week_2/day_1/w2_d1_s2.txt
   creating: course/all/
 extracting: course/all/w1_d1_s1.txt
 extracting: course/all/overall.txt
 extracting: course/all/w1_d1_s2.txt
 extracting: course/all/w2_d4_s2.txt
 extracting: course/all/w1_d3_s2.txt
 extracting: course/all/w2_d4_s1.txt
 extracting: course/all/w1_d3_s1.txt
 extracting: course/all/w1_d5_s1.txt
 extracting: course/all/w2_d2_s1.txt
 extracting: course/all/w1_d5_s2.txt
 extracting: course/all/w2_d2_s2.txt
 extracting: course/all/w1_d2_s1.txt
 extracting: course/all/w3_d3_s2.txt
 extracting: course/all/w2_d5_s1.txt
 extracting: course/all/w1_d2_s2.txt
 extracting: course/all/w3_d3_s1.txt
 extracting: course/all/w2_d5_s2.txt
 extracting: course/all/w2_d1_s1.txt
 extracting: course/all/w2_d1_s2.txt
 extracting: course/all/w1_d4_s2.txt
 extracting: course/all/w1_d4_s1.txt
   creating: course/week_1/
   creating: course/week_1/day_3/
 extracting: course/week_1/day_3/w1_d3_s2.txt
 extracting: course/week_1/day_3/w1_d3_s1.txt
   creating: course/week_1/day_4/
 extracting: course/week_1/day_4/w1_d4_s2.txt
 extracting: course/week_1/day_4/w1_d4_s1.txt
   creating: course/week_1/day_5/
 extracting: course/week_1/day_5/w1_d5_s1.txt
 extracting: course/week_1/day_5/w1_d5_s2.txt
   creating: course/week_1/day_2/
 extracting: course/week_1/day_2/w1_d2_s1.txt
 extracting: course/week_1/day_2/w1_d2_s2.txt
   creating: course/week_1/.day_6/
   creating: course/week_1/day_1/
 extracting: course/week_1/day_1/w1_d1_s1.txt
 extracting: course/week_1/day_1/w1_d1_s2.txt
 extracting: course/week_1/day_1/.w1_d1_sol.txt
test@LAPTOP-LLCMMN9C:~/repos$ ls
course  course.zip  test
test@LAPTOP-LLCMMN9C:~/repos$ ls
course  course.zip  test
test@LAPTOP-LLCMMN9C:~/repos$ cd course/
test@LAPTOP-LLCMMN9C:~/repos/course$ ls
all  week_1  week_2
test@LAPTOP-LLCMMN9C:~/repos/course$ cd all/
test@LAPTOP-LLCMMN9C:~/repos/course/all$ ls
overall.txt   w1_d1_s2.txt  w1_d2_s2.txt  w1_d3_s2.txt  w1_d4_s2.txt  w1_d5_s2.txt  w2_d1_s2.txt  w2_d2_s2.txt  w2_d4_s2.txt  w2_d5_s2.txt  w3_d3_s2.txt
w1_d1_s1.txt  w1_d2_s1.txt  w1_d3_s1.txt  w1_d4_s1.txt  w1_d5_s1.txt  w2_d1_s1.txt  w2_d2_s1.txt  w2_d4_s1.txt  w2_d5_s1.txt  w3_d3_s1.txt
test@LAPTOP-LLCMMN9C:~/repos/course/all$ git remote -v
origin  https://github.com/ChetanChavan92/test.git (fetch)
origin  https://github.com/ChetanChavan92/test.git (push)
test@LAPTOP-LLCMMN9C:~/repos/course/all$ git add overall.txt
test@LAPTOP-LLCMMN9C:~/repos/course/all$ git commit -m "first file"
[master 1b80e02] first file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 repos/course/all/overall.txt
test@LAPTOP-LLCMMN9C:~/repos/course/all$ git push
Username for 'https://github.com': ChetanChavan92
Password for 'https://ChetanChavan92@github.com':
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 435 bytes | 435.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ChetanChavan92/test.git
   8798007..1b80e02  master -> master
test@LAPTOP-LLCMMN9C:~/repos/course/all$



### FSD.W1.2.2_6

- Sync the folder `week_1` to the remote repo with the message "Week1 Course" (HINT: use the `git status` command to make sure only `week_1` folder is getting synced)
- Sync the folder `week2/day_5` to the remote repo with the message "W2 D5"
- Check if the online created file is now present in the `test` folder and see if the history of commits (HINT: use `git log`)




test@LAPTOP-LLCMMN9C:~/repos/course$ git remote -v
origin  https://github.com/ChetanChavan92/test.git (fetch)
origin  https://github.com/ChetanChavan92/test.git (push)
test@LAPTOP-LLCMMN9C:~/repos/course$ git add week_1
test@LAPTOP-LLCMMN9C:~/repos/course$ git commit -m "Week1 Course"
[master fdda114] Week1 Course
 11 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 repos/course/week_1/day_1/.w1_d1_sol.txt
 create mode 100644 repos/course/week_1/day_1/w1_d1_s1.txt
 create mode 100644 repos/course/week_1/day_1/w1_d1_s2.txt
 create mode 100644 repos/course/week_1/day_2/w1_d2_s1.txt
 create mode 100644 repos/course/week_1/day_2/w1_d2_s2.txt
 create mode 100644 repos/course/week_1/day_3/w1_d3_s1.txt
 create mode 100644 repos/course/week_1/day_3/w1_d3_s2.txt
 create mode 100644 repos/course/week_1/day_4/w1_d4_s1.txt
 create mode 100644 repos/course/week_1/day_4/w1_d4_s2.txt
 create mode 100644 repos/course/week_1/day_5/w1_d5_s1.txt
 create mode 100644 repos/course/week_1/day_5/w1_d5_s2.txt
test@LAPTOP-LLCMMN9C:~/repos/course$  git remote set-url origin https://github.com/ChetanChavan92/test.git
test@LAPTOP-LLCMMN9C:~/repos/course$ git push
Username for 'https://github.com': ChetanChavan92
Password for 'https://ChetanChavan92@github.com':
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 12 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (11/11), 804 bytes | 804.00 KiB/s, done.
Total 11 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ChetanChavan92/test.git
   1b80e02..fdda114  master -> master
test@LAPTOP-LLCMMN9C:~/repos/course$ ls
all  week_1  week_2
test@LAPTOP-LLCMMN9C:~/repos/course$ cd week_2
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ ls
day-4  day_1  day_2  day_3  day_5
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ cd ..
test@LAPTOP-LLCMMN9C:~/repos/course$ git add week2/day_5/
warning: could not open directory 'repos/course/week2/day_5/': No such file or directory
fatal: pathspec 'week2/day_5/' did not match any files
test@LAPTOP-LLCMMN9C:~/repos/course$ cd week_2
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ git add day_5
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ git commit -m "W2 D5"
[master a3d5755] W2 D5
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 repos/course/week_2/day_5/w2_d5_s1.txt
 create mode 100644 repos/course/week_2/day_5/w2_d5_s2.txt
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ git remote -v
origin  https://github.com/ChetanChavan92/test.git (fetch)
origin  https://github.com/ChetanChavan92/test.git (push)
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ git push
Username for 'https://github.com':  ChetanChavan92
Password for 'https:// ChetanChavan92@github.com':
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (7/7), 484 bytes | 242.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ChetanChavan92/test.git
   fdda114..a3d5755  master -> master
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$ git log
commit a3d57552ee7dc47d888a29397181f30fafe06f21 (HEAD -> master, origin/master)
Author: chetan <chetanchavan0300@gmail.com>
Date:   Thu Nov 28 23:25:55 2024 +0800

    W2 D5

commit fdda114fbf1c18721b36bf55d3b69c7822c5d86d
Author: chetan <chetanchavan0300@gmail.com>
Date:   Thu Nov 28 21:07:31 2024 +0800

    Week1 Course

commit 1b80e0279068cd303a9dad01b5b7937e321aa4f5
Author: chetan <chetanchavan0300@gmail.com>
Date:   Tue Nov 26 14:04:20 2024 +0800

    first file

commit 8798007dfffcf5a5eb153f8b7b0d496e7dad70de
Author: chetan <chetanchavan0300@gmail.com>
Date:   Mon Nov 25 00:45:09 2024 +0800

    commit

commit e9f736832fb95a7c2796d25221a3a450fb232ce7
Author: chetan <chetanchavan0300@gmail.com>
Date:   Sun Nov 24 19:11:01 2024 +0800

    commit
test@LAPTOP-LLCMMN9C:~/repos/course/week_2$



### FSD.W1.2.2_7

Create a new file called `complete` in the `test` folder and sync it to the online repo 


test@LAPTOP-LLCMMN9C:~/repos/course$ ls
all  week_1  week_2
test@LAPTOP-LLCMMN9C:~/repos/course$ echo "" >>complete
test@LAPTOP-LLCMMN9C:~/repos/course$ git add complete
test@LAPTOP-LLCMMN9C:~/repos/course$ git commit -m "file complete"
[master c3c3212] file complete
 1 file changed, 1 insertion(+)
 create mode 100644 repos/course/complete
test@LAPTOP-LLCMMN9C:~/repos/course$ ls
all  complete  week_1  week_2
test@LAPTOP-LLCMMN9C:~/repos/course$ git remote -v
origin  https://github.com/ChetanChavan92/test.git (fetch)
origin  https://github.com/ChetanChavan92/test.git (push)
test@LAPTOP-LLCMMN9C:~/repos/course$ git push
Username for 'https://github.com':  ChetanChavan92
Password for 'https:// ChetanChavan92@github.com':
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 424 bytes | 424.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ChetanChavan92/test.git
   a3d5755..c3c3212  master -> master
test@LAPTOP-LLCMMN9C:~/repos/course$


### FSD.W1.2.2_8

- Go to your home directory `cd ~`

- Navigate to the `repo` directory

- Clone the repo <https://github.com/masai-school/cohort_1> 

### FSD.W1.2.2_9

- There is folder called `attendance` inside the `cohort_1` repo
- Navigate to `attendance` folder
- Copy the `template.md` file with the name `firstname_lastname.md`
- Sync back the newly created file `firstname_lastname.md` to the remote repo