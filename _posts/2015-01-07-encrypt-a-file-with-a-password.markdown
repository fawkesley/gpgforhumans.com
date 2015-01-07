---
layout: post
title:  "Encrypt a File With a Password"
date:   2015-01-07 21:31:03
categories: encrypt
---

GPG can use symmetric encryption to protect the contents of a file with a
passphrase (as opposed to asymmetric, public/private key encryption):

{% highlight bash %}

$ gpg --symmetric myfile.zip
$ ls
myfile.zip
myfile.zip.gpg

{% endhighlight %}

This will create a new file `myfile.zip.gpg`, leaving the original `myfile.zip`
intact. Don't forget to delete it if required.
