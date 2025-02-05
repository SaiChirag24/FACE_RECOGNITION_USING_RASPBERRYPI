Face Recognition using Raspberry Pi

This project implements a real-time face recognition system on a Raspberry Pi using the OpenCV and face_recognition libraries. It captures live video from a camera, detects faces, and identifies them using pre-trained encodings.

Features:

✅ Real-time Face Detection using OpenCV

✅ Face Recognition with pre-trained encodings

✅ Support for Raspberry Pi Camera Module & USB Webcams

✅ LED Indicators for recognized/unrecognized faces

✅ Encodings Stored in a Pickle File for Fast Matching



Hardware Requirements:

Raspberry Pi 3B+ or later

Pi Camera Module or USB Webcam

LEDs (Optional, for indicating face recognition status)

16x2 LCD Display (Optional, for displaying recognized names)



Software Requirements:

OS: Raspberry Pi OS (Raspbian)

Python Version: Python 3


Libraries Required:

sudo apt-get update

sudo apt-get install python3-pip

pip3 install opencv-python face_recognition imutils RPi.GPIO numpy

Project Setup

1. Clone the Repository

    Download the zip file

2. Train and Encode Faces
 
    Place images of known people inside dataset/ (one folder per person).

    Run the encoding script to generate encodings.pickle:

    python3 encode_faces.py

4. Run Face Recognition
 
    Start the real-time face recognition system:

    python3 facial_req.py


How It Works:

The Raspberry Pi captures a live video feed.

The face_recognition library detects faces and compares them with known encodings stored in encodings.pickle.

If a match is found, the person's name is displayed.

If no match is found, it labels the face as "Unknown".

LEDs or other output devices can provide visual feedback.



File Structure:


face-recognition-raspberrypi/
├── dataset/                # Stores face images for training

├── encodings.pickle        # Encoded face data

├── facial_req.py           # Main face recognition script

├── encode_faces.py         # Generates encodings from images

├── README.md               # Project documentation


Troubleshooting:

Face not detected? Ensure good lighting and a clear camera view.

Slow performance? Resize the image or use a lightweight model.

Module not found? Install missing dependencies using pip3 install.


Future Enhancements:

🔹 Improve face recognition accuracy with more training data

🔹 Optimize performance using hardware accelerators (e.g., Coral TPU)

🔹 Integrate with IoT for automated access control


License:
This project is open-source and available under the MIT License.

