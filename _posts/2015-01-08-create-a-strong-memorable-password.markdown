---
layout: post
title: "Create a Strong Memorable Password"
categories: encryption
---

Humans are terrible at coming up with strong passwords for many reasons. We're
also really bad at remembering long sets of random characters.

**In short, don't try.**

Buy a set of die and [follow these instructions](diceware) for generating a
 Diceware passphrase. You'll create something like this:

`vita jar elbow admix mike libido`

... which is surprisingly simple to remember, given the large amount of entropy
(randomness) it contains.

## Quick and Dirty

If you don't need it to be memorable and you don't care that your computer's
randomness is significantly worse than a dice, you could run the following:

{% highlight bash %}
$ openssl rand -base64 30
ZrTc8OKJpb2YY+yD3t0Zrd31K+j38MCBCdUZWgJ8
{% endhighlight %}

[diceware]: http://www.diceware.com

## Passwords vs Passphrases

They're essentially the same thing, except that a pass*phrase* is an reminder
that *"letmein"* really isn't good enough.
