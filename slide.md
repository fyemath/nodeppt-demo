title: Intro to Nodeppt
speaker: Fei
plugins:
    - echarts

<slide class="bg-primary bg-gradient-v  aligncenter">

# Intro to Nodeppt {.text-landing.text-shadow}

By Fei {.text-intro}

<!-- [:fa-github: Github](https://github.com/ksky521/nodeppt){.button.ghost} -->

<slide class="bg-light">

## Install

```
npm install -g nodeppt
```

<slide class="bg-light">

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

<slide class="bg-light">

## Presenting Usage

### Presenter mode  

To open the presenter mode, add `?mode=speaker` after the url.

### Keyboard Shortcuts

- Page: ↑/↓/←/→ Space Home End
- Fullscreen: F
- Overview: -/+
- Speaker Note: N
- Grid Background: Enter

<slide class="bg-light">

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

<slide class="bg-light">

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

<slide class="bg-light">

## Slide Configuration - Example

```
  <slide image="https://source.unsplash.com/UJbHNoVPZW0/">
  <!-- adding a background image -->

  <slide image="https://source.unsplash.com/UJbHNoVPZW0/ .dark">
  <!-- adding a background image and a dark layer -->
```

- For available classes, please see [ksky521/nodeppt/site/classes.md](https://github.com/ksky521/nodeppt/blob/master/site/classes.md) on github.
