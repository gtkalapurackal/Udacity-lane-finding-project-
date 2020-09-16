# Udacity-lane-finding-project-


Goal: 
Finding lane lines in the images and the videos provided marking it on the go 

Pipeline : 
Loading the image and take a look on the input size and shape , next thing is to convert it to gray scale from RGB image for easy processing , apply on it a Gaussian smoothening with kernel size of 5 or less as preferred to remove the noises in the images , on it apply the canny function provided by the Pipeline : loading the image and understanding the input size and shape , next thing is to convert it to gray scale from RGB image for easy processing .Apply on it a Gaussian smoothening with kernel size of 5 or less as preferred to remove the noises in the image, on it apply the canny function provided by the CV2 to find the brightness gradient in the image represented as bright dots .Now we crop out the region of our interest ,take  note of the polygon points in the image where the lane lines tentatively contained, from  the canny output image by masking the other areas . On this output apply the Hough transform to find the best fit lines, now we will get lot of lines which is a best fit to make out a sing left and right lane we will average out all the lines which is left sloped and right sloped and draw the left averaged lane and right averaged lane on the output image then we will extrapolate it on to the original image. Now we get both left and right lane marked. 

Shortcomings:
Right and left lane is drawn on the road image and videos.

Opportunity:
Lines are identified but when coming to curves it is not perfectly marked for this we have analyze the image segment by segment and extrapolate
