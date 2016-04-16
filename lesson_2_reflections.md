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
working directory, and still be able to cleanly craft logical commits via the staging area.

What are some situations when branches would be helpful in keeping your history
organized? How would branches help?

How do the diagrams help you visualize the branch structure?

What is the result of merging two branches together? Why do we represent it in
the diagram the way we do?

What are the pros and cons of Git’s automatic merging vs. always doing merges
manually?
