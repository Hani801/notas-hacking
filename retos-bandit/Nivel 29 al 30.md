## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

## Datos de acceso al nivel
Usuario: bandit29@bandit.labs.overthewire.org
Contraseña: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
Puerto: 2220
## Solución
bandit29@bandit:~$ mkdir /tmp/llave
mkdir: cannot create directory ‘/tmp/llave’: File exists
bandit29@bandit:~$ mkdir /tmp/llave12
bandit29@bandit:~$ cd /tmp/llave12
bandit29@bandit:/tmp/llave12$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/llave12$ ls
repo
bandit29@bandit:/tmp/llave12$ cd repo/
bandit29@bandit:/tmp/llave12/repo$ ls
README.md
bandit29@bandit:/tmp/llave12/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/llave12/repo$ git log
commit 4364630b3b27c92aff7b36de7bb6ed2d30b60f88 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    fix username

commit fca34ddb7d1ff1f78df36538252aea650b0b040d
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/llave12/repo$ git checkout 4364630b3b27c92aff7b36de7bb6ed2d30b60f88
Note: switching to '4364630b3b27c92aff7b36de7bb6ed2d30b60f88'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 4364630 fix username
bandit29@bandit:/tmp/llave12/repo$ ls
README.md
bandit29@bandit:/tmp/llave12/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/llave12/repo$ git branch
* (HEAD detached at 4364630)
  master
bandit29@bandit:/tmp/llave12/repo$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
bandit29@bandit:/tmp/llave12/repo$ git logg
git: 'logg' is not a git command. See 'git --help'.

The most similar command is
        log
bandit29@bandit:/tmp/llave12/repo$ git logg
git: 'logg' is not a git command. See 'git --help'.

The most similar command is
        log
bandit29@bandit:/tmp/llave12/repo$ git log
commit 4364630b3b27c92aff7b36de7bb6ed2d30b60f88 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    fix username

commit fca34ddb7d1ff1f78df36538252aea650b0b040d
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/llave12/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/llave12/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/llave12/repo$ git log
commit 1d160de5f8f647f00634bbf3d49b9244275217b6 (HEAD -> dev, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    add data needed for development

commit 73d0f769233ffc2f59595412e22f41afc6218c04
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    add gif2ascii

commit 4364630b3b27c92aff7b36de7bb6ed2d30b60f88 (origin/master, origin/HEAD, master)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    fix username

commit fca34ddb7d1ff1f78df36538252aea650b0b040d
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Oct 5 06:19:43 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/llave12/repo$ ls
code  README.md
bandit29@bandit:/tmp/llave12/repo$ cat RE
cat: RE: No such file or directory
bandit29@bandit:/tmp/llave12/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS



## Notas
El comando `git checkout` cambia entre ramas o restaura los archivos del árbol de trabajo (working tree)

## Referencias 
