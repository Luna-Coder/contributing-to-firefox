# contributing-to-firefox

`hg add filename1 filename2`

Begin tracking changes to files or folders.
* Unlike git, in mercurial the `add` command is only used for *new* files, not files you want to begin tracking.

\
`hg commit -m "commit message"`

Commit all outstanding changes reported by `hg status` into the repository.
* The state of the working directory relative to its parents is recorded as a new changeset (revision).

\
`hg commit --amend -m "amend message"`

The `--amend` flag can be used to update a changeset.
* The amendment will take place in the parent of the working directory.

\
`hg pull central`

Pull changes from a remote repository to a local one.
* In our case, `mozilla-central` is the remote repository. Since this is the only repository we work with, `central` is optional.

\
`hg pull central -u` 

The `-u` flag is used to pull and update to the new branch head in one step.
* In mercurial, pulling changes and updating is a two-step process, this method makes it less verbose.

\
`hg update central`

Update working directory or navigate to different revision. Useful when working on multiple bugs and need to switch between them.

* May also appear as the alias `hg up`. 
* In our case, we update to the `central` branch after pulling the changes.

\
`hg update --clean`

* The `--clean` flag discards uncommitted changes.
* Useful if you want to cancel modifications made to files that have not been committed.

\
`hg update tip`

* Update work to match `tip`.

\
`hg update <REV>`

* Update work to specified revision.
* <REV> can be a Revision ID (####) or SHA-1 (#a#b#c#).
  
\
`hg wip`
 
* Displays a colorful tree view of the work in progress of changesets relevant to you.
* This command is a variation of the `hg log` command. Normally used in conjunction with `hg update` to view revisions to navigate to.

\
`hg status [filename]`

* Show changed files in the working directory or in the file if a filename is given.
* See hg status codes for info regarding the meaning of the prefix symbols.

\
`hg status --change <REV>`

* list the changed files of a given revision.

\
`hg revert [filename]`

* Discards changes and restores files to their unmodified state.
* The modified file is saved as `filename.orig` and `hg status` will list it as not tracked `? filename.orig`

\
`hg rebase`
* command to move changeset (and descendants) to a different branch.
* usually used after ‘hg pull central’ to place a changeset on top of the latest changes.






