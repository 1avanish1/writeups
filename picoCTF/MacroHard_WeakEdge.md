# MacroHard WeakEdge
basic premise is that a ppt file is a zip file of images,
so binwalk gives us a bunch of files.
Being clueless,I navigated around the different extracted folders,
under ppt>slideMasters i found a file called "hidden",and opening 
that gave me,
```
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q
  ```
which is just base64 encoded data,with that we get the flag.
What  i could have done for questions involving PPT's is:
grep -r pico (find recursively) for things like "pico" or "{" except none of it was useful. I tried find -D tree|grep flag in hopes of finding a flag file
which also didn't work. Eventually after some guessing I tried find -D tree|grep hidden which returned:
```python
s = s.split(" ")
print("".join(s))


```
this is a python code which will remove the gaps between the base64.
