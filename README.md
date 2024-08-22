# Kidney-Stone-Detection-Using-YOLOv8

This project is basically learned in  Kaggle which is excuted in jupyter notebook.
What is YOLO:
YOLO (You Only Look Once) is an advanced real-time object detection algorithm utilized in computer vision. Its primary capability lies in rapidly and precisely identifying objects within images or video frames. The most recent iteration of this technique is the YOLOv8 network, which proves effective in addressing classification, object detection, and image segmentation challenges.

YOLOv8 in medicine:
YOLOv8 is making a big impact in medicine by quickly spotting things in pictures and videos. This helps doctors find issues faster, which is really useful for diagnosing and treating patients. It can even find tricky things like tumors in X-ray pictures. This helps doctors make decisions faster. YOLOv8 is also good for telemedicine, where doctors can help patients remotely. This shows how YOLOv8 could change healthcare by giving quick and important information. In kidney stone detection, YOLOv8 is showing how it could change healthcare again. It's good at finding kidney stones in pictures and videos, which helps doctors make choices and treat patients faster. It's accurate and helps with telemedicine too. This teamwork between YOLOv8 and kidney stone detection is a big step forward in making patients better with fast and accurate information.

Dataset:
Kidney Stone Images with Bounding Box Annotations
This dataset comprises three main folders: "train," "valid," and "test," each containing "images" and "labels" subfolders. The "images" folder houses the actual image data, while the "labels" folder holds annotations, specifically bounding box information. Additionally, there is a YAML format file provided, streamlining the training process by offering direct compatibility.

The ultralytics package has the YOLO class, used to create neural network models and "yolov8m.pt" is a middle-sized model for object detection.

First_Model with epochs=5.
During the initial execution of this code, you'll encounter a prompt requiring an API key. The message will read: "Paste an API key from your profile and press Enter, or use ctrl+c to exit." Retrieve your API key from your browser by visiting this link: https://wandb.ai/authorize.

What is mAP:
Mean Average Precision (mAP) is a metric used to measure how well object detection algorithms identify and locate objects in images. It combines precision (accuracy of the predictions) and recall (completeness of finding objects) for different object categories. The mAP is the average of the Average Precision (AP) values for each category, giving an overall assessment of the algorithm's performance.

If the achieved mAP after the final epoch is not satisfactory, you have several options for improving the results. You can consider extending the number of epochs and reinitiating the training process. Additionally, experimenting with other parameters such as batch size, initial learning rate (lr0), learning rate range (lrf), or adjusting the optimizer choice could also yield better outcomes. For a comprehensive list of adjustable arguments, refer to the documentation at https://docs.ultralytics.com/modes/train/#resuming-interrupted-trainings

Second_Model with epochs=5 and optimizer='Adam'

Switching the optimizer in Second_Model didn't have a positive impact on the mAP value; instead, it decreased. As a result, We've gone back to using the default optimizer, which is SGD (Stochastic Gradient Descent) and decreased the lr0 value.

Third_Model with epochs=5, and lr0=0.001.

