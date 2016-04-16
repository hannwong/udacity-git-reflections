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

What is the benefit of having a copy of the last known state of the remote
stored locally?

    Fill in your answer here

How would you collaborate without using Git or GitHub?  What would be easier,
and what would be harder?

    Fill in your answer here

When would you want to make changes in a separate branch rather than directly in
master?  What benefits does each approach have?

    Fill in your answer here
