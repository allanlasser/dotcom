---
title: How I publish this website
date: 2017-01-26 11:01:22 -0500
tags: reference
---

In order to smooth the procedure of updating my website[^1], I developed a very simple script. It syncs the folder that keeps my website  on my Mac with the [Amazon S3 bucket](https://aws.amazon.com/s3/) that keeps my website in the cloud. Here it is:

```
cd ~/projects/allanlasser.com
~/.rbenv/shims/rake build
/usr/local/bin/s3cmd sync -r _site/ s3://www.allanlasser.com/
```

Here's the breakdown of what's happening:

1. First, my script enters the directory that holds my website files.
2. Since I use [Jekyll](https://jekyllrb.com) to make publishing my website easier, I run [a build command](https://github.com/allanlasser/allanlasser.com/blob/master/Rakefile) that generates the necessary website files for me.
3. I use the [`sync`](http://s3tools.org/s3cmd-sync) command provided by the [`s3cmd`](https://github.com/s3tools/s3cmd) utility to sync the folder with my generated website (`_site`), as well as any folders inside that folder (that's why I use the `-r` flag), with the Amazon S3 bucket that holds my website (`s3://www.allanlasser.com/`).

Finally, I bundled this script into an [Automator Service](https://www.macosxautomation.com/services/index.html) which I can call with a simple keystroke, making the whole process smooth and painless.

[^1]: All in the hopes it will encourage me to update it more often! I'm trying!!!