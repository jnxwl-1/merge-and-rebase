# merge-and-rebase

host@host MINGW64 ~/Documents (master)
$ git clone https://github.com/jnxwl-1/merge-and-rebase.git homework
Cloning into 'homework'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

host@host MINGW64 ~/Documents (master)
$ cd h
HW/       homework/

host@host MINGW64 ~/Documents (master)
$ cd h
HW/       homework/

host@host MINGW64 ~/Documents (master)
$ cd homework/

host@host MINGW64 ~/Documents/homework (main)
$ mkdir branching

host@host MINGW64 ~/Documents/homework (main)
$ cd branching/

host@host MINGW64 ~/Documents/homework/branching (main)
$ nano merge.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (main)
$ nano rebase.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (main)
$ git add *

host@host MINGW64 ~/Documents/homework/branching (main)
$ git commit -m "prepare for merge and rebase"
[main 66d7955] prepare for merge and rebase
 2 files changed, 17 insertions(+)
 create mode 100644 branching/merge.sh
 create mode 100644 branching/rebase.sh

host@host MINGW64 ~/Documents/homework/branching (main)
$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 532 bytes | 532.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/jnxwl-1/merge-and-rebase.git
   83be0f0..66d7955  main -> main

host@host MINGW64 ~/Documents/homework/branching (main)
$ git checkout -b git-merge
Switched to a new branch 'git-merge'

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ nano merge.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git add merge.sh

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git commit -m "merge: @ instead *"
[git-merge 57012fe] merge: @ instead *
 1 file changed, 2 insertions(+), 2 deletions(-)

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git push origin git-merge
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 443 bytes | 443.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'git-merge' on GitHub by visiting:
remote:      https://github.com/jnxwl-1/merge-and-rebase/pull/new/git-merge
remote:
To https://github.com/jnxwl-1/merge-and-rebase.git
 * [new branch]      git-merge -> git-merge

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ nano merge.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git add merge.sh

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git commit -m "merge: use shift"
[git-merge 0ee415b] merge: use shift
 1 file changed, 3 insertions(+), 2 deletions(-)

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git push origin git-merge
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 513 bytes | 513.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jnxwl-1/merge-and-rebase.git
   57012fe..0ee415b  git-merge -> git-merge

host@host MINGW64 ~/Documents/homework/branching (git-merge)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

host@host MINGW64 ~/Documents/homework/branching (main)
$ nano rebase.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (main)
$ git add rebase.sh

host@host MINGW64 ~/Documents/homework/branching (main)
$ git commit -m "replace lines in rebase.sh"
[main 9416e5f] replace lines in rebase.sh
 1 file changed, 4 insertions(+), 2 deletions(-)

host@host MINGW64 ~/Documents/homework/branching (main)
$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 455 bytes | 455.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jnxwl-1/merge-and-rebase.git
   66d7955..9416e5f  main -> main

host@host MINGW64 ~/Documents/homework/branching (main)
$ git log
commit 9416e5f8ce1b6b4f755ad915550a7c0b2388088b (HEAD -> main, origin/main, origin/HEAD)
Author: Евгений Кандауров <e@servicews.ru>
Date:   Fri Aug 6 01:24:01 2021 +0300

    replace lines in rebase.sh

commit 66d79557b06825d3ce9413f2897d19869aa2bfcf
Author: Евгений Кандауров <e@servicews.ru>
Date:   Fri Aug 6 01:12:15 2021 +0300

    prepare for merge and rebase

commit 83be0f0a19d99680498ad54860a0879f3fcde096
Author: Evgeniy Kandaurov <87278229+jnxwl-1@users.noreply.github.com>
Date:   Fri Aug 6 01:03:48 2021 +0300

    Initial commit

host@host MINGW64 ~/Documents/homework/branching (main)
$ ^C

host@host MINGW64 ~/Documents/homework/branching (main)
$ git checkout 66d79557b06825d3ce9413f2897d19869aa2bfcf
Note: switching to '66d79557b06825d3ce9413f2897d19869aa2bfcf'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 66d7955 prepare for merge and rebase

