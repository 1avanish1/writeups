Points: 40
Category: Web Exploitation

## Description

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:17781/](http://mercury.picoctf.net:17781/)

## Hints

(None)

## Approach

The link goes to something that looks like this:

![home page](./home.png)

I typed in "snickerdoodle" and entered it.
> I love snickerdoodle cookies!

Ctrl + Shift + I will reveal some things, navigate to storage, then find cookies storage.
I ran burpsuite on this,which kept interacting with the server entering values from 1 to 32,only one of them
had a file size different from others,entering that gave the flag.
