# scripts
> Usefull scripts to perform tasks

I will be adding scripts that somehow had helped me at some point with rutinary work.

| ID | Script Name | Use case |
| ---- |:----:|:----:|
| 1 | git-author-rewrite | Changes the username and mail from all commits in GIT |

## Usage example

1. git-author-rewrite:

   Replace the **OLD_EMAIL** with the old email you want to change.  
   Replace the **CORRECT_NAME** with the new name that will appear in all commits.  
   Replace the **CORRECT_EMAIL** with the new email that will appear in all commits.

Put the file in the GIT project folder you want to change and run: `./git-author-rewrite.sh`
You can also use `git filter-branch -f --env-filter "GIT_AUTHOR_NAME='Newname'; GIT_AUTHOR_EMAIL='new@email'; GIT_COMMITTER_NAME='Newname'; GIT_COMMITTER_EMAIL='new@email';" HEAD` but be aware that this code will change all the users, even if you have a repo with more than one committer.


## Important

1. git-author-rewrite:

   This script will rewrite the history of your entire GIT repository, therefore it will change all the SHA1 of your commits.  
   More Info: [Git Tools - Rewriting History](https://git-scm.com/book/en/v1/Git-Tools-Rewriting-History)
   
## Meta

Bruno Retolaza

[https://github.com/Kuruchy](https://github.com/Kuruchy/)
