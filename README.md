# Real-time Car Plate Detection And Recognition

![Video](output_video.mp4)


### Project
  building a real-time car plate detection and recognition.
  
### Intuition
  let's split the problem into 3 parts
  1. Car Plate Detection: Using computer vision algorithms and techniques such as YOLO (You Only Look Once) to detect and draw bounding boxes around license plates.
  2. Crop the image around the license plate.
  3. Character Recognition: Build a character recognition Model to recognize the characters on the license plate using YOLO.

  First of all, for detecting plates there are a lot of options like tf object detection API and YOLO.
  So because most of the research papers do prove that YOLO is better and faster than any other algorithm and it is considered the state of the art in object detection 
  and i will use it here.

### Model
  1. We will use the most recent YOLO algorithm with is V8 from ultralytics.
  2. Prepare the plates dataset as the following image.
  <img width="739" alt="detect" src="https://user-images.githubusercontent.com/26833433/134436012-65111ad1-9541-4853-81a6-f19a3468b75f.png">
  
  3. Train the plate model.
  4. save the weights
  5. Prepare and train the character recognition model
  6. save the above models
  7. crop the image around the predicted box
  8. run the recognition model on the cropped image
  9. Output the text of the plate license.