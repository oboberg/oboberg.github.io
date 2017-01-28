+++
title = "odi-tools"
math = false
summary = "A pipeline for the One Degree Imager(ODI)"
date = "2017-01-27T09:42:30-08:00"
tags = ["software"]
highlight = true
external_link = ""
image = "m53_rgb.jpeg"
image_preview = "m53_rgb.jpeg"

+++

The [One Degree Imager (ODI)](http://www.wiyn.org/ODI/index.html) is a
relatively new instrument on the [WIYN 3.5-meter](https://www.noao.edu/wiyn/)
telescope at the Kitt Peak National Observatory (KPNO). In its current
configuration, the ODI focal plane is made up of 30 individual
[orthogonal transfer array (OTA)](http://www.wiyn.org/graphics/ODILayout5x6.jpg)
CCDs covering approximately a degree on the diagonal. The raw data taken
on ODI are stored and reduced on the
[ODI Pipeline, Portal, and Archive (PPA)](https://portal.odi.iu.edu/index/front)
using a Python based pipeline called
[QuickReduce](http://members.galev.org/rkotulla/research/podi-pipeline/).

To cover the gaps between the 30 OTAs, as well as the gaps internal to each OTA,
a single ODI field typically requires a 9 point dither pattern. This essentially
results in 270 individual images that have to be combined into the final
stacked image. Working with another graduate student at Indiana University,
[Bill Janesh](http://bjanesh.github.io/), we developed a Python pipeline called
**odi-tools** to reproject, align, scale, and stack ODI images. The image shown
at the top of this this page is a portion of and ODI field stacked using
**odi-tools**. The object in this image is the globular cluster M 53. By using
the Gaia DR1, we are able to determine a very precise WCS solution for all of
the OTAs that go into a stack images. This was crucial for being able to stack
crowded fields like the one shown in M 53.

The code for **odi-tools** is completely open source and hosted on
[GitHub](https://bjanesh.github.io/odi-tools/). There is also full
Read The Docs style documentation available
[here](http://odi-tools.readthedocs.io/en/latest/).
