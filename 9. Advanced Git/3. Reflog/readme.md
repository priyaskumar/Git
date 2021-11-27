_Reflog_
=
A journal that has every movement of the HEAD pointer movements

- Record updates applied to tips of branches and other commit references  
- Every time a branch tip is updated for any reason (by switching branches, pulling in new changes, rewriting history or simply by adding new commits), a new entry will be added to the reflog  

---
## _When do we use reflog ?_
- Recover deleted commits 
- Recover deleted branch

---
## _Recover deleted commit_

Lets say, I wanna recover the last 2 commits I accidentally deleted.

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143668739-96f73f76-d028-4da2-8801-e15125d87262.png" width="600" title="branch">
</p>

In order to see the reference logs, give the following command  
```
git reflog
```
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143668792-0415b374-05eb-49c8-85a2-d9d26587b26b.png" width="600" title="branch">
</p>  

Now, copy the hash-key of the state to which it is required to revert back to.

Use the following command
```
git reset --hard [hash_key]
```
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143668854-c7d3f595-086e-45a8-8d3b-809b09f941cf.png" width="600" title="branch">
</p>

The commits are recovered successfully.
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143668868-58702bdc-702c-4016-a673-4d6ca261c6f5.png" width="600" title="branch">
</p>

---

## _Recover deleted commit_

Lets say, I have to recover the deleted branch 'TempBranch'
<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143669017-8a6de285-6eab-4719-959a-d70f4e1dabc3.png" width="600" title="branch">
</p>

Use the command `git reflog` to get the log history.

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143669125-a82654a8-3fdf-46e8-9abe-de8eb51398fe.png" width="600" title="branch">
</p>

Copy the hash-key of checkout state.

Now, use the command 
```
git branch [deleted_branch_name] [haskey]
```

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143669114-90e82b23-286a-4cfe-abe8-d8675b5ea06f.png" width="600" title="branch">
</p>

Your branch is now recoverd successfully.


