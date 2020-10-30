##Gruppe G: What should I glue? 
(Jakob Lobmeyer, Sebastian Rabe, Melchior Schilewa)


	"For an AR Assistant Application for adhesive testing, it is 
	necessary to detect and track pieces for gluing in the camera 
	image. Your task is to implement the detection of such pieces
	in preprared images and video material."

Goal: 
Implementation of an application that should be able to detect, mark (display some additional informations, what steps should be taken to complete the test) and track test pieces as well as determine if glue/adhesive has been applied or other interactions occured (dropped test piece...).  Since this apllication is for adhesive testing it is performed in a controlled environment and we can focus on specific testing setups (fixed size and shape of the test pieces...). 


detect
(
- Motion Detection (simple, but might work in laboratory like environment)
- (Sobel) Edge Detection (the test pieces have distinct edges)
- adaptive Threshholding (might help with reflective surfaces)

ML
- HOG + Linear SVM (difficult to run in real-time), 
- Haar cascade (difficult to find the right params, scale and neighbors => missing objs or slow and possible false positives)
- bag of visual words
- CNNs (RCnn, Fast/Faster RCNN)
- YOLO (v1-3)
- SSD
- RetinaNet
)

track
(
- centroid 
- MIL
- KCF
)