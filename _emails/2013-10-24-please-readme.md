---
subject: "PLEASE_README.md - How to write a good README"
---

Someone said to me the other day: "A README file on GitHub is the best developer marketing
there is." That got me thinking: What popular advice about marketing pages can we apply to 
READMEs?

# Sell Benefits, Not Features

People don't buy stuff because it has 46 great features. They buy stuff that makes their
life easier or helps them to be awesome. I don't care that your project uses a native SAX
parser, I care that it helps me work with XML without flipping a table over.

Take this great example from Kenneth Reitz' Requests library:

```
Requests is an Apache2 Licensed HTTP library, written in Python, for human beings.

Most existing Python modules for sending HTTP requests are extremely verbose and cumbersome. 
Python's builtin urllib2 module provides most of the HTTP capabilities you should need, but the
api is thoroughly broken. It requires an enormous amount of work (even method overrides) to 
perform the simplest of tasks.
```

Three sentences in and it is already clear why you want to use Requests over the 
Python standard library.

# Social Proof

Whether you want to call it [social proof][sp], the [halo effect][hl], or [positive framing][pf], 
when you position your product as something that other people value, my perception changes.
Oh, this is used by Amazon? They are a big company full of smart people, I should use it to!

The open-source equivalent of the typical [lineup of logos][logos] are README badges.

!["README Badges"](http://mdswanson.com/static/stinger_badges.png)

Badges can signal to the "buyer" that the author cares about [code quality][cc], that 
[solid engineering practices][tr] are used, that this library has 
[been around the block a few times][fr], or that your community is a [friendly bunch][fb].

Something that I've seen pop up a few times recently is to add "customer testimonials". This
is straight out of the marketing playbook, but I could see this becoming a way to supplement
traditional metrics on GitHub (stars/forks). Below is an example from [Nathan Kontny][nk].

!["Customer Testimonials in a README"](http://mdswanson.com/static/n8_readme.png)

# Call to Action

In a typical marketing context, your CTA is usually "BUY THIS THING!!". For an open-source
project, the two major actions you want to promote are: install/use this code or contribute
to this project.

So make sure you have clear instructions for both. Try to follow your communities preferred
method of installation and automate whatever you can. The time it takes to provide a VM image
of a tricky setup will be worth it to not have to help troubleshoot strange configurations.

Check out this [slick demo of RethinkDB][rt] - hit a button and it launches you a sample
instance of the database using Docker. I don't think we are too far away from seeing this
kind of functionality pop up all over GitHub.

---

I'm sure there are some hardcore developers out there that are super pissed off that so
much of open source (at least on GitHub) is about marketing and less about things like
quality and reliability. I think that, ultimately, a great library is like a great product &mdash;
all the marketing in the world can't make up for an offering that sucks.

Just remember that you can have the world's greatest library, but if no one is using it
or knows about it...well, you don't have anything, really.

---

Seen any cool READMEs lately? Disgruntled marketer that wants to yell at me for comparing
your field to a 12kb Markdown file? Hit the reply button and let me know :)


[sp]: http://en.wikipedia.org/wiki/Social_proof
[hl]: http://en.wikipedia.org/wiki/Halo_effect
[pf]: http://en.wikipedia.org/wiki/Framing_effect_(psychology)
[logos]: http://herearesomelogos.tumblr.com/
[cc]: https://codeclimate.com
[tr]: https://travis-ci.org/
[fr]: http://badge.fury.io/
[fb]: https://waffle.io/
[nk]: https://github.com/n8
[rt]: http://tryrethink.info/