# Git Commands Reference Table

| Command          | Plain Language                                             | Formal Definition                                                                                                                                          |
| ---------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git log`          | What happened in this branch?                              | Shows the commit history of a repository, displaying commit messages, authors, dates, and IDs.                                                             |
| `git reflog`       | Where have I been?                                         | Displays a history of branches and commits that you have checked out, showing your navigation path through the repository.                                 |
| `git reset`        | Unstage if it's a file and delete commits if it's a branch | Updates the branch reference and optionally modifies the staging area or working directory, used to undo changes.                                          |
| `git reset --hard` | Make this branch point to a different commit               | Resets the branch pointer to specified commit, discards all changes in staging area and working directory.                                                 |
| `git diff`         | Show me what lines have changed since the last commit      | Shows changes between commits, commit and working tree, etc., displaying added, removed, and modified lines.                                               |
| `git rebase`       | Pretend I started here                                     | Reapplies commits on top of another base commit, effectively rewriting the commit history by moving a branch to a new starting point.                      |
| `git rebase -i`    | Let me rewrite history                                     | Interactive rebase that allows editing, reordering, squashing, or dropping commits before reapplying them to the base.                                     |
| `git restore`      | Give me a different version of this file                   | Restores specified files from a specific source (commit, stage, etc.) to the working directory.                                                            |
| `git switch`       | Go to another branch                                       | Switches to the specified branch, creating it if necessary when used with -c option.                                                                       |
| `git checkout`     | Restore plus switch                                        | Switches between branches or restores working tree files, updating the working directory to match the selected branch or commit.                           |
| `git add`          | Make this part of the next commit                          | Adds file contents to the staging area (index), preparing them to be included in the next commit.                                                          |
| `git add -p`       | Decide what is part of my next commit                      | Interactively choose portions of files to stage, allowing you to make more granular commits.                                                               |
| `git status`       | What files changed since the last commit                   | Displays the state of the working directory and staging area, showing which changes have been staged, which haven't, and which files aren't being tracked. |
| `git cherry-pick`  | Give me the changes from this commit                       | Applies changes introduced by existing commits to the current branch, creating new commits with the same changes.                                          |

# Git Cheatsheet

## Core Concepts

- **Git**: A distributed version control system that tracks changes to files and
  coordinates work among multiple people.
- **Hash**: A unique code (like a fingerprint) that Git creates for each commit
  to identify it; every change gets its own specific ID number.
- **Log**: A history of commits showing author information, timestamps, and
  commit messages, accessed using the `git log` command.
- **Ref**: A human-readable name that points to a specific commit, such as
  branch names, tags, or HEAD.
- **Reflog**: A log that records all changes to refs in your local repository,
  useful for recovering lost commits or branches.
- **Commit**: A saved snapshot of your project at a specific moment, like taking
  a photo of your work that you can return to later.
- **Branch**: A separate line of development that lets you work on features or
  fixes without affecting the main project; think of it as a bookmark that moves
  forward as you make new changes.
- **Staging**: The process of marking modified files to be included in the next
  commit using `git add`.
- **File Tree**: The hierarchical structure of files and directories tracked by
  Git at a specific commit.
- **Release**: A labeled version of your project that's ready to share with
  users, typically representing a completed set of features or improvements.
- **Patch**: A small file that contains just the specific changes made to code,
  allowing you to share and apply these changes without sending the entire
  project.
- **Diff**: A representation of the differences between files, commits, or
  branches, showing what was added, removed, or modified.
- **File**: Any document or data tracked by Git, which can exist in different
  states: untracked, tracked, modified, staged, or committed.
- **HEAD**: A pointer that indicates which commit you're currently looking at or
  working with; it usually points to the latest commit on your current branch.
