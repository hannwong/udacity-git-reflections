# Reflection 1

## What happens when you initialize a repository? Why do you need to do it?

Git creates a hidden folder ``.git`` which contains metadata for the new and blank Git
repository.

According the the video "_What Makes a Repository a Repository?_", 2 types of stuff are
contained in ``.git``:

* config (configurations for the git repository?)
* objects (actual file contents tracked by Git?)

I need to do a ``git init`` so that Git actually creates a Git repository in the folder I choose to
make a Git repository. If I don't do that initialization, the folder will be a plain vanilla folder
that is *not* a Git repository, and Git wouldn't be able to operate on it (like track my change
history in that folder).

How is the staging area different from the working directory and the repository?
What value do you think it offers?

# Reflection 2

## How is the staging area different from the working directory and the repository? What value do you think it offers?

The staging area is different from the working directory in that it only contains the changes that
are staged (``git add``), whereas the working directory contains all changes made (since the last
commit).

The staging area is also different from the repository in that it contains changes that are _not_
committed (this is similar to the working directory), whereas the repository contains changes that
are committed.

The staging area allows me to work really fast and include into the working directory all changes my
mind happens to think about at any second in time. This way of working frees me from overheads such
as _planning_ and _(strategic) organization_, and frees me up to focus on the _tactical_ aspects
(actual work). I do have to perform planning and strategizing, but the coding phase isn't suited for
that but is instead more suited for experimentation, exploration and actual work.

Another benefit the staging area provides is the ability for me to make logical and coherent commits
(units of changes). No matter how much work brain pukes out, I can capture all that work in the
working directory, and still be able to cleanly craft logical commits
via the staging area.

# Reflection 3

## How can you use the staging area to make sure you have one commit per logical change?

Only ``git add`` from the working directory to the staging area those changes that make up a logical
change. After reviewing the staged changes and confirming that they constitute a single logical and
integral change, I can commit those staged changes.

# Reflection 4

## What are some situations when branches would be helpful in keeping your history organized? How would branches help?

* Exploring 2 untested approaches to a problem, and then picking the best parts of both.
* Creating (and keeping) a feature that may be useful, but may ultimately not be wanted (yet) by users.
* Creating a bugfix for some published branch, and this fix does not apply for the unpublished
  (experimental or developmental) branch.

# Reflection 5

## How do the diagrams help you visualize the branch structure?

They show which commits are reachable by which branches.

Commits that are unreachable by a particular branch will not contribute code to that branch. For
example, if Commit A contains a bug fix for a bug that is also in Branch B, and if Commit A is
unreachable by Branch B, that would mean Branch B does not contain the bug fix contributed by Commit
A.

# Reflection 6

## What is the result of merging two branches together? Why do we represent it in the diagram the way we do?

The result is a new commit that contains the changes from both branches. The "*changes from both
branches*" actually mean the changes since the branches diverged, at which point is really the
common commit (base?) of both branches.

Since the new commit contains changes from both branches, it has both branches (the commit at *tip*
of each branch) as parents. Notice that each regular non-merge commit always contains all the codes
in its parent, and a diagram would link it to its parent; the same principle applies for merge
commits that contain codes from multiple parents.

# Reflection 7

## What are the pros and cons of Git’s automatic merging vs. always doing merges manually?

Pro of automatic merging: Git's automatic merging handles 80% of the merges we encounter. Most of
the time, a bare minimum of team communication will prevent team members from working on the same
project areas and potentially duplicating each other's efforts (waste of manpower). Without
automatic merging, merging efforts would increase at least four times (assuming automatic merging
handles 80% of all merge cases).

Con of automatic merging: There can be cases where Git's automatic merging goes through without
issue, but a bug or code duplication actually occurred. Let's say a function was modified by
Programmer A at line 50, a new invocation of the function was inserted by Programmer B at
line 100. The new invocation could be surrounded by new code that relied on the old behavior of the
function before modification by Programmer A. In this case, Git would accept both changes, and cause
a bug in Programmer B's function invocation.

Test-Driven Development (TDD) can be useful in spotting such errors quickly and pretty much
automatically (using test suites).
