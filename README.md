#**Finding Lane Lines on the Road** 

[//]: # (Image References)

[image1]: ./test_images_output/gray_solidYellowCurve "Gray"
[image2]: ./test_images_output/gray_blursolidYellowCurve "Gray Blur"
[image3]: ./test_images_output/edges_solidYellowCurve "Edges"
[image4]: ./test_images_output/masked_edges_solidYellowCurve "Masked Edges"
[image5]: ./test_images_output/result_solidYellowCurve.jpg "Result"

* I converted the images to grayscale
* I reduced the noise by using Gaussian Blur. 
* I detected edges with Canny edge detector.
* I created a subset image which contains lane lines.
* I detected lines with using Hough Lines.


![Gray image][image1]
![Gray Blur][image2]
![Edges][image3]
![Masked Edges][image4]
![Result][image5]


### 2. Potential shortcomings with my current pipeline


One potential shortcoming would be what when there is an object or another shape on the road, the accuracy tends to decrease. 

According to conditions of ligth and color of road, lines may be misleading or missing.


### 3. Possible improvements to my pipeline

A possible improvement would be detecting more robust, good filtered lines.

Another potential improvement could be to fitting curve instead of fitting line to represents lane lines.

