_Sub Modules_
=

- Copy pasting third party code

- Mixing external code with your own files
- Updating the external code

Sub module is also a usual, fully - functional repository nested inside another apparent repository.

---

## _When to use submodules?_

- When an external component or subproject is changing too fast or upcoming changes will break the API, you can lock the code to a specific commit for your own safety.

-  When you are delegating a piece of the project to a third party and you want to integrate their work at a specific time or release. 

---

## _Add git submodule_
The git submodule add is used to add a new submodule to an existing repository. 
```
git submodule add [repo URL link]
```
---
## _Git submodule Init_
The default behavior of git submodule init is to copy the mapping from the .gitmodules file into the local ./.git/config file.
```
git submodule init
```

---
## _Submodule workflows_
- Once submodules are properly initialized and updated within a parent repository they can be utilized exactly like stand-alone repositories

- When making changes to a submodule it is important to publish submodule changes and then update the parent repositories reference to the submodule

 - So, make sure to always commit and push the submodule and parent repository.

