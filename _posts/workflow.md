---
layout: post
title: OpenManuscript Workflow
categories: [technology, writing]
image: /images/posts/rw_three_v02.png
---

By profession and passion, I'm a computer programmer, which means I have a very
specific relationship with computers, text, and data. I have a favorite text
editor that I've used for a long time ([vim](https://www.vim.org/)), and my
fingers are so used to typing with this program that it's a true pain for me to
write in something like Microsoft Word. I could go on and on about the beauty of
a simple text editor, but maybe you've already started using  

Instead, I write manuscripts as a set of text-only files that can be edited by
almost anything. This separation of data (the text) from formatting (for
example, a fiction manuscript [format](https://www.shunn.net/format/classic)) is
a very powerful way of maintaining flexibility. 

## The search for simplicity

If you've written fiction for any length of time, you've run into a couple of
things related to software:

- Your current writing tool sucks. It truly blows, and is an impediment to 
  keeping you in the flow of writing or editing. You know what I'm talking
  about.
- When you get right down to it, you are forced to use Microsoft Word files,
  because that's what editor, agents and everyone else wants. So no matter what
  you do, you have to eventually wind up with a Word file. But that doesn't mean
  you have to start there. Instead, you only have to *end* there. Along the way,
  you can do anything you'd like. 
- Your current tool makes seemingly simple things (like switching the order of 
  scenes or chapters) difficult, and generally takes more mental effort than 
  you'd like.
- Old files that you edited with something (like Microsoft Word, for example),
  no longer work with the current software, and need to be updated.
- Maybe that favorite writing tool you used five years ago is no longer being
  supported. That crazy internet company went out of business, and you can't get
  the new version for your whatever-you-use-now machine.

## Manage Simple Stuff

A manuscript is, at a high level, a way of organizing scenes into chapters, 
and putting those chapters in a particular order. 

In computer science, it's often a good idea to *abstract* data from the products
that make it up. That's the entire idea behind *markup languages* that include
some information about how to show the text right along with the text. The
current systems for writing things like this are based on *markdown*,
a specification that was written by (someone).


```
    novel/
        author.json
        manuscript.json
        scenes/
            001.md
            002.md
            003.md
            ...
```


