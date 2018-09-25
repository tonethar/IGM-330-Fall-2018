# Week 5A - Tuning up our Audio Visualizers

## I. Overview
Today we'll discuss some potential enhancements to our audio visualizer project - [Project 1 - Audio Visualizer](../projects/project-1.md)

## II. Required Reading & Assignments

**Data Viz in General:**
  - https://datavizcatalogue.com
  - https://informationisbeautiful.net/visualizations/what-makes-a-good-data-visualization/
  
**Audio Viz Specifically:**
- https://medium.com/@delu/a-perceptually-meaningful-audio-visualizer-ee72051781bc (some practical tips)
- https://www.awwwards.com/awwwards/collections/web-audio-api-and-adio-visualization/ (really nice examples!)
- https://99designs.com/blog/design-other/sound-visualization-design-inspiration/ (cool, but out there!)


## III. Presentation
- **What makes for an effective audio visualization?**
  - there should be an analogous relationship between the sound data and what people are seeing on the screen - drawing should not be random like our "screen savers" at the beginning on the semester were. Can you instead help your viewer **learn** about sound & music by making new connections, and seeing new patterns, such as:
    - visualizing the "beat"
    - human voices fall into the lower frequencies
    - electronic instruments have a different "shape" than natural instruments
  - have a good "starting state" to your visualization - the controls should be pre-set to where the visualization has a pleasing state when the user first opens it. Here's a good example of this: https://mcs2515.github.io/Magical_Visualizer/#
  - don't bore the user - have the visualization periodically change in major ways, automatically. Here's an example: http://igm.rit.edu/~acjvks/courses/2015-fall/330/demos/p1-demo/web-audio-example.html
  - give the user controls (sliders, check boxes, pull downs) to effect the visualization
- Other tips:
  - on project 1, 

## IV. Demo
- Today's demo, where we add multiple controllable audio effect nodes to a previous demos, is stepped through here: [demo-more-web-audio.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-more-web-audio.md)

## V. Review Questions

### V-A. Web Audio
1. The connections between the audio nodes in the Web Audio API is commonly visualized as a ___________
2. True or False. An *analyser node* modifies the audio data
3. If we request 32 samples from a sound, how many elements will be present in the typed array we get back?
4. Give 3 differences between a typical JS Array created with `[]`, and a JS *typed array* such as a `Uint8Array`
5. Give 3 possible sources for a "source node"
6. What does a "destination node" typically point at?

### V-B. Bitmap Data
1. Suppose your canvas is has dimensions of 500 x 500 pixels. How many elements will be in the *typed array* you get back from `ctx.getImageData(0, 0, canvasWidth, canvasHeight)`
1. Why do we step through the image data array 4 elements at a time?

### V-C. Other
1. What does **IIFE** stand for?
1. What is the primary benefit of using an IIFE in your JS code?




<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-04B-notes.md**](week-04B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-05B-notes.md**](week-05B-notes.md)
