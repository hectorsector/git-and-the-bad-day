I did some late-night committing. And I thought everything was fine.

And when I got out of bed, I spilled my morning coffee and by mistake I started a software update on my machine which bricked it for most of the morning. When I finally logged on I realized I committed directly to master part of this story I didn't want, so I could tell it was going to be a terrible, horrible, no good, very bad day.

So I decided to do some `git bisect` because on any other day it would probably help me find which commit broke my story. Besides, my friends Matt and Eric always found their bugs with `git bisect`.

My most recent commit was obviously bad.

And I don't even remember the last time I looked at my story, so I figured only the first commit was safe.

It took a couple of tries, but soon enough I found that contained the offending line. But when I reverted the commit, I got a merge conflict!

When Matt used `bisect` he reverted a missing semicolon, a misspelled variable name, and a pretty alarming lack of comments.

When Eric used `bisect` he reverted some missing environment variables, some badly indented blocks, and part of his grocery list that got accidentally pasted into his code.

When I used `bisect`, I just got a gnarly merge conflict.

After breakfast, Briana got to teach her favorite group of students. Cynthia spent some time watching trains with her son. I was stuck trying to figure out how to resolve my merge conflict. When I complained, no one even responded.

I could tell it was going to be a terrible, horrible, no good, very bad day.

Before lunch, I treated the conflict as any other conflict. I opened the file, and removed the conflict markers. Then was wondering how to finish my revert.

`git revert` didn't work

`git commit` didn't work

I wish I could revert this day.

Once the revert was finished, I realized I should've done it in its own branch. I wanted to `git reset` this terrible, horrible, no good, very bad day!

That's what it was, because that afternoon I actually tried `git reset`. My commit was made to the wrong branch, so I figured I'd create a new branch, then reset to the the previous commit, and when I switched to the new branch my revert was there!

I then realized a `git cherry-pick` would've done the same thing for me.

I wished I could cherry-pick myself out of this day.

Later that night, I realized I uploaded my Keynote presentation binary to the repo. What a waste of space!

I figured I could just revert the commit, but that just means that any previous commits would still have the file. This was a terrible, horrible, no good, very bad day.

Because each commit is a complete snapshot of the codebase, and I had no idea when I committed the binary, I knew this would be a messy clean-up. But `git filter-branch` should help me get out of this mess.

But before bed I decided to give it another shot. I was successful with `git filter-branch` I was happy with myself, but then I realized a local backup of what I cleaned up was still in my local git directory.

I pushed my changes up to GitHub, and my push was rejected. It's because I altered commit history so I had to force push. Cynthia then told me that GitHub caches commits that may still have my credentials. So I had to contact Support and they removed the cached commits from GitHub.
