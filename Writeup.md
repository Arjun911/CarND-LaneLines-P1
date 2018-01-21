# **Finding Lane Lines on the Road** 



### 1. Pipeline for finding lane lines on the road

My pipeline consists of following steps
 
a) Apply Color Thresholds

b) Canny edge detection 
  
c) Masking the region

d) Apply Hough Transform to identify line segments

    1) Classify the lines into left and right lanes based on the points. 

    2) Determine the equation of line for left lane and right lane using opencv polyfit method.
       This gives us average/mean slope of both lanes.

    3) Extrapolate the line segments to  bottom of the image using the line equation

    4) Identify the top most line segment of either lanes and extrapolate both lanes to top most point

### 2. Potential shortcomings with your current pipeline

Not effective during sharp turns or steep curves

When there are shaded patches, lanes might not be identified

### 3. Suggest possible improvements to your pipeline

One possible improvement would be to consider other color spaces other than RGB and GRAY

Another potential improvement could be to consider line slope from previous frame and compare it with the present frame when the present frame slope is not accurate