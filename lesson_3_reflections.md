# Reflection 1

## When would you want to use a remote repository rather than keeping all your work local?

When I want to collaborate with other people on my project.

Having the "_origin_" Git repo online where all my team members can access it allows all team
members to pull (download) each other's changes.

# Reflection 2

## Why might you want to always pull changes manually rather than having Git automatically stay up-to-date with your remote repository?

In cases where the remote branch has some new commits added, doing a pull will probably merge those
changes into my local branch! That doesn't make me lose any local commits, but it is still annoying
to have my branch moved forward to contain merges I'm not ready to review and incorporate into my
project.

Hence, an automatic pull would be annoying and can potentially break my train of thought as a work
on my local branch.

What about the case where my local branch contains some commits the remote doesn't have? Does Git
warn me about that and avoid doing the pull?

# Reflection 3

## Describe the differences between forks, clones, and branches.  When would you use one instead of another?

Fork is a GitHub feature which basically clones a Git repository residing on GitHub into a new Git
repository that will also reside on GitHub.

Clone is a Git feature that duplicates an entire Git repository onto another location (which may be
on another machine or even on the same machine).

Branch is a Git feature that is essentially a label pointing to a commit. In labeling a commit like
this, all commits from that commit and upstream will be taken as part of the branch.

I would use a Fork to attribute the basis of my new work to the original author of that basis. So,
when I forked Larry's *recipes* repository, my own *recipes* repository on GitHub would contain a
link that attributes the basis of my work (on the new repository) to Larry. I would imagine that my
"*contributing*" to a Fork could be a way for Larry to assess my skills before officially making me
a contributor (with ``git push`` permissions) on his repository, if he deems me good enough.

I would use a Clone whenever I need to work on a repository from a new location (new machine,
usually). This is very different from a Fork. If I clone Larry's repository while still having no
permission to ``git push`` to that repository, my Clone will still *not* allow me to push to that
repository.

I would use a Branch whenever I need to work on a new feature, experiment or approach within an
existing repository. I can imagine also using a Branch to *KIV work-in-progress* that I am not sure
I want to keep or discard. Or, just before I'm about to do some crazy Git operations that may result
in loss of some commits.

# Reflection 4

## What is the benefit of having a copy of the last known state of the remote stored locally?

* Work offline, anywhere.
* Redundancy, in case the remote crashes and is destroyed.

# Reflection 5

## How would you collaborate without using Git or GitHub?  What would be easier, and what would be harder?

I would be sending many versions of my files to my team members. We would all be using diff programs
to hopefully generate visually convenient diffs between the different versions. We would have to
communicate a lot just to confirm what changes were made and what changes we're supposed to review
for one another. We would also need an elaborate "*version naming*" convention to ensure we can
reliably refer to any particular version in our team communication. In short, communicating without
GitHub's "*Pull Request*" feature would be disjointed and would require non-trivial manual
coordination.

What would be easier is that we won't have to learn Git and GitHub. Sending versions of files to one
another via file transfers (DropBox, BitTorrent Sync, etc) is easy; ``git push`` and ``git pull``
require a non-trivial understanding of Git concepts.

What would be harder is everything else besides what is easy (mentioned above), such as team
communication, referring to any particular version, making sure we're reviewing the correct changes,
etc. It may be easy to just send versions of files to one another, but we can also easily get
overwhelmed by the sheer number of files being thrown back and forth within the team.

# Reflection 6

## When would you want to make changes in a separate branch rather than directly in master?  What benefits does each approach have?

* To keep each programmer's work distinct from one another.

  This way, each programmer won't have his base (his previous commits on the branch he's working on)
  change from under him.

  This is also great for reviewing each programmer's work to design training programs tailored to
  each individual programmer.

* To separate work into distinct coherent and integral tracks (branches).

  Like Feature A will be on a separate branch from Feature B, both features being in development at
  the same time.

The main benefits of using the separate-branch approach has to do with *facilitation of
collaboration*. Each programmer's work is kept coherent (so is his train of thought) and kept
integral without interruptive changes from other people. That *coherence of each programmer's work*
also lends well to easy comprehension of his work by other team members, facilitating peer reviews
and especially benefiting discussions for merging together work that was done separately.

The main benefit of using the single-branch approach is that we can avoid complex merge
conflicts. An arguably weak benefit is that all programmers are forced to keep up-to-date with one
another *at all times* (which can be disrupting to workflow, ironically).  The inevitable *frequent
call to incorporate all other team member's work* ensures that everyone is up-to-date with everyone
all the time (or at least when they try to perform a ``git status`` or ``git commit``). As each
programmer commits onto the single branch, all other programmers will immediately have to check that
commit and incorporate it into their own work. This approach can only benefit small teams; for
larger teams, there would be more "*noise*" than actual work done.
