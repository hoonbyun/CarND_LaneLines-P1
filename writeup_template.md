#**Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[solidWhiteCurve]: ./solidWhiteCurve.jpg
[solidWhiteRight]: ./solidWhiteRight.jpg
[solidYellowCurve]: ./solidYellowCurve.jpg
[solidYellowCurve2]: ./solidYellowCurve2.jpg
[solidYellowLeft]: ./solidYellowLeft.jpg
[whiteCarLaneSwitch]: ./whiteCarLaneSwitch.jpg

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps
Open image with grayscale
Smooth image with gaussian blur
Edge detection wth canny method
Mask the region of the image to cut interesting part only
Run hough line detection
Combine original image and the output lines from the above step 

To extend lines, I modified the helper function “draw_lines()”, what is doing
Compute slop for each candidate line to classify if slop is negative, the line belongs to the left line otherwise it belongs to the right line, then compute an average of the slop and the offset (ax+b = y) for each lane line, then draw the solid line crossing the min and max edges.

* solidWhiteCurve
![][solidWhiteCurve]
* solidWhiteRight
![][solidWhiteRight]
* solidYellowCurve
![][solidYellowCurve]
* solidYellowCurve2
![][solidYellowCurve2]
* solidYellowLeft
![][solidYellowLeft]
* whiteCarLaneSwitch
![][whiteCarLaneSwitch]


###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


###3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
