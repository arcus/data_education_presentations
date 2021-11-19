---
title: Presentation title
theme: night
revealOptions:
  transition: none
  navigationMode: linear
  controlsTutorial: false

---

# First slide

- Point 1
- Point 2

---

## Second slide

> Best quote ever.

Note: speaker notes FTW!

---

# slide3

This slide has no background image.

---

<!-- .slide: data-background="./example_image.jpeg" -->

## slide4

<span id='dark_back'>This one does!</span>

---

<div id="right">

![](media/example_image.jpeg)

</div>

<div id="left">

#### Panda facts

1. Big
2. Soft
3. Slow

</div>

---

![](media/example_image.jpeg)

Notes:
No slide title, just an inserted image

<style>

#left {
    margin: 10px 0 15px 20px;
    float: left;
    text-align: center;
    z-index:-10;
    width:48%;
    font-size: 0.85em;
    line-height: 1.5;
}
#right {
    margin: 10px 0 15px 0;
    float: right;
    text-align: center;
    z-index:-10;
    width:48%;
    font-size: 0.85em;
    line-height: 1.5;
}

#dark_back {
  background-color: rgba(0, 0, 0, 0.7);
  color: #fff;
  padding: 20px;
}

</style>
