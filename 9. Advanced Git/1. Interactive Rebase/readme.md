_Interactive Rebase_
=

A tool to manipulate the commit history (optimizing and cleaning up)

- change a commit's msg
- delete commits
- reorder commits
- combine multiple commits
- split a commit into multiple new ones
- edit a commit

_NOTE_ : 

- don't use Interactive Rebase on commits that are already pushed in a remote repository

- use it to clean up the local commits before pushing them into the main branch

---
## _General Workflow_ :     

  
### **STEP 1** : _Determine the range of commits to be manipulated_   
If you have to go back to the nth commit from the base commit , give the following git command  
```  
# Displays a list of the last n commits on the current branch
git rebase -i HEAD~n
```   
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143466915-aaa8b531-c885-40cc-a2ed-85c2ecf373fe.png" width="600" title="branch">
</p> 


'Edit commit message' window opens in your default editor  

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143467206-c281bbc8-4874-4ca8-9be0-fca315fd4525.png" width="600" title="branch">
</p>
  
---
  
### **STEP 2** : _Determine the actions to be performed_  
Don't change commit data in this step, yet. Choose the action.

For instance, Replace `pick` with `reword` before each commit message you want to change.

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143467886-84fbc3e5-c103-48a6-9294-b44e57b4ddcb.png" width="600" title="branch">
</p>  
  
Now save and close the file.  
  
---

### **STEP 3** : _Perform the selected actions_ 
  
In each resulting commit file, type the new commit message, save the file, and close it.

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143468502-f082f05e-7e69-4718-842e-a4b76cf26ada.png" width="600" title="branch">
</p>  

Your changes will be reflected! 
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143468675-91134741-0ec8-4801-aa9b-9b728d0373d5.png" width="600" title="branch">
</p> 
  
---  

### **STEP 4** : _Push the changes to Github_ 

When you're ready to push your changes to GitHub, use the push --force command to force push over the old commit.

```
git push --force [branch name]
```
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143469284-aae806f3-7ee0-4f49-9522-88dca7a45123.png" width="600" title="branch">
</p>  

---

