# Face Counter 
AIM – To implement FACE COUNTER in real time using MATLAB.

EQUIPMENTS –
1.	PC with windows(95/98/XP/NT/2000)
2.	MATLAB software
3.	Image Acquisition Toolbox
4.	OS Generic support package for using camera

INTRODUCTION - Face Counter, also called facial detection is an artificial intelligence (AI) based computer technology used to find and identify human faces in digital images. Face counting technology can be applied to various fields including security, biometrics, law enforcement, entertainment, and personal safety to provide surveillance and tracking of people in real time. Thus, this Face Counter using the MATLAB program helps count the number of persons present in a meeting hall or classroom at a time and is very useful.

STEPS INVOLVED – 
Face Detection - For Face detection we have used Viola-Jones algorithm
1.	Install the required Add-ons.

2.	Get Device ID via: info=imaqhwinfo("winvideo").

![image](https://user-images.githubusercontent.com/71866596/207364548-0f750db9-8a53-44d8-92ba-16ed69215cb2.png)

3.	Add the ID to the Code.

4.	Find the Supporting Version.

![image](https://user-images.githubusercontent.com/71866596/207365572-f386c921-21d7-4cdf-bcdf-825da9118194.png)


To detect a face or a particular feature on the faces of people, following steps are used in MATLAB program (testing.m) – 

1.	Define and set up your cascade object detector using the constructor.
detector=vision.CascadeObjectDetector
It creates a system object detector that detects objects using the Viola-Jones algorithm. Its Classification Model property controls the type of object to detect. By default, the detector is configured to detect faces.

2.	Call the step method with the input image I, the cascade object detector object, detector, points PTS and any optional properties. See the syntax below for using the step method. Use the step syntax with input image I, the selected cascade object detector object, and any optional properties to perform detection.
BBOX = step (detector, I)
It returns BBOX, an M-by-4 matrix defining M bounding boxes containing the detected objects. This method performs multi-scale object detection on the input image I. Each row of the output matrix BBOX contains a four-element vector (x, y, width and height) that is specified in pixels, the upper-left corner and size of a bounding box. Input image I must be a grayscale or true color (RGB) image.

3.	insertObjectAnnotation(I, ‘rectangle’, Position, Label)
It inserts rectangles and corresponding labels at the location indicated by the position matrix. The position input must be an M-by-4 matrix, where each row (M) specifies a rectangle as a four-element vector 
(x, y, width, height). The elements x and y indicate the upper-left corner of the rectangle, and the width and height specify the size.


OUPUT –

1.	Run the program (count.m). A graphic user interface will appear.
 ![image](https://user-images.githubusercontent.com/71866596/207364844-d7b584e0-3d79-411c-95f6-a1657f596017.png)

2.	Click on Start Camera button to initialize camera settings.
 ![image](https://user-images.githubusercontent.com/71866596/207364885-beb778d4-b913-4dcb-835d-48d25d2c9ef0.png)

3.	Next click on the Count Face button and the camera will start counting the faces.
 ![image](https://user-images.githubusercontent.com/71866596/207364989-6e2dfcdc-7e85-484f-b749-d89b2c16068e.png)

![image](https://user-images.githubusercontent.com/71866596/207365020-67b10672-0487-458b-bbcb-29b563efdd89.png)
  
![image](https://user-images.githubusercontent.com/71866596/207365051-4cc28a26-ec5a-4959-81eb-92ec18eec431.png)

4.	To stop, click the Stop button.

RESULT – Finally this project helps count the number of faces, such that this system is used for various applications.
