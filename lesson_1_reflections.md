# Reflection 1

## How did viewing a diff between two versions of a file help you see the bug that was introduced?

Viewing the diff let me quickly spot all changes to the file. Since any change can potentially
introduce a bug, the diff lets me easily run through the changes systematically to assess whether
each change can cause a bug.

The 2 benefits that I saw were:

1. Easy and quick listing of all changes (which usually comprise only 1-5% of the whole file, if the
   changes are small and focused.)
1. Facilitates systematic review of all changes to find bug.

One reservation I have is about benefit 1 above. What if the changes are not small and focused, but
instead comprise at least 50% of the whole file? Then the diff will be rendered a lot less useful
(though still more useful than looking at 2 versions of the file side-by-side).

# Reflection 2

## How could having easy access to the entire history of a file make you a more efficient programmer in the long term?

Great for reflection and continuous learning! I could easily answer questions like "*what was I
thinking when I made that newbie mistake?*".

Given quick answers that quickly explain my past idiocy, I can benefit in the following ways:

1. Always be notified of and taught by all of my past idiocies.
1. Quickly identify a past idiocy, and save time in fixing consequent errors (rather than trying
   hard to figure out if the "_error_" was really a past genius).
1. Easily see a conherent train of thought from the string of past history. Guides my continuing the
   work-in-progress.
1. Let's me restore past "_genius_" moves that I unwittingly overwrote or deleted.
1. Makes me faster at work, have more appetite for risk, have reduced _planning paralysis_.

One reservation I have about all benefits above... I would still have to assess each change to flag
it as "_idiocy_" or "_genius_". I could solve that by annotating my file, but that would clutter up
the file's content; that wouldn't work if I'm drafting a long legal document or any document I
intend to publish to someone.

Now that I think about it, about the only benefit I can really reap of the last one: increased work
speed, increased risk appetite and exploration efficiency, decreased planning paralysis.

# Reflection 3

## What do you think are the pros and cons of manually choosing when to create a commit, like you do
in Git, vs having versions automatically saved, like Google docs does?

Manual Commits:

* Pro: Each commit is a logical and coherent unit of change.

  That would avoid a situation where I tell my boss to review my work like this... "_Boss, I've built
  23% of the table you asked for, and 12% of the chair. Could you maybe check my work in the West
  Factory for the table, and the East Factory for the chair? Just doing my job reporting to you and
  getting my work checked and reviewed!_"

  Instead, it could be like "_Boss, I've completed 2 tasks for the table, which is to fashion the
  legs and table top. I've completed 1 task for the chair, which is to create the sitting board._"

* Pro: Manual commits keep me alert and organized.

  That would avoid a situation like "_I was working on the table before, and I then remembered
  something crucial for the chair. Now, where was I with the table? Wait, where's the chair?_".

  Instead, it could be like "_I'm done with task 1 for the table, and that was 1 commit. I was doing
  task 2 halfway when I remembered something crucial for the chair. Now that I have completed task 1
  for the chair, I'm going back to task 2 for the table_".

* Con: Requires an alert and organized mind.

  Doesn't allow me to "_zombie_" through my work day. You mean I have to actually stay alert
  and know where I am in my WIPs at all times?? I hope you have good staff benefits like a pantry
  stocked with coffee!

Automatic Commits:

* Pro: Saves work-in-progress even for the most lazy and sleepy minds.

* Pro: Allows rapid work in long stretches, especially when on a roll or brainstorm.

* Pro: Useful for early stages of a project, where many easy features are rapidly thrown in with
  high chance of working successfully (easy features).

* Con: Each commit will often hardly make sense, not a coherent or logical unit of change.

# Reflection 4

## Why do you think some version control systems, like Git, allow saving multiple files in one commit, while others, like Google Docs, treat each file separately?

Git was built primarily to track program codes. Program codes are certainly a lot more verbose than
documents containing natural language (holding the amount of work or messages transmitted
constant). Hence, program codes often have to span several files to achieve some level of
organization, so that the codes are manageable and maintainable.

Google Docs deal primarily with documents containing natural language, such as legal document,
thesis, article, and so on. Natural language is more concise than program codes, given that natural
language leverages a lot of implicit rules from societies and cultures for interpretation. Most
documents is comprised of a single file, even when containing hundreds of pages (such as a novel).

Whereas program codes consumed by computers must be precise and consequently quite verbose and
organized over several files, documents consumed by humans need to be in a single file, book or
document. Humans write and read natural languages quickly and efficiently, and should not be
burdened with carrying multiple books or documents containing overly verbose content.

How can you use the commands git log and git diff to view the history of files?

# Reflection 5

## How can you use the commands git log and git diff to view the history of files?

``git log`` lets me go through the entire history of my changes (most recent on top). This ties in
to Reflection 2.

Important side note: Aha! Annotations via _Commit Message_! So I don't have to put my annotations
into the file's contents? That would render all wishlisted benefits for Reflection 2
*wish-granted*! I will be able to annotate all my past idiocy and genius, and have truly continuous
learning throughout my work life!

(TODO: Find out how to do anchors and links in Github-Flavored Markdown. For the link to Reflection
2 above.)

``git diff`` then lets me compare any versions of any file. Great for spotting bugs by
systematically assessing all changes, including intentional and idiotic ones. By comparing any
version with the one right before it, I can see the exact changes made in each version. This ties in
to Reflection 1.

# Reflection 6

## How might using version control make you more confident to make changes that could break something?

Hmm, I've already mentioned this in Reflection 2. I'll read it again to see if there's anything I
can add here.

(TODO: Find out how to do anchors and links in Github-Flavored Markdown. For the link to Reflection
2 above.)

I get more adventurous and more willing to take risks and learn from failures. I actually am already
excited by humiliating and humbling failures to begin with, but I still won't want to bring down
Google's servers for 100s of millions of people if I worked on those servers! Having the ability to
quickly _switch back to a known working state_ within seconds is a very comforting _license_ to
_fail fast, fail cheap, learn fast and work faster_!

Well, I probably will be tasked to work on a _copy_ of Google's servers rather than the ones in live
production. But being able to switch back quickly to a known working state is great for when boss
asks "_so how are things going (and not breaking)?_"!

# Reflection 7

## Now that you have your workspace set up, what do you want to try using Git for?

* Drafting of long legal contracts

  (hey! I can do my own rental agreements now!)

* Writing a novel

  (now I can easily assess whether my novel breaks down if I introduce romance for 3 main
  characters!)

* Writing program codes, of course.

* Tracking my Udacity profile texts.

  (Is the word "_driven_" going to work better than "_energetic_"?)

* Tracking all the different resumes I send to different employers.

  (I can finally remember whether I told a particular employer I was "_ready to sign on_" or
  "_waiting for clarification on info X or Y or Z aspects_"
