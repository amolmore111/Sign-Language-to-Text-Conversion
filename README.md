# Sign-Language-to-Text-Conversion
Sign language, being one of the oldest and most natural forms of communication, serves as a crucial means of expression for individuals with hearing and speech impairments. Deaf and dumb (D&M) individuals heavily rely on sign language for communication, given their limitations in using spoken languages. In this context, we are introducing a real-time method utilizing neural networks for finger spelling based on American Sign Language (ASL). Automatic human gesture recognition, especially from camera images, has become an intriguing area for developing computer vision applications. Recognizing hand gestures in real-time from camera images can significantly enhance communication for individuals with hearing and speech impairments. The proposed method employs Long Short-Term Memory (LSTM) to recognize hand gestures associated with American Sign Language.


![image](https://github.com/amolmore111/Sign-Language-to-Text-Conversion/assets/123639865/8704adac-10e3-4e7a-90d7-6dd9c11cae78)


In our project we basically focus on producing a model which can recognise Finger spelling based hand gestures in order to form a complete word by combining each gesture.
The gestures we aim to train are as given in the image below.

#Signs

![Sign Language signs](https://github.com/amolmore111/Sign-Language-to-Text-Conversion/assets/123639865/4183904f-f0eb-42f1-b5a7-d04a79272c04)

#Motivation:

Existing sign language recognition systems lack real-time capabilities, adaptability to varied environments, and holistic solutions, hindering seamless communication for Deaf and hardof-hearing individuals.

#Objectives:

 Achieve real-time recognition of finger-spelling gestures.

 Ensure system performance in diverse real-world settings.

 Optimize the use of Convolutional Neural Networks (CNNs) for gesture recognition.

 Provide a holistic communication solution incorporating real-time translation and userfriendly interfaces.

 Foster social inclusion and understanding through improved communication accessibility.

#Scope:

 Exploration and implementation of various background subtraction algorithms.

 Aim to enhance gesture recognition accuracy, particularly in complex backgrounds.

 Research and implementation of preprocessing techniques to improve gesture prediction in low light conditions.

 Focus on achieving higher accuracy in challenging lighting environments.

#Implementation Details

#1.Project Modules

1.1 Creating Custom Dataset and Preprocessing

 MediaPipe library for tracking hand and extracting keypoints.

 Created dataset by capturing images for each hand gesture (A to Z).

 Created labeled sequences for model training.

1.2 Keypoint Extraction

 Utilized functions like "mediapipe_detection", "draw_styled_landmarks" and "extract_keypoints" for image processing and landmarks extraction.

1.3 Model Training

 Loaded and preprocessed the custom dataset using sequences and labels.

 Used „train_test_split‟ to split data into training and testing set.

 Utilized LSTM based deep learning model for hand gesture recognition.

 Utilized TensorBoard callbacks for monitoring training progress.

 Trained the model for a specific number of epochs and saved the trained model architecture to a JASON file and weights to an H5 file.

1.4 Application

 Loded JASON and H5 file using Keras.

 Hand tracking and extraxting keypoints using MediaPipe.

 Capturing video frames and displaying output using OpenCV.

 Applied a threshold for gesture detection to control the output.

#Analysis

 For "modelAtoF", "modelGtoO" and "modelPtoZ" we observed high accuracy more than 90% in most cases.

 For „modelGtoO‟ the accuracy and speed to detect the sign is high, but there is confusion in some signs such as "J" and "N".

 For "modelPtoZ" the accuracy and speed to detect the sign is high, but there is 
 in some signs such as "P" or "U" and "V" or "X" and "Z".
 
 While training the "modelAZ" with expanded dataset we observed that as the epochs cross certain numbers the model would overfit. This resulted in decreasing the 
accuracy significantly. So we had to adjust the epochs we train the model on.

#Conclusion

In conclusion, the results underscore the strengths and areas which needs improvements in the sign language detection system. We started with small "ModelAtoC" with a custom dataset, emphasizing the clarity and simplicity. We developed a functional sign language detection for needed people using custom dataset which works in real-time.
