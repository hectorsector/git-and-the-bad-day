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
