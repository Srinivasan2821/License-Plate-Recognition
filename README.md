# License-Plate-RecognitionLicense Plate Recognition
This project is focused on detecting and recognizing license plates from images using a combination of YOLOv5 for detection and Tesseract OCR for recognition.

Table of Contents
Introduction
Features
Installation
Usage
Dataset
Training the Model
Testing the Model
Results
Contributing
License
Introduction
The goal of this project is to develop an automated system for license plate recognition using deep learning techniques. It leverages the YOLOv5 model for object detection to locate license plates in images and uses Tesseract OCR to extract the text from these plates.

Features
Detects license plates in images.
Recognizes and extracts text from the detected license plates.
Saves the results in CSV files.
Installation
Prerequisites
Python 3.7+
PyTorch
OpenCV
Tesseract OCR
Clone the Repository
bash
Copy code
git clone https://github.com/yourusername/License-Plate-Recognition.git
cd License-Plate-Recognition
Install Dependencies
bash
Copy code
pip install -r requirements.txt
Setup Tesseract OCR
Install Tesseract OCR on your system:

For Ubuntu:

bash
Copy code
sudo apt-get update
sudo apt-get install -y tesseract-ocr
For Windows:

Download the installer from here and add Tesseract to your system's PATH.

Usage
Directory Structure
Ensure your project directory has the following structure:

scss
Copy code
License-Plate-Recognition/
├── yolov5/
│   ├── models/
│   ├── utils/
│   ├── detect.py
│   └── ... (other YOLOv5 files)
├── test/
│   └── ... (test images)
├── output/
│   └── ... (output files will be saved here)
├── requirements.txt
└── main.py
Running the Code
Place your test images in the test directory.

Run the main script:

bash
Copy code
python main.py
The script will process the images, perform detection and OCR, and save the results in the output directory.

Dataset
You can use any dataset containing images of vehicles with visible license plates. Ensure the dataset is split into training and testing sets appropriately.

Training the Model
If you need to train your YOLOv5 model, follow these steps:

Prepare the dataset: Ensure your dataset is in the YOLO format (images and corresponding label files).

Train the YOLOv5 model:

bash
Copy code
cd yolov5
python train.py --img 640 --batch 16 --epochs 100 --data your_dataset.yaml --weights yolov5s.pt --cache
Replace your_dataset.yaml with your dataset configuration file.

Save the trained model weights in the runs/train/exp/weights/ directory.
Testing the Model
To test the trained YOLOv5 model on new images, ensure your test images are placed in the test directory and run the main.py script as mentioned in the usage section.

Results
The results of the detection and OCR will be saved in the output directory:

plate_numbers.csv: Contains image names and the recognized plate numbers.
bounding_boxes.csv: Contains image names and bounding box coordinates of the detected plates.
Contributing
Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or new features to suggest.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

