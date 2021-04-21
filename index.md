title: An brief Introduction to Nodeppt
speaker: Fei Ye
plugins:
    - echarts
    - KaTeX

<slide class="bg-primary bg-gradient-v  aligncenter">

# An brief Introduction to Nodeppt {.text-landing.text-shadow}

By Fei Ye {.text-intro}

[:fa-github: Github](https://github.com/fyemath/nodeppt-demo){.button.ghost}

<slide class="bg-blue">

## What is nodeppt

- A html slide creator

- Build in js

- Based on webslides、webpack、markdown-it and posthtml

<slide class="bg-blue">

## Install

```
npm install -g nodeppt
```

<slide class="bg-blue">

## Basic Usage

### New, Preview and Build

```
# create a new slide with an official template
$ nodeppt new slide.md

# start local sever to preview slide
$ nodeppt serve slide.md

# build a slide using the default output dir
$ nodeppt build slide.md

# build a slide using customized output dir
$ nodeppt build -d dirname slide.md
```

### Help

```
# help
nodeppt -h
# serve help
nodeppt serve -h
```

<slide class="bg-blue">

## Presenting Usage

### Presenter mode  

To open the presenter mode, add `?mode=speaker` after the url.

### Keyboard Shortcuts

- Page: ↑/↓/←/→ Space Home End
- Fullscreen: F
- Overview: -/+
- Speaker Note: N
- Grid Background: Enter

<slide class="bg-blue">

## Composing Slides

Nodeppt uses markdonw syntax and `<slides>` to break the file into individual slide.

One can figure the slides in the top part using yaml language. For example,

```yaml
title: nodeppt markdown demo
speaker: 三水清
url: https://github.com/ksky521/nodeppt
js:
    - https://www.echartsjs.com/asset/theme/shine.js
prismTheme: solarizedlight
plugins:
    - echarts
    - katex
```

<slide class="bg-blue">

## Slide Configuration - Syntax

- Nodeppt recognize each `<slide>` as a new slide indicator and uses it to layout the whole markdown file into slides.

- Slide style can be configured by adding tags to `<slide>`.

- Supported tags includes\:
  - `class/style`
  - `image="img_url"`
    for slides background
  - `video="video_src1,video_src2"`
    for slides background video
  - `:class`
    add class to the wrapper.

<slide class="bg-blue">

## Slide Configuration - Example

```
  <slide image="https://source.unsplash.com/UJbHNoVPZW0/">
  <!-- adding a background image -->

  <slide image="https://source.unsplash.com/UJbHNoVPZW0/ .dark">
  <!-- adding a background image and a dark layer -->
```

- For available classes, please see [ksky521/nodeppt/site/classes.md](https://github.com/ksky521/nodeppt/blob/master/site/classes.md) on github.
