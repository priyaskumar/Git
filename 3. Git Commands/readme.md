Git Commands
=== 

### **_config_**
Sets the author name and email address respectively to be used with your commits
```
git config –global user.name “[name]” 
git config –global user.email “[email address]”
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143033738-73f48ba3-2f28-4909-9037-ea69f7937355.png" width="600" title="pull">
</p>


### **_init_**
Intializes git in the current path
```
git init
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143033042-10a7d734-862c-47a2-b323-004bd97947ff.png" width="600" title="pull">
</p>


### **_clone_**
Bring a repository that is hosted somewhere like Github into a folder on local machine
```
git clone git@github.com:priyaskumar/Git-and-Github.git
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143028803-b573baef-897d-4b12-a436-9e387960713d.png" width="600" title="clone">
</p>


### **_add_**
Track changes in the file
```
git add [filename]
```
Track all files in Git.
```
git add .
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143034249-e7690d68-0af9-4a58-92c9-7e0f56955b78.png" width="600" title="clone">
</p>


### **_commit_**
Save changes/files in Git
```
git commit -m "Commit title" -m "some description"
```
Add and Save changes/files in Git
```
git commit -am "Commit title" -m "some description"
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143034711-5776a228-ab12-4aae-9361-e658142b7385.png" width="600" title="clone">
</p>

### **_remote_**
Connect local repository to the remote repository
```
git remote add [variable name] [Remote Repository Link]
```
Check if the connection to remote repository is enabled
```
git remote - v
```

### **_push_**
Upload all changes/files to the master branch of a remote repo (like Github, bitbucket, gitlab)
```
git push origin master
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143035089-894a04e2-74ad-4c9a-a022-45a272d09aa6.png" width="600" title="clone">
</p>


### **_pull_**
Dowload changes/files from a remote repo to local computer
```
git pull https://github.com/priyaskumar/Git-and-Github.git
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143029380-9d9a0d98-f734-40de-af09-c8f126c9139a.png" width="600" title="pull">
</p>

### **_log_**
List the version history for the current branch
```
git log  
```
<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143037908-8ca0c059-67e6-4898-b1a2-2eea1f7657d9.png" width="400" title="pull">
</p>

### **_status_**
List all the files that is to be committed
```
git status  
```
<p align="center">
  <img src="https://user-images.githubusercontent.com/94846381/143038287-ec6a1ab5-6109-4292-bb3d-15281cb42df6.png" width="600" title="pull">
</p>

### **_Delete last commit_**

Deleting the last commit is the easiest case. Translated to git terminology, when there's a need to force a branch of the origin remote repository to the parent of the last commit, use

```
git push origin +[commitkey]^:[branch_name]
```  
git interprets x^ as the parent of x and + as a forced non-fastforward push.



