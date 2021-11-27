Git Branching
===
**_Master_**      
A naming convention for main or default branch in the repository

**_Feature Branch_**    
- Code on master and new feature branch is same at first.   
- Updates made to feature branch reflected only in that feature branch and not on master.

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143050865-6d0fa818-0470-4510-a2d2-08d570ea4cf8.png" width="600" title="branch">
</p>

**_Branching is useful when_**  
    -> more than one people work on a same repository

  

**_Git commands for branching_**

Display all branches in the local repository
```
git branch
```

Create a new branch with given name
```
git checkout -b [branch_name]
```


Delete a specific branch
```
git branch -d [branch_name]
```


Go to a specific branch
```
git checkout [branch]
```


Show differences in the code after updation
```
git diff
```
  
Merging
===
Merge a feature branch back into the master branch in GitHub when changes in feature branch is approved

**_Git command for merging_**  

Merge the given branch to the main/master branch
```
git merge [branch_name]
```

Pull the merged master branch from the remote repository to the local machine  

```
git pull origin master
```

