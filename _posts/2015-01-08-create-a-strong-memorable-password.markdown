---
layout: post
title: "Create a Strong Memorable Password"
categories: encryption
---

Buy a dice and make a 6-word [Diceware passphrase](diceware), which
looks like this:

`vita jar elbow admix mike libido`

(77.5 bits of entropy: 30 dice rolls = 6^30 ~= 2^77.5)

## Humans and Computers Aren't Very Random

Humans are terrible at inventing strong passwords for many reasons. We're
also really bad at remembering long sets of random characters.

Computers can generate random data but there are numerous pitfalls and attacks,
making it an area ripe for extensive discussion & research.

**Go old-school**

You can shortcut that entire debate by purchasing a set of die and [following
these instructions](diceware) for generating a Diceware passphrase.

Diceware passphrases are surprisingly memorable compared with random
combinations of letters and numbers having the same number of bits of entropy.

Be sure to read the author's section on number of words, and the sort of
additional security protections each length of passphrase would imply.

## Quick and Dirty

If you're OK with an unmemorable password and you're happy with the limitations
of your computer's entropy sources, you could run the following:

{% highlight bash %}
$ dd if=/dev/urandom bs=1 count=32 2> /dev/null | base64
QSEd54oRBf9PPKxLXbci+0Zqw6DFENGa/in9ITCJG5k=
{% endhighlight %}

The resulting password has 256 bits of "entropy" which cannot be brute-forced
without a significant new discovery such as quantum computing.

[diceware]: http://www.diceware.com

## Passwords vs Passphrases

They're essentially the same thing, except that the word pass*phrase* is a
reminder that *"letmein"* really isn't good enough ;)
