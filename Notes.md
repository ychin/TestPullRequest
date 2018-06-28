# Comparisons

Below are comparisons of the 4 main Git repository hosts (Visual Studio Online, Gitlab, Github, Bitbucket) and see how they compare in different use cases and what functionalities they provide.

## Record pushes

VSTS: Explicit feature
Gitlab: Sort of hidden under "Activities"
Github / Bitbucket: None

## Search by author in commits
VSTS: Yes
Gitlab: No
Github: No
Bitbucket: No

## Comparing revisions

VSTS: Each file has a "History" and "Compare" tab to compare different revisions. History allows filtering by author/etc just like regular commits browsing. Neat.
GitLab: Each file only "history". *But* it has a generic "Compare" page to compare any arbitrary commits so if you can still get file revision diffs, just more work and have to filter thorugh the diff for your file.
Bitbucket: Nice per-file history that allows arbitrary commit diffing of the file.
Github: Only per-file history… Lame

## Pull request - recognizing pushes

VSTS:
  - Individual pushes are well organized as "updates".
  - Can see each update's change compared to previous one.
      - Smart enough to not show unrelated added files that got added in master commit and put pulled in via rebase.
      - *Cannot* diff different arbitrary updates against each other.
  - File organization via left sidebar. Clearer to navigate.
  - Under each file you can also go to compare individial revisions like regular file browsing so you can group together a list of commits and see their aggregate diff, which Gitlab can't do.

Gitlab:
  - Recognizes updates, and show in activities, but not organized separately like VSTS.
  - Can see each update's changes and can even diff arbitrary different updates against each other.
      - Added unrelated files *will* show up when comparing different updates which sucks.
  - File organization is through unified list with a search box which I find more cluttered and harder to use in large PR.

Bitbucket: Sort of upderstands pushes, but not really.

Github: Doesn't make updates explicit.
  - Does provide ability to see a file's diffs with a selected range of commits (not updates).

Gitlab is arguably the best, but even so, I still wish there is a "diff the diff" optino to simply see if a rebase operation has actually changed anything to the actual commit change.

## Pull request - commenting system

VSTS
  - Leave comments and can resolve/close/won't fix.
  - Front page sees all issues, and each file will show you as well. Clean and neat.
  - Markdown.

Gitlab
  - Can comment and leave open discussions that need to be resolved. UI doesn't give filtering capabilities though so could be hard to find in dozens of discussions.
  - Markdown.

Github
  - Actually decent. You need to officially "start a review", and leave comments on different parts. Then you can approve the review or send back for rework.
  - The UI also remembers your last reviewed location and can show you only updated code since then, similar to how Code Collab works which is pretty useful for large / long reviews. Also this provides a centralized place to see yay or nay on a PR.
  - Markdown.

Bitbucket
  - Just comments, and can make "tasks" which is ok, not great.
  - Also comments are not in Markdown.

Github is actually quite good on this, especially with the explicit review state and the ability to remember your last reviewed commit so as to only show you need diffs next time.

## Search within files

Github: Search works

Gitlab: Search works (filename or content both fine)

Bitbucket: No

VSTS: Surprisingly, no.

# General thoughts

Surprised how Github actually kind of sucks and not that much better than Bitbucket.
Gitlab comes out looking good with some neat features. In general I actually still prefer VSTS which is a lot more feature-rich.
