---
layout: post
title:  "Encrypt a File With a Password"
date:   2015-01-07 21:31:03
categories: encrypt
---

To encrypt a file with a password or passphrase, use the `--symmetric` command:

{% highlight bash %}

$ gpg --symmetric myfile.zip
$ ls
myfile.zip
myfile.zip.gpg

{% endhighlight %}

You'll be prompted to enter a passphrase twice, then a new file
`myfile.zip.gpg` will be created.

Don't forget to delete the original `myfile.zip` if required.

## Password Encryption is *Symmetric* Encryption

GPG can encrypt in one of two modes:

  - **symmetric**, using a password to create a key:

    `gpg --symmetric myfile.zip`

  - **asymmetric**, using someone's public key:

    `gpg --encrypt --recipient alice@email.com myfile.zip`