host@host MINGW64 ~/Documents/homework/branching ((66d7955...))
$ git checkout -b git-rebase
Switched to a new branch 'git-rebase'

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ nano rebase.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git add rebase.sh

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git commit -m "git-rebase 1"
[git-rebase b047ef9] git-rebase 1
 1 file changed, 4 insertions(+), 2 deletions(-)

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git push origin git-rebase
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 450 bytes | 450.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'git-rebase' on GitHub by visiting:
remote:      https://github.com/jnxwl-1/merge-and-rebase/pull/new/git-rebase
remote:
To https://github.com/jnxwl-1/merge-and-rebase.git
 * [new branch]      git-rebase -> git-rebase

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ nano rebase.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git add rebase.sh

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git commit -m "git-rebase 2"
[git-rebase 7aba4bb] git-rebase 2
 1 file changed, 1 insertion(+), 1 deletion(-)

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git push origin git-rebase
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 424 bytes | 424.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jnxwl-1/merge-and-rebase.git
   b047ef9..7aba4bb  git-rebase -> git-rebase

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

host@host MINGW64 ~/Documents/homework/branching (main)
$ git merge git-merge
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory
Merge made by the 'recursive' strategy.
 branching/merge.sh | 5 +++--
 1 file changed, 3 insertions(+), 2 deletions(-)

host@host MINGW64 ~/Documents/homework/branching (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 417 bytes | 417.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jnxwl-1/merge-and-rebase.git
   9416e5f..ee691f4  main -> main

host@host MINGW64 ~/Documents/homework/branching (main)
$ git rebase -i main
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory
Successfully rebased and updated refs/heads/main.

host@host MINGW64 ~/Documents/homework/branching (main)
$ git checkout git-rebase
Switched to branch 'git-rebase'

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git rebase -i main
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory
error: could not parse 'pick'
error: invalid line 2: fixup pick 7aba4bb git-rebase 2
You can fix this with 'git rebase --edit-todo' and then run 'git rebase --continue'.
Or you can abort the rebase with 'git rebase --abort'.

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE)
$ git rebase -i main
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE)
$ git rebase --abort

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git rebase -i main
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory
error: could not apply b047ef9... git-rebase 1
Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply b047ef9... git-rebase 1
Auto-merging branching/rebase.sh
CONFLICT (content): Merge conflict in branching/rebase.sh

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 1/2)
$ cat rebase.sh
#!/bin/bash
# display command line options

count=1
for param in "$@"; do
<<<<<<< HEAD
    echo "\$@ Parameter #$count = $param"
=======
    echo "Parameter: $param"
>>>>>>> b047ef9 (git-rebase 1)
    count=$(( $count + 1 ))
done

echo "====="

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 1/2)
$ nano rebase.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 1/2)
$ git add rebase.sh

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 1/2)
$ git rebase --continue
error: could not apply 7aba4bb... git-rebase 2
Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply 7aba4bb... git-rebase 2
Auto-merging branching/rebase.sh
CONFLICT (content): Merge conflict in branching/rebase.sh

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 2/2)
$ nano rebase.sh
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 2/2)
$ git add rebase.sh

host@host MINGW64 ~/Documents/homework/branching (git-rebase|REBASE 2/2)
$ git rebase --continue
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory
[detached HEAD 9cb4779] Merge branch 'git-merge'
 Date: Fri Aug 6 01:32:25 2021 +0300
Successfully rebased and updated refs/heads/git-rebase.

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git pu
pull   push

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git push -u origin git-rebase
To https://github.com/jnxwl-1/merge-and-rebase.git
 ! [rejected]        git-rebase -> git-rebase (non-fast-forward)
error: failed to push some refs to 'https://github.com/jnxwl-1/merge-and-rebase.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git push -u origin git-rebase -f
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 479 bytes | 479.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jnxwl-1/merge-and-rebase.git
 + 7aba4bb...9cb4779 git-rebase -> git-rebase (forced update)
Branch 'git-rebase' set up to track remote branch 'git-rebase' from 'origin'.

host@host MINGW64 ~/Documents/homework/branching (git-rebase)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

host@host MINGW64 ~/Documents/homework/branching (main)
$ git merge git-rebase
Error in /etc/nanorc on line 237: Error expanding /usr/share/nano/*.nanorc: No such file or directory
Merge made by the 'recursive' strategy.
 branching/rebase.sh | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

host@host MINGW64 ~/Documents/homework/branching (main)
