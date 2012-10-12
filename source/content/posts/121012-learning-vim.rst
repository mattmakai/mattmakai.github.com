Learning Vim - A Colleague's Question
=====================================

:category: post
:date: 2012-10-12
:slug: learning-vim-colleague-question

I received the following question from my colleague this morning:

  Hey buddy, finally taking the plunge to learn VIM because it will make 
  me a lot more productive when working with Puppet manifests.  Any 
  helpful tips you've come across?  I already set up my client with 
  pathogen to allow me to easily use new plugins and I pulled in things 
  like tabular, syntastic and puppet syntax highlighting.  Love to hear 
  anything else you'd recommend.

  Thanks!

I love Vim and I've been using it for about four years as my only editor
when coding in Python, typing up blog posts, or learning new 
programming languages. So here's my recommendation.

It takes awhile to learn VIM but it's amazing once you do. I took the 
Vim cheatsheet (http://www.tuxfiles.org/linuxhelp/vimcheat.html) and 
tried to learn a command each day.

Also, I disabled the use of the arrow keys so I could get used to the "hlkj" movement.

The major logical leap is understanding that Vim is basically a language where you have a command and it can be prefixed by a number to execute it multiple times. For example,

dd <-- cut the line and move it into the "clipboard"

5dd <-- cut 5 lines and move them into the "clipboard"

Definitely start out by 
