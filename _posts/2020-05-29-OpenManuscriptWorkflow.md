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

So, in a file browser, a novel would look like this:

```
    novelname/          (directory)
        author.json     (information about the author)
        manuscript.json (information about chapters)
        scenes/         (directory)
            001.md      (a scene text file)
            002.md      (a scene text file)
            003.md      (a scene text file)
            ...
```

To write a scene, you just edit some file, and make sure to save it in the
`scenes/` directory. Then you edit the `manuscript.json` file to show where the
chapter fits in the manuscript.

So you edit along like this, and then when you want to give someone a manuscript
in Microsoft Word format, or if you want to see the manuscript for yourself, you
need a tool to do that
