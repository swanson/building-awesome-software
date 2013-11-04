---
subject: "Wishful Thinking"
---

I am a wizard, basically.

I can write code, which means that I can create just about anything (*listen, 
just shut up and let me have this moment, okay?*). That is powerful!

"That is pretty powerful", you might say, "But then how come you sometimes 
write code that looks like this?"

``` ruby
mood_by_dates = @team.moods.group_by { |m| m.date }

dates_with_averages = {}
mood_by_dates.each do |date, mood_by_date|
  moods = mood_by_date.select(&:value).map(&:value)
  dates_with_averages[date] = moods.mean unless moods.empty?
end

data_points = []
dates_with_averages.each do |date, avg|
  data_points << "[Date.UTC(#{date.year}, #{date.month-1}, #{date.day}), #{avg}]"
end

data_points.join(",")
```

Commence hand-waving.

---

I want to talk about a wizard-like technique: **Programming by Wishful
Thinking**. The basic idea is to write code that you wished worked (and then go
make it so).

I think we can all agree that the code snippet above is kind of gross. It's not
the worst thing I've ever seen and it [probably] works. But it isn't easy to
understand without a bit of thinking; you can't glance at it and immediately
know what is going on.

This code is the opposite of wishful thinking. Instead of thinking about the
methods I wish I had, I decided to just "use what I've got".

I think this is a very common approach when you are a newbie (either to software
in general or a new language/framework). You are kind of [MacGyver'ing][mg] your
way through a problem; I've got a hash, a `group_by`, a stick of bubble gum and
I've got to figure out a way to pass this data to a JavaScript charting library!

So what does this code look like if we apply some wishful thinking? Maybe
something like...

``` ruby
mood_avgs_by_date = MoodCalculator.compute_daily_averages(@team.moods)

DailyAverageChart.build_javascript(mood_avgs_by_date)
```

What if I had started with that? If I had pretended that all of these handy and
convenient helpers existed already?

Well, it would be easier to understand what this code was doing when I look at
it 3 weeks later. The implementation may still be kind of confusing, but I have
more context. I don't need to know all of the details on the 
`compute_daily_averages` method to grok what is going on.

There are other benefits, too.

* Easier to write unit tests
* Easier to re-use logic in other places
* Teammates won't strangle me for making them review a mess of spaghetti-code

Programming by Wishful Thinking is one of the biggest things that separates
beginners from more advanced developers. 

But the good news is that it is super easy to learn and apply this skill. You 
can go practice this on the very next piece of code you write.

[mg]: http://fathom.info/macrecipes/











