---
subject: "The trouble with timestamps"
---

*This tweet was sent about 2 hours ago.*

*You ordered this item about a week ago.*

*This file was last modified about 4 years ago.*

The pretty "time ago" format has become popular on the web.

And it's good...until it isn't.

There are certain types of data where the pretty format is fine. It originally
came out of social networks, where the content was very time-sensitive. After
a couple of days, the content would be stale and no one would be looking at it
anyways.

But what about `git` commits? What if I needed to see exactly when a change was
introduced into my code? The bug report was entered on October 04, have we
fixed it already?

!["GitHub time ago"](http://i.imgur.com/Iz7yIMC.png)

A month ago doesn't really tell me a whole lot.

!["GitHub full timestamp on hover"](http://i.imgur.com/HqkrfWq.png)

(ProTip&trade;: you can hover over dates on GitHub to see the full timestamp)

---

Think about the context &mdash; most people don't refer to status updates based
on specific times or dates. But I'm sure you've definitely looked at your source
control history to see if a fix was applied in your release last Wednesday.

What are the common use-cases for timestamped data in your app? Do users want
a rough estimate or an exact value? Is the data short-lived or an important
reference point?

The "time ago" style is prettier, but it isn't always the most functional.