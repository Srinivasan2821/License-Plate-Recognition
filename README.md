_**License Plate Recognition**_

![image](https://github.com/Srinivasan2821/License-Plate-Recognition/assets/154582529/a97aefd5-a705-448e-b4b2-177636f5a586)

This project is designed to automate the process of license plate recognition using a combination of YOLOv5 for object detection and Tesseract OCR for optical character recognition.

**Table of Contents**
  Introduction
  Features
  Installation
  Usage
  Directory Structure
  Dataset
  Training the Model
  Testing the Model
  Results
  Contributing
  License
  
**Introduction**
The aim of this project is to develop an automated system capable of detecting and recognizing license plates from images. It utilizes YOLOv5, a state-of-the-art object detection model, to accurately identify the location of license plates in images. Once detected, Tesseract OCR is used to extract the text from these license plates.

**Features**
**License Plate Detection**: Uses YOLOv5 to detect license plates in images.
**Text Recognition:** Extracts text from the detected license plates using Tesseract OCR.
**CSV Output:** Saves the results, including image names and detected plate numbers, in CSV files for further analysis.

**Installation**

**Prerequisites**
Before you begin, ensure you have Python 3.7 or higher installed on your system. You will also need to install PyTorch, OpenCV, and Tesseract OCR.

**Steps**
**Clone the Repository:** Obtain the project files by cloning the GitHub repository.
**Install Dependencies:** Install all necessary Python packages listed in the requirements.txt file.
**Setup Tesseract OCR:** Install Tesseract OCR on your system. For Ubuntu, use the apt-get package manager, and for Windows, download the installer from the Tesseract OCR GitHub page and add it to your system's PATH.

**Usage**
**Prepare Test Images:** Place your test images in the designated test directory within the project folder.
**Run the Main Script:** Execute the main script to perform detection and OCR on the test images. The results will be saved in the output directory.
Directory Structure
The project should have a specific directory structure to function correctly. Key directories include:

**yolov5:** Contains the YOLOv5 model files and scripts.
**test:** This is where you place your test images.
**output:** The results of the detection and OCR processes will be saved here.

**Dataset**
You can use any dataset that includes images of vehicles with visible license plates. Ensure that your dataset is properly organized and split into training and testing sets. The YOLOv5 model requires data to be in a specific format with corresponding label files.

**Training the Model**
If you need to train your own YOLOv5 model:

**Prepare the Dataset:** Ensure your dataset is formatted correctly for YOLOv5.
**Train the Model:** Run the training script with your dataset to train the YOLOv5 model. The trained model weights will be saved in the specified directory.
Testing the Model

**To test the trained YOLOv5 model:**
**Place Test Images:** Ensure your test images are in the correct directory.
**Run the Main Script:** Execute the script to process the images. The script will use the trained model to detect license plates and perform OCR to extract the text.
Results
The results of the license plate detection and OCR processes are saved in the output directory.

**The output includes:**
A CSV file containing the image names and the recognized license plate numbers.
Another CSV file listing the bounding box coordinates for each detected license plate.
Contributing
Contributions to this project are welcome. If you have any suggestions or improvements, please open an issue or submit a pull request on GitHub.

**License**
This project is licensed under the MIT License. Refer to the LICENSE file for more details.
