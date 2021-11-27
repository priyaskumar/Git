Cherry-picking
===
We generally integrate all new commits from one branch into current head branch. At times, we might want only a specific commit to be integrated in head branch.

Cherry - pick allows to select individual commits to be integrated to the required branch.
  
_NOTE_ :  
- It's not a good practice to use cherry-picking as a substitution for merging and rebase.
- Use cherry-picking only in specific circumstances i.e. when there's an absolute purpose for it.  

---
## _When to use git cherry pick ?_    

- Git cherry-pick can be useful for undoing changes.
- For instance, say a commit is accidently made to the wrong branch. It can be switched to the correct branch by cherry-picking the commit to where it should belong.  
- **_Team collaboration_** :   
    * If a person working with a feature branch wants a commit belonging to another feature branch in his branch, he can cherry-pick the commit.
    * This lets the person to work on his branch side by side.
- **_Bug fixes_** :  
    * It is important to fix a bug when discoverd quickly, before reaching a large no. of users.
    * Lets say a person has started to work on a new feature. During that new feature development he identifies a pre-existing bug. 
    * He will create an explicit commit patching this bug. This new patch commit can be cherry-picked directly to the main branch to fix the bug before it effects more users. 
- **_Restoring lost commits_** :
    * Sometimes a pull request might get closed without merging. 
    * Git never loses those commits and through commands like git log and git reflog they can be found and cherry picked back to life.
---
## _How to use git cherry pick?_  

Consider this,

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143484722-46408647-6a30-4ebe-a21f-87edf20e3f6a.png" width="400" title="branch">
</p>   

For instance, lets say commit 'f' has to be cherry picked to main branch too. The following commands are given to do it right.

1. Go to the main branch   
      ```  
      git checkout main  
      ```   
      Now, you're at the main branch.  
  
2. Cherry pick the required commit  
      ```  
      git cherry-pick f       // commit key is provided instead of f  
      ```  


<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143485420-0fac57ef-fa6a-4392-8f3a-ade0c8cbe472.png" width="400" title="branch">
</p> 
   
   The commit 'f' has been successfully picked into the main branch.


