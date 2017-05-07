---
layout: post
title: "realtime behavior visualization"
categories: misc
---

<video src="{{ site.url }}/assets/movie.mp4" width="320" height="200" controls preload></video>

video is best viewed in fullscreen

The left panel shows coded behavior streams. The color of each rectangle indicates the object looked at during that particular moment in time. The right panel shows a 3d representation of the interaction based on a 3d motion tracking system.

Users can use the Left and Right mouse clicks to set Begin and End points. The tool will playback the interaction during that specific time segment.

The right panel indicates the position of the head and hands of the infant (blue spheres) and parent (pink spheres).

The object positions are not actually tracked. However, exact moments when hands touch objects is manually coded for. Therefore, with the assumption that only hands will move objects, we can use hand xy-positions, plus the hand-to-object coding, to infer the location of objects at any given frame. When objects are let go, we just leave them in the last known xy position, until they are picked back up.