# AgriTech Project
## Project link: https://github.com/Gurkirat2915X/CS50W-finalProject.git
## Overview

AgriTech is a comprehensive solution designed to assist farmers and agricultural enthusiasts in identifying plant diseases through image analysis. The project leverages advanced deep learning models, including YOLOv11 and SAM2, to detect and classify diseases affecting various parts of plants such as leaves, stems, and fruits.

## Features

- **Image Upload**: Users can upload images of plants to detect diseases.
- **Disease Detection**: The system identifies and highlights the diseased areas in the uploaded images.
- **Chatbot Integration**: A chatbot is available to provide additional information and assistance.
- **User-Friendly Interface**: The web application offers an intuitive and easy-to-use interface for users.
- **Machine Learning Models**: Utilizes YOLOv11 for object detection and SAM2 for segmentation to accurately identify plant diseases.
- **Image Processing**: Implements preprocessing steps to enhance image quality and accuracy of disease detection.
- **Responsive Design**: The web application is designed to work seamlessly on various devices and screen sizes.
- **Easy Access**: Users can access the application from any device with an internet connection.

## Distinctiveness and Complexity

### Distinctiveness

This project stands out due to its integration of multiple advanced technologies to provide a robust solution for plant disease detection. Unlike typical web applications, AgriTech combines machine learning, image processing, and a user-friendly interface to deliver a unique and valuable tool for the agricultural sector.

### Complexity

The complexity of this project lies in its multi-faceted approach:

- **Machine Learning Models**: Utilizes YOLOv11 for object detection and SAM2 for segmentation, ensuring precise identification of plant diseases.
- **Image Processing**: Implements preprocessing steps to enhance image quality and accuracy of disease detection.
- **Web Integration**: Seamlessly integrates the machine learning models with a web interface, allowing users to upload images and receive real-time analysis.

## File Descriptions

### Main Directory

- **LICENSE**: Contains the MIT license for the project.
- **README.md**: This file, providing an overview and instructions for the project.

### `finalProject/Chatbot/`

- **chatbot.js**: JavaScript file for handling chatbot interactions.
- **index.html**: HTML file for the chatbot interface.
- **styles.css**: CSS file for styling the chatbot interface.
- **training.py**: Python script for training the chatbot model.
- **intents.json**: JSON file containing the intents and responses for the chatbot.

### `finalProject/image_detection_and_segmentation_model/`

- **model.ipynb**: Jupyter notebook for building and training the image detection and segmentation model.
- **weigths_and_bias/**: Directory containing the trained model weights.

### `finalProject/website/`

- **manage.py**: Django management script.
- **db.sqlite3**: SQLite database file.
- **disease_detector/**: Django app for disease detection.
  - **models.py**: Defines the database models.
  - **views.py**: Handles the web requests and responses.
  - **urls.py**: URL routing for the app.
  - **static/**: Contains static files like CSS and JavaScript.
  - **templates/**: Contains HTML templates for the web pages.
- **requirements.txt**: Contains the required Python packages for the project.
- **website/**: Django project settings and configurations.
- **media/**: Directory for storing user-uploaded images and other files.
  - **images/**: Subdirectory for storing uploaded images.
  - **detection_images/**: Subdirectory for storing processed images with disease annotations.
  - **models/**: Subdirectory for storing the trained machine learning model.
  - **Chatbot/**: Subdirectory for storing chatbot-related files.

## How to Run the Application

1. **Navigate to the Project Directory**:
   ```sh
   cd finalProject
   ```
2. **Install the Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```
3. **Run Migrations**:
   ```sh
    python website/manage.py migrate
   ```
4. **Start the Development Server**:
    ```sh
    python website/manage.py runserver
    ```
## Additional Information
- **Model Training**:
  - The `model.ipynb` notebook contains the code for training the image detection and segmentation model.
  - The trained model weights are saved in the `weigths_and_bias` directory.
- **Chatbot Training**:
  - The `training.py` script is used to train the chatbot model based on the intents and responses in `intents.json` and `HTML,CSS,JS` present here are only for testing and not used in actual website.

### Special Thanks to CS50W Team for providing the guidance and support throughout the course.
