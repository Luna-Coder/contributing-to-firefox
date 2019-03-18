# contributing-to-firefox

**`hg add filename1 filename2`**
\- Begin tracking changes to files or folders.

* Unlike git, in mercurial the `add` command is only used for *new* files, not files you want to begin tracking.

\
**`hg commit -m "commit message"`**
\- Commit all outstanding changes reported by `hg status` into the repository.

* The state of the working directory relative to its parents is recorded as a new changeset (revision).

\
**`hg commit --amend -m "amend message"`**
\- The `--amend` flag can be used to update a changeset.

* The amendment will take place in the parent of the working directory.

\
**`hg pull central`**
\- Pull changes from a remote repository to a local one.

* In our case, `mozilla-central` is the remote repository. Since this is the only repository we work with, `central` is optional.

\
**`hg pull central -u`**
\- The `-u` flag is used to pull and update to the new branch head in one step.

* In mercurial, pulling changes and updating is a two-step process, this method makes it less verbose.

\
**`hg update central`**
\- Update working directory or navigate to different revision. 

* May also appear as the alias `hg up`. 
* Useful when working on multiple bugs and need to switch between them.
* In our case, we update to the `central` branch after pulling the changes.

\
**`hg update --clean`**
\- The `--clean` flag discards uncommitted changes.

* Useful if you want to cancel modifications made to files that have not been committed.

\
**`hg update tip`**
\- Update work to match `tip`.

\
**`hg update <REV>`**
\- Update work to specified revision.

* <REV> can be a Revision ID (####) or SHA-1 (#a#b#c#).
  
\
**`hg wip`**
\- Displays a colorful tree view of the work in progress of changesets relevant to you.

* This command is a variation of the `hg log` command. Normally used in conjunction with `hg update` to view revisions to navigate to.

\
**`hg status [filename]`**
\- Show changed files in the working directory or in the file if a filename is given.

* See hg status codes for info regarding the meaning of the prefix symbols.

\
**`hg status --change <REV>`**
\- List the changed files of a given revision.

\
**`hg revert [filename]`**
\- Discards changes and restores files to their unmodified state.

* The modified file is saved as `filename.orig` and `hg status` will list it as not tracked `? filename.orig`

\
**`hg rebase`**
\- Command to move changeset (and descendants) to a different branch.

* usually used after ‘hg pull central’ to place a changeset on top of the latest changes.

\
**`hg rebase [-s <REV> | -b <REV>] [-d <REV>]`**

* -s <REV> source flag used to rebase the specified changeset and descendants.
* -b <REV> base flag used to rebase everything from branching point of specified changeset.
* -r <REV> rev flag to signals to rebase these revisions.
* -d <REV> destination flag to rebase onto the specified changeset.
  
\
**`hg forget filename`**
\- Mark the specified file(s) so they will no longer be tracked after the next commit.

* This only removes files from the current branch, not from the entire project history, and it does not delete them from the working directory.

\
**`hg remove filename`**
\- Stop tracking and remove the specified files from the current branch on the next commit.

* May also appear as the alias `hg rm`.

\
**`hg diff [filename]`**
\- List tracked file changes or changes to a file if a file is specified.

\
**`hg diff -r <REV> -r <REV> [filename]`**
\- Show differences between revisions for the specified file(s) or directory.

* Displays the file names along with any uncommitted changes you have made to a file.

\
**`hg log [file]`**
\- Show revision history of entire repository or files.

* By default is prints revision number, changeset id, tags, user, date/time, and summary for each commit.

\
**`hg summary`**
\- Generates a brief summary of the working directory state, including parents, branch, commit status, phase and available updates.

\
**`hg heads [<REV>]`**
\- With no arguments, show all open branch heads in the repository. 

* Branch heads are changesets that have no descendants on the same branch.
* If one or more <REV> is given, only open branch heads on the branches associated with the specified changesets are shown.

\
**`hg histedit`**
\- Interactive history editing

* visit link for more information https://www.mercurial-scm.org/doc/hg.1.html#histedit

\
**`hg strip <REV>`**
\- The strip command removes the specified changesets and all their descendants. from history.

* visit link for more information https://www.mercurial-scm.org/doc/hg.1.html#strip


\
**`arc help`**
\- Displays detailed help about available commands

\
**`arc help [command]`**
\- Detailed information about a specific command

\
**`arc diff`**
\- Send your code to Differential for review.

* Alternatively the `moz-phab` command is available.

\
**`arc diff --create`**
\- Force create a revision in the working copy.

\
**`arc diff --update <REV>`**
\- Force update a specific revision.

\
**`arc which`**
\- Displays what `arc` believes to be in the working copy.

\
**`arc list`**
\- Show pending revision information.

\
**`arc close-revision`**
\- Closes a revision from the CLI without going through the web UI.

