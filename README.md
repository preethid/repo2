# repo2
![k8s](https://github.com/user-attachments/assets/6efc21ee-0a7e-4653-9d5c-6596ab6d5d5e)


 ```
  chmod aws.pem 400
```
1.3.1 Git Branching, Merging, and Stashing

# Hands-On Lab: Git Branching, Merging, and Stashing 

This lab provides a detailed walkthrough of essental Git workfows like branching,merging, resolving conficts, and stashing. Each step is demonstrated using commands and examples to deepen understanding. 

## Lab Overview 

### In this lab, you will: 

1. Create and manage branches.

2. Perform merges with and without conficts.

3. Resolve merge conficts efectvely.

4. Use Git stash to save and restore uncommited changes.

## Step-by-Step Instructons 

## 1. Git Branching 

1. List all branches: 
```
 git branch
```
2. Create a new branch from master:
```
 git branch b1 master 
```
3. Switch to the new branch:
```
 git checkout b1
```
4. Verify the actve branch:

 git branch

5. Add and commit changes to the branch:

 vim index3.html

git add index3.html 

git commit -m "Added index3.html on b1"

## 2. Git Merging 

### Merge Without Conficts 

1. Switch to the master branch:

 git checkout master 

2. Merge the b1 branch into master: 

 git merge b1

3. Verify the merge:

 git log --oneline

### Merge with Conficts 

1. Create confictng changes on the master and b1 branches: 

 # On master: 

git checkout master 

vim index4.html 

git add index4.html 

git commit -m "Edited index4.html on master"

 # On b1:

git checkout b1 

vim index4.html 

git add index4.html 

git commit -m "Edited index4.html on b1"

## 2. Atempt to merge b1 into master:

 git merge b1

## 3. Resolve the confict by editng the afected fle(s):

 vim index4.html

4. Mark conficts as resolved:

 git add index4.html 

5. Commit the merge: 

 git commit -m "Resolved merge conficts"

6. Verify the merge result:

 git log --oneline

# 3. Git Stash 

## Save Changes to Stash

1. Edit fles: 

 vim index1.html vim index2.html 

2. Check the status: 

 git status 

3. Stash the changes: 

 git stash 

4. List stashed changes:

 git stash list 

## Restore Changes from Stash 

1. Apply the stash without removing it from the list:

 git stash apply stash@{0} 

## 2. Remove the stash and apply changes:

 git stash pop stash@{0} 

# 3. Verify the restored changes:

 git status 

# Partal stash

# 4. Stash a partcular fle 

 git stash -p

## Drop or Clear Stashes 

1. Drop a specifc stash:

 git stash drop stash@{0} 

2. Clear all stashes: 

 git stash clear 

## Key Commands Summary


| Command  | Descripton  |
| -- | -- |
| git branch  | List branches or create a new branch.  |
| git checkout &lt;branch&gt; | Switch to a branch.  |
| git merge &lt;branch&gt; | Merge a branch into the current branch.  |
| git stash  | Save uncommited changes to a stash.  |


git stash apply Apply changes from a stash.

git stash pop Apply changes and remove the stash.

git stash drop Remove a specifc stash.

git stash clear Clear all stashes.

By completng this lab, you have practced branching, merging, resolving conficts,and using stash for change management in Git. 

