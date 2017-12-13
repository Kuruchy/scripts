# Useful Scripts
Usefull scripts to perform tasks

I will be adding scripts that somehow had helped me at some point with rutinary work.

| ID | Script Name | Use case |
| ---- |:----:|:----:|
| 1 | git-author-rewrite | Changes the username and mail from all commits in GIT |

# Usage Examples

Learn how to use the scripts by reading and understanding the proper section.

## 1.- Git-author-rewrite.sh
   
With this script you will change all the commits that were made and match the **OLD_EMAIL**. In case you want to change all of the commits, independent of the committer, see section Important after point 6.
  
   1. Replace the **OLD_EMAIL** with the old email you want to change.  
   2. Replace the **CORRECT_NAME** with the new name that will appear in all commits.  
   3. Replace the **CORRECT_EMAIL** with the new email that will appear in all commits.
   4. Put the file in the GIT project folder you want to change. 
   5. Change the permissiont to be able to execute it: `chmod +x git-author-rewrite.sh`
   6. Run it: `./git-author-rewrite.sh`
  
   #### Important

   If you want to change ALL the commits independent of the commited mail, you can also use `git filter-branch -f --env-filter "GIT_AUTHOR_NAME='Newname'; GIT_AUTHOR_EMAIL='new@email'; GIT_COMMITTER_NAME='Newname'; GIT_COMMITTER_EMAIL='new@email';" HEAD` instead of using **git-author-rewrite.sh** but be aware that this code will change all the users, even if you have a repo with more than one committer.
   
   Both scripts will rewrite the history of your entire GIT repository, therefore it will change all the SHA1 of your commits.  
   More Info: [Git Tools - Rewriting History](https://git-scm.com/book/en/v1/Git-Tools-Rewriting-History)
  
   7. Right now if you make a `git log  --graph --all --decorate --oneline` you will see that the commits are duplicated, the old ones remain, under an "original" folder, and the new ones are in the HEAD.
   
   8. If you want to get rid of the old commits just delete the original folder `rm -r .git/refs/original/`
   
## Meta

Bruno Retolaza

[https://github.com/Kuruchy](https://github.com/Kuruchy/)
