---
layout: post
title: RogueWriter, A DIY distraction-free writing device
categories: [technology, writing]
---
<meta name="twitter:image" content="{{ site.baseurl }}/images/posts/rw_three_v02.png">k

It's a writer's dream. Or maybe it's just an obsession.

Oh, for the days when writers would bang out fiction on a
well-oiled, clackity-clackity mechanical typewriter. I love a good typewriter, but I love the advantages 
of a computer, too. The problem is that more and more we associate computers with 
distraction, social interaction, and media of all types. So for me, the computer 
is less a machine for writing fiction than it is a machine for distraction. 

Wouldn't it be great if we had a machine with the single purpose of a typewriter, and some of the benefits that a computing device has?

There are a lot of different at such a device, including the
[freewrite](https://getfreewrite.com/products/freewrite-smart-typewriter), the
[alphasmart](https://en.wikipedia.org/wiki/AlphaSmart), and [
raspberry pi](https://en.wikipedia.org/wiki/Raspberry_Pi)-based devices like 
[this](https://www.reddit.com/r/raspberry_pi/comments/7e4n2n/my_portable_distractionfree_writing_machine/),
and
[this](https://www.hackster.io/news/scripto-is-a-distraction-free-raspberry-pi-powered-writing-device-65916a3e5bb7)
and
[this](https://spectrum.ieee.org/geek-life/hands-on/write-without-distraction-with-this-diy-eink-typewriter).
Like I said, this can be an obsession.

## RogueWriter

![three]({{ site.baseurl }}/images/posts/rw_three_v02.png)

So here's my addition to this bestiary of devices ...

**RogueWriter** is a portable device with a keyboard and display that makes it easy to write, without all the distractions 
a full laptop can offer. It is also, importantly, *easy to assemble*, requiring
no soldering, case cutting, 3D printing or other finicky stuff. The parts can be
plugged together, taped in place, and you're done.

The **RougeWriter** is:

- portable
- battery-powered
- wireless- and bluetooth-enabled, and
- inexpensive
- a bit wonky, like a clacky old typewriter. 

Importantly, you won't be embarrassed to been with it out in the wild.
In fact, the visual design of this thing is important, and it drives some of 
the purchasing decisions. 

My version of this device boots to a text display (a bash shell, to be specific), ready for writing.
The workflow I use is discussed in a later post, and is one possible workflow
among many.

So let's go ... 

## Buy The Parts

First you have to buy the parts. Let's lay this thing out and take a look at the guts. 
It's basically **display (plugged into a) computer (plugged into a) battery**,
with a **bluetooth keyboard**. Once you plug these things
together, you have a pretty powerful computer for about **$150**:

![guts]({{ site.baseurl }}/images/posts/rw_diagram_v02.png)

1. [**Computer. ($14)**](https://www.adafruit.com/product/3708) This design uses
the **Raspberry Pi W**, a small, low-power computer that has both wifi and
bluetooth on board. We'll use a **Pi W** with pre-soldered header pins, so you
can plug in the specified display. To get the **Pi** up and running, you'll need
a memory card with the [OS pre-installed](https://www.adafruit.com/product/3259), 
or you can [install it yourself](https://www.raspberrypi.org/downloads/noobs/). 
2. [**Display. ($49)**](https://www.amazon.com/gp/product/B0716RVNTS)
The display is important. I've seen a lot of designs using small displays, and they typically have
cables and plugs sticking out of them. To me that would be distracting. I chose
a display that lays flat and has a ribbon connection, which is visually much cleaner.
3. **Keyboard. ($55)** Buyer's choice here. There are lots of options for
bluetooth keyboards, and you can make your own choices on portability, feel,
size, etc. The most important thing is whether or not the keyboard robustly
connects to the **Pi** through power cycles. Some keyboards just don't do it.
I haven't found a cheap bluetooth keyboard that works well, but YMMV.
    - Here's my current [favorite keyboard](https://www.amazon.com/gp/product/B019PIXO78).
      It's portable, and when unfolded it's a nice size and the layout is great for touch typing. 
      It holds a good charge, and turns on/off as the keyboard is opened/closed. Nice product.
4. **Battery. ($18)** Your choice, based on price, battery life, form factor,
etc. A lot of different batteries will work, and I always have an eye out for
a smaller battery pack on sale. You have to make a tradeoff between size, price,
and battery life. There's a post on that.
    - [Here's the one that I'm using now](https://www.amazon.com/gp/product/B07QXZ6DJL). 
      Preliminary [testing](https://www.amazon.com/gp/product/B013FANC9W) 
      shows this should last for **9 hours**. More detailed testing on the way.
5. [**USB on/off
switch**](https://www.amazon.com/gp/product/B07CTHKXDW).
    Keeps the battery from draining after shutting down the **Pi**.
6. [**USB right angle
adapter**](https://www.amazon.com/gp/product/B01C6031MA).
You may not need this, but for my arrangement of parts,
I used one for access to the **Pi**'s USB
connector. This lets me plug in a mouse for software fixes if that's needed. In this design, the adapter is hidden beneath the fold in the display's ribbon cable, but just barely pokes out on the left side.
7. [**USB A to B adapter**](https://www.amazon.com/gp/product/B001K9BEJ6).
Connects the battery to the on/off switch cable.

### Other Parts

- A really cool cigar case. Mine measures 7 1/4"w,5 5/8"d,1 5/8"h. The wood is 
  about 3/16" thick. The case is important, as it sets the parameters of the
  final device. Don't obsess too long about it, though, as you can always take
  these parts and put them into a new, cooler case. In fact, you might say that
  that's kind of the point of this whole thing - getting the guts together and
  getting your workflow going, and then futzing around by keeping an eye out for
  the perfect case.
- Double stick tape and velcro. This holds things together well enough to keep
  everything in place, but it can be repositioned if you need to change things. I ended up using 
  double stick tape for the display, the `pi`, the switch, and cables. Sometimes
  you need to use two layers of tape to position the component properly (like the
  screen). I used
  velcro to keep the battery in place, because it's the one thing you need to
  remove from time to time. Being able to remove it means you don't need to 
  monkey around with holes in the cigar box (I think these always look crappy),
  and you can just pull it out to recharge it. Simple.
- Small bit of lighting chain, and two screws to keep the lid in place. You
  may not need this, if your cigar box has some nifty hinges that stay open.
- Tools. All I needed was an x-acto knife to cut the double sided tape, and the cardboard cover.

## Connect the Pieces, and Tape Them in Place 

It's important that you let go of making this some futzy, crazy, perfect thing.
Some tape and bubble gum keeping it together is a good thing. As long as you
have a cool cigar box, you're good.

1. Assemble the guts of the device (computer, display, battery).
2. Plug them together to make sure it all works. This includes installing the OS for the **Pi**. If you've bought the [pre-installed OS](https://www.adafruit.com/product/3259), just plug the card in, and turn it on. The computer will boot to a desktop.
3. Find a nice way to fit everything into your case, and lightly double stick tape the components in place. This will take some trial and error, but since you're not soldering or gluing, it's pretty easy to fit things in. Once you have things settled in, you can velcro the battery in place, and more permanently tape everything in place.

## OS/Software

Now that you have a **RogueWriter** up and running, you have a choice. What workflow
do you want to support? We'll cover some options in the next post.
