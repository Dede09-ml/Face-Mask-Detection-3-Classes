# Face-Mask-Detection

I got this dataset from https://www.kaggle.com/andrewmvd/face-mask-detection. Face mask detection contains 2 folder (annotations and images). Annotation folder contains every coordinates or boundingbox for each images (with mask, without mask, and mask weared incorrect). Images folder contains 853 pictures where each pictures show person with mask, without mask, mask weared incorrect, or mixing of them. 


So, First thing i did is read every images and xml files. after that, from coordinate (bounding box xmin, xmax, ymin, ymax) in xml files, i cropped images and save them to my google drive. 
you can see the code https://github.com/Dede09-ml/Face-Mask-Detection/blob/main/Cropping_Pictures.ipynb


Then, i tried again to read cropped images in my drive directories. Preprocessing and train model with 3 ways; Baseline with image augmentation, MobileNetV2 with image augmentation, and Baseline without image augmentation. After train model, i save each model to my directories (you can save model to /content/ on google colab and download it manually)
you can see the code https://github.com/Dede09-ml/Face-Mask-Detection/blob/main/Training_model.ipynb


I got train model, and ready to try this detection model on webcam. you can't run this code on google colab because colab is not support it. So, use python IDLE to run this code. You need this file; deploy.prototxt and res10_300x300_ssd_iter_140000.caffemodel. Make one directory of all your files include .py file and model.
you can see the code https://github.com/Dede09-ml/Face-Mask-Detection/blob/main/detect_mask_fix.py
Run it, and wait until your webcam show.

Notes : i this code on google colab except when implemented code to webcam or real time detection.
Very thankful for https://www.pyimagesearch.com/ and https://www.kaggle.com/andrewmvd/face-mask-detection. (My reference to build this code) 
