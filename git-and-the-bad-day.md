I did some late-night committing. And I thought everything was fine.

And when I got out of bed, I spilled my morning coffee and by mistake I started a software update on my machine which bricked it for most of the morning. When I finally logged on I realized I committed directly to master part of this story I didn't want, so I could tell it was going to be a terrible, horrible, no good, very bad day.

So I decided to do some `git bisect` because on any other day it would probably help me find which commit broke my story. Besides, my friends Matt and Eric always found their bugs with `git bisect`.

My most recent commit was obviously bad.

And I don't even remember the last time I looked at my story, so I figured only the first commit was safe.
