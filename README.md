# contributing-to-firefox


| Command | Description| Additional Info |
| --- | --- | --- |
| `hg add filename1 filename2` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Begin tracking changes to files or folders. | Unlike git, in mercurial the `add` command is only used for *new* files, not files you want to begin tracking. |
| |
| `hg commit -m "commit message"` | Commit all outstanding changes reported by `hg status` into the repository. | The state of the working directory relative to its parents is recorded as a new changeset (revision). |
| |
| `hg commit --amend -m "amend message"` | The `--amend` flag can be used to update a changeset. | The amendment will take place in the parent of the working directory. |
| |
| `hg pull central` | Pull changes from a remote repository to a local one. | In our case, `mozilla-central` is the remote repository. Since this is the only repository we work with, `central` is optional. |
| |
