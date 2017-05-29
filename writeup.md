# **Finding Lane Lines on the Road** 

[//]: # (Image References)

[image1]: ./test_images_output/gray_solidYellowCurve.jpg "Gray"
[image2]: ./test_images_output/gray_blursolidYellowCurve.jpg "Gray Blur"
[image3]: ./test_images_output/edges_solidYellowCurve.jpg "Edges"
[image4]: ./test_images_output/masked_edges_solidYellowCurve.jpg "Masked Edges"
[image5]: ./test_images_output/result_solidYellowCurve.jpg "Result"

---

### Reflection

### 1. Pipeline and the draw_lines() function.

My pipeline consisted of 5 steps. 
* I converted the images to grayscale
* I reduced the noise by using Gaussian Blur. 
* I detected edges with Canny edge detector.
* I created a subset image which contains lane lines.
* I detected lines with using Hough Lines.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by starting with separateing left and right line according to their slope because slope of left lines should be negative and slope of right lines should be pozitive. After that, I added filter for detecting irrelavent lines. Finally, I fitted two lines as lane lines according to end points of left and right line segments by using least square method.


![Gray image][image1]
![Gray Blur][image2]
![Edges][image3]
![Masked Edges][image4]
![Result][image5]


### 2. Potential shortcomings


One potential shortcoming would be what when there is an object or another shape on the road, the accuracy tends to decrease. 

According to conditions of ligth and color of road, lines may be misleading or missing.


### 3. Possible improvements

A possible improvement would be detecting more robust, good filtered lines.

Another potential improvement could be to fitting curve instead of fitting line to represents lane lines.
