---
layout: post
title: "web-based image annotation"
---

![image of grid]({{ site.url }}/assets/grid.png)

Allows sub-areas of an image to be manually defined. This is useful for observational-based psychology studies or creating training data for object/scene detection algorithms.

It uses a minimal set of tools: HTML5, PHP, and javascript. As such, it can easily be deployed on any basic web-server.

Users can click squares defined by the grid-overlay to highlight portions of the image. Output includes a list of indices, indicating the set of squares clicked.

Here is an example output file

    #config
    pixel_size,40
    image_width,1280
    image_height,720
    highlight_color,0,255,255
    highlight_transparency,0.5
    randomize_images,0
    line_width,1
    radio_buttons,0
    textbox_label,notes if any
    results_save,1
    savefilename,../results/demo.txt
    confirmation_code,demo
    taskcode,demo
    #selection
    ../images/demo/img_127.jpg,208,209,223,224
    ../images/demo/img_215.jpg,193,211,225,226,229
    ../images/demo/img_3.jpg,137,154,155,172,173
    ../images/demo/img_355.jpg,283,284,285
    ../images/demo/img_537.jpg,185,186,187,203,204
    #end
    #textbox
    ../images/demo/img_127.jpg,horse
    ../images/demo/img_215.jpg,dog
    ../images/demo/img_3.jpg,cat
    ../images/demo/img_355.jpg,barn
    ../images/demo/img_537.jpg,apple
    #end

    
<!--[github/fosterseth]({{ site.github_url }}) for more details.-->



