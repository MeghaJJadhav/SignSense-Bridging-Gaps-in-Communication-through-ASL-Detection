# SignSense-Bridging-Gaps-in-Communication-through-ASL-Detection
Innovative project leveraging Random Forest &amp; Logistic Regression for real-time ASL alphabet recognition. Explored LSTMs for complex hand movements. Future vision: Evolving into a user-friendly web app. Open to collaboration and ideas. [My 2nd Year College Project] 



#Abstract

SignSense utilizes Random Forest and Logistic Regression models for ASL alphabet recognition. The project also experimented with CNN for handling composite hand 

movements (Note: CNN stack is not provided in the repository).



###Implementation###

-Data Collection

-Capture diverse images and videos of ASL signers for dataset creation.

-Data Preprocessing

-Resize, normalize, and augment the dataset for effective model training.



###Model Training###

-Train Random Forest: train.ipynb

-Real-time Testing

-Use realtimetest_2.0.ipynb for real-time ASL alphabet recognition.
note - ignore model files other than model.p 


###Usage###

-Data Collection

1)Refer to pnew.ipynb for the data collection process.

-Data Preprocessing

1)Explore create_dtset.ipynb for dataset preprocessing.

2)What is MediaPipe?

MediaPipe is an open-source framework developed by Google for building multimodal (e.g., video, audio) machine learning pipelines. It provides a variety of pre-built solutions for real-time applications, such as hand tracking, face detection, and object detection.

3)Why Convert Images to RGB?

The cv2.imread function from OpenCV reads images in BGR (Blue, Green, Red) format by default. However, MediaPipe requires images in RGB (Red, Green, Blue) format for accurate processing. Converting images to RGB ensures that the color channels are in the correct order for MediaPipe to process them accurately. Incorrect color channels could lead to poor landmark detection performance.

4)What is Being Extracted from the Image and How?

MediaPipe processes the RGB image to detect hand landmarks. If a hand is detected, MediaPipe provides the coordinates of 21 key points (landmarks) on the hand, representing joints and tips of fingers.These coordinates are essential for understanding the hand's pose and gestures. Each landmark provides a (x, y) coordinate in the image space, which can be used to distinguish different hand gestures.

5)Why is Normalization Done?

Normalization involves adjusting the landmark coordinates so that the hand's position is consistent across different images. Specifically, the code normalizes the coordinates by subtracting the minimum x and y values from each coordinate.


-Model Training

1) Refer train.ipynb

The RandomForestClassifier model's good performance in real-time image classification of hand gestures can be attributed to a combination of effective preprocessing, the robustness of the Random Forest algorithm, and the characteristics of the dataset.

Starting with the preprocessing steps, MediaPipe's accurate detection of 21 hand landmarks provided a rich set of features representing the hand's geometry. Each landmark gave precise x and y coordinates, crucial for distinguishing different hand gestures. Additionally, the normalization step, which adjusted the landmark coordinates by translating the hand's position to a common origin, ensured that the model received consistent input data. This translation reduced variability and made the model more robust to different hand positions within the image frame, allowing it to generalize better to new images.



#Future Plans

-Host the web application on a server or cloud platform for public access.

-Evolve the project into a user-friendly web application for broader accessibility.

-Open to collaboration and ideas for further improvement and implementation of CNN.



#OUTCOME:

![1720784146569968](https://github.com/user-attachments/assets/b8b57c88-5d19-4bfe-b286-31ed7bfa9106)


License

This project is licensed under the MIT License.



Contact

For inquiries or collaboration, reach out to me via meghajjadhav17@gmail.com

Feel free to explore and contribute to SignSense!
