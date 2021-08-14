# Demo
Some description
## Subheader
Watch tutorial on Youtube

1. Add a file to cloned folder
2. check the git status
3. local files in the cloned folder will show up as untracked files
4. Use git add to start tracking these files
5. by default period(.) is used to indicate all files in the local repo copy 
6. git add .
7. This will stage the files in to git ==> git will start tracking these files
8. you can also use to put individual file names to track/stage(ready to commit)
9. git add my-work.md
10. git status, will show the untracked files as "changes to be committed"
11. git commit -m "my commit message for the file" -m "message for description box"
12. git commit => readies the file in local repo, but go live or to remote repo, you need to push it
13. git push 
14. for push to work, you need to connect your local repo to the remote repo, using ssh keys or personal access tokens
    15. ssh key generated. goto your home directory.
    16. ssh-keygen -t rsa -b 4096  -C "skguruprasad@gmail.com"
    17. give name as gp-git-key
    18. Your identification has been saved in gp-git-key
    Your public key has been saved in gp-git-key.pub
    The key fingerprint is:
    SHA256:KRt4cPQtp+3dPFEN82RxfIj5NSbzyuJIppOexEgloek skguruprasad@gmail.com
    19. $ ls | grep gp-git-key
    gp-git-key
    gp-git-key.pub
    20. gp-git-key ==> private key
    gp-git-key.pub ==> public key, it is to be uploaded to the github account. Public key is ok to be shared.
    21. copy the public key
    cat gp-git-key-pub
    removed reference to pub
    22. goto github repo, settings, ssh and gpg keys, add ssh key
    23. Enable ssh on local machine
    https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
    24. Add ssh private key to ssh-agent
    25. ssh-add ~/gp-git-key
    Identity added: /c/Users/skgur/gp-git-key (skguruprasad@gmail.com)
26. git push orgin main
    origin => represents the remote repo
    main => is the branch of the repo
27. vscode, prompted the browser authentication for github, i cancelled
28. vscode, again prompted vscode to be allowed to authenticate github with username and password and i accepted.
29. git push worked, but not sure if due to ssh or vscode unp 
30. post push, i can see my new file till step 10 when the commit was done.

/c/Users/skgur/.ssh/gp-git-key: No such file or directory

skgur@LAPTOP-634LMU0N MINGW64 ~/Downloads/gp/Code/github-slideshow (main)       
$ ssh-add ~/gp-git-key
Identity added: /c/Users/skgur/gp-git-key (skguruprasad@gmail.com)

skgur@LAPTOP-634LMU0N MINGW64 ~/Downloads/gp/Code/github-slideshow (main)       
$ git push origin main
fatal: helper error (-1): authentication prompt was canceled
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 596 bytes | 45.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gpkarnam/github-slideshow.git
   2a025b2..0310bc4  main -> main
31. 