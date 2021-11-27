Undoing in git / Reset
===

In order to resolve the merge conflicts, we try to go back in time i.e, go a step backward and remove unnecessary commits.
  

**_Git command to reset_**  
  

Reset all the changes in file that has been tracked but not yet committed
```
git reset [filename]
```  
  
Reset all the files that have been modified
```
git reset 
```  
  
Undo the last commit  
(Note : HEAD is a pointer pointing to the last commit. On this command, HEAD is set to HEAD-1)
```
git reset HEAD~1
```  
  
  
Reset to the commit specified and delete all subsequent commits 
```
git reset --hard [hash_key]
```
hash_key - each commit has unique hash-key; it is provided in the first line of every commit in git log  
  

  

