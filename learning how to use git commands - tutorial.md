learning how to use git commands - tutorial
pwd- mostra o diretório em que estamos
cd (caminho do diretório da pasta)
Git init (diretório interno do doc). OU Git clone (Diret[orio externo do doc) 
obs - mudanças no arquivo constam como modified (nesse caso ainda nunca adicionadas e não add ou salvas no repositório - untracked)
obs 2: Cmd Cd (caminho do diretório) navega na pasta raiz; Cmd Cd .. Vai voltando no diretório
Git Status - Mostra o status do que foi feito no versionamento do código
git add nome do arquivo passa o arquivo para a área de staged
git commit -am "nome do arquivo" - passa o arquivo para a área de unmoodified (salvo com todas as alteraçoes - não existem novas alterações a serem feitas)
Git remote add origin url - cria link entre o repositório remoto (github)
git push -u origin main - importa o repositório interno para o remoto (github).
git fetch ver se tem algo no reposit[orio remoto para fazer alterações no local
Git Pull - traz do reposit[orio remoto pro local]


CMDS USADOS 

cisinojr ~/Documents/datasciencecourse  $ pwd
/Users/cisinojr/Documents/datasciencecourse
cisinojr ~/Documents/datasciencecourse  $ cd ..
cisinojr ~/Documents  $ cd /Users/cisinojr/Documents/datasciencecourse
cisinojr ~/Documents/datasciencecourse  $ git init /Users/cisinojr/Documents/datasciencecourse 
Initialized empty Git repository in /Users/cisinojr/Documents/datasciencecourse/.git/
cisinojr ~/Documents/datasciencecourse  $ git add learning how to use git commands - tutorial.md
fatal: pathspec 'learning' did not match any files
cisinojr ~/Documents/datasciencecourse  $ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add
cisinojr ~/Documents/datasciencecourse  $ git add .
cisinojr ~/Documents/datasciencecourse  $ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   learning how to use git commands - tutorial.md

cisinojr ~/Documents/datasciencecourse  $ git commit learning 
error: pathspec 'learning' did not match any file(s) known to git
cisinojr ~/Documents/datasciencecourse  $ git commit learning how to use commands - tutorial.md
error: pathspec 'learning' did not match any file(s) known to git
error: pathspec 'how' did not match any file(s) known to git
error: pathspec 'to' did not match any file(s) known to git
error: pathspec 'use' did not match any file(s) known to git
error: pathspec 'commands' did not match any file(s) known to git
error: pathspec '-' did not match any file(s) known to git
error: pathspec 'tutorial.md' did not match any file(s) known to git
cisinojr ~/Documents/datasciencecourse  $ git commit -m "first commit"
[main (root-commit) 93d544e] first commit
 1 file changed, 9 insertions(+)
 create mode 100644 learning how to use git commands - tutorial.md
cisinojr ~/Documents/datasciencecourse [main] $ git status
On branch main
nothing to commit, working tree clean
cisinojr ~/Documents/datasciencecourse [main] $ git log
commit 93d544edb4d1f58288f14e3c1287b409bf1fbc84 (HEAD -> main)
Author: Cisino Junior <cisino.gomes@stone.com.br>
Date:   Fri May 26 16:20:45 2023 -0300

    first commit
cisinojr ~/Documents/datasciencecourse [main] $ git commit -am "second commit"
[main 99a863f] second commit
 1 file changed, 2 insertions(+), 1 deletion(-)
cisinojr ~/Documents/datasciencecourse [main] $ git status
On branch main
nothing to commit, working tree clean
cisinojr ~/Documents/datasciencecourse [main] $ git remote add origin https://github.com/AdriCardozo/learninghowtousegitcommands.git
cisinojr ~/Documents/datasciencecourse [main] $ git push origin -u
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

cisinojr ~/Documents/datasciencecourse [main] $ git commit -am "third commit"
On branch main
nothing to commit, working tree clean
cisinojr ~/Documents/datasciencecourse [main] $ git commit -am "third commit"
[main 61b2d1a] third commit
 1 file changed, 2 insertions(+), 1 deletion(-)
cisinojr ~/Documents/datasciencecourse [main] $ git commit-am "fourty commit" 
git: 'commit-am' is not a git command. See 'git --help'.

The most similar command is
        commit-graph
cisinojr ~/Documents/datasciencecourse [main] $ git commit -am "fourty commit"
[main 02aaafb] fourty commit
 1 file changed, 1 insertion(+), 1 deletion(-)
cisinojr ~/Documents/datasciencecourse [main] $ git push 
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

cisinojr ~/Documents/datasciencecourse [main] $  git push -u origin main 
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 1.46 KiB | 1.46 MiB/s, done.
Total 12 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/AdriCardozo/learninghowtousegitcommands.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
cisinojr ~/Documents/datasciencecourse [main] $ git commit -am "final commit"
[main 9e504f2] final commit
 1 file changed, 1 insertion(+), 1 deletion(-)
cisinojr ~/Documents/datasciencecourse [main] $ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 378 bytes | 378.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/AdriCardozo/learninghowtousegitcommands.git
   02aaafb..9e504f2  main -> main
branch 'main' set up to track 'origin/main'.
cisinojr ~/Documents/datasciencecourse [main] $ git push -u origin main       
