# AgriTech Project
## Project link: https://github.com/Gurkirat2915X/CS50W-finalProject.git
## Overview

AgriTech, my CS50W capstone project, offers a comprehensive solution for farmers and agricultural enthusiasts to identify plant diseases through image analysis. This web application allows users to upload images of plants, which are then processed using machine learning models to detect and highlight diseased areas. Utilizing models such as SAM2 and YOLOv11, AgriTech effectively segments the affected parts of the plant.

Furthermore, AgriTech includes a chatbot that offers additional information and assistance to users. Powered by NLTK and PyTorch, the chatbot enhances user interaction and support. This feature aims to empower farmers with the tools and knowledge necessary to protect their crops and optimize agricultural practices.

## Problem Statement

Plant diseases pose a significant threat to crop yield and quality, impacting farmers worldwide. Identifying and treating these diseases in a timely manner is crucial to prevent crop loss and ensure food security. However, manual detection of plant diseases can be challenging and time-consuming, often requiring expert knowledge and resources.

I address this problem by leveraging machine learning and image processing techniques to automate the detection of plant diseases. By providing a user-friendly platform for uploading images and receiving real-time analysis, AgriTech enables farmers to quickly identify diseased plants and take appropriate action. The integration of a chatbot further enhances the user experience by offering guidance and support throughout the process. With AgriTech, I aim to revolutionize plant disease detection and management, empowering farmers with the tools needed to protect their crops and livelihoods.

## Features

- **Image Upload**: Users can upload images of plants to detect diseases.
- **Disease Detection**: The system identifies and highlights the diseased areas in the uploaded images.
- **Chatbot Integration**: A chatbot is available to provide additional information and assistance.
- **User-Friendly Interface**: The web application offers an intuitive and easy-to-use interface for users.
- **Machine Learning Models**: Utilizes YOLOv11 for object detection and SAM2 for segmentation to accurately identify plant diseases.
- **Image Processing**: Implements preprocessing steps to enhance image quality and accuracy of disease detection.
- **Responsive Design**: The web application is designed to work seamlessly on various devices and screen sizes.
- **Easy Access**: Users can access the application from any device with an internet connection.
- **User Authentication**: Implements user authentication to ensure secure access to the application.
- **Storing Images**: Allows users to access the uploaded images and detection images in the database for future reference.

## Distinctiveness and Complexity

### Distinctiveness

AgriTech stands out from existing solutions due to its unique combination of features and capabilities:
- **Storing Images**: Allows users to upload images of plants for disease detection and analysis. The uploaded images are stored in the database for future reference.
- **Machine Learning Models**: Makes use of YOLOv11 and SAM2 models for precise detection and segmentation of plant diseases.
- **Chatbot Integration**: Offers a chatbot for user interaction and support, enhancing the overall user experience. I have created a chatbot using NLTK and PyTorch which is trained on intents.json file. I used my knowledge from CS50AI course to create this chatbot.
- **User-Friendly Interface**: Provides an intuitive and easy-to-use interface for users to upload images and receive real-time analysis.
- **User Authentication**: Implements user authentication using Django's built-in authentication system, ensuring secure access to the application.

#### How it is different previous projects present in the course:
Here I will discuss how AgriTech is different from the previous projects present in the course and how it stands out as a unique project.

- **Old CS50W Pizza Project:**
In the pizza project, the main focus was on creating a web application for ordering pizzas. The project involved creating a Django application with features like adding pizzas to the cart, placing orders, and viewing order history.

  **Difference**: AgriTech is not a application for ordering pizza, it is a web application for detecting plant diseases. Using this I have tried to solve a real world problem of farmers.

- **CS50W Project 2 - Commerce:**
In the commerce project, the main focus was on creating an e-commerce platform where users can list items for sale, place bids on items, and view listings.

  **Difference**: AgriTech is not a e-commerce platform, it is a web application for detecting plant diseases. This project does not involve buying or selling items, it is focused on detecting plant diseases using machine learning models.

- **CS50W Project 4 - Network:**
In the network project, the main focus was on creating a social network platform where users can post messages, follow other users, and like posts.

  **Difference**: AgriTech is not a social network platform, it is a web application for detecting plant diseases. This is not a platform to post messages or follow other users, it is focused on detecting plant diseases using machine learning models.

Thus from the above points it is clear that AgriTech is different from the previous projects present in the course. It is a unique project that aims to solve a real world problem using machine learning. It provides a platform for farmers and agricultural enthusiasts to identify plant diseases through image analysis.

### Complexity

In this section I will discuss the complexity of the project and how I have implemented every feature of the project in detail.

- **Image Upload**: This I have implemented by first creating a model in Django for storing the uploaded images. Then I have accepted the image form and in  `finalProject/website/disease_detector/views.py`. In this I have also implemented the functionality to store the uploaded images and image from detection in the `finalProject/website/media/images` and `finalProject/website/media/detection_images` directory.

- **Disease Detection**: For this I have used the YOLOv11 model for object detection and SAM2 model for segmentation.I have at first trained the model on the plant disease dataset: [https://universe.roboflow.com/plantdoc-xztat/proposed] and saved the weights in the `finalProject/website/media/models/` directory. Then I have implemented the functions for image processing, disease detection in `finalProject/website/disease_detector/utils.py`. All the training has been done by using the `model.ipynb` notebook present in the `finalProject/image_detection_and_segmentation_model/` directory and done on Google Colab.I have implemented this in `finalProject/website/disease_detector/utils.py`. In this I have implemented the functions for image processing, disease detection.
- **Chatbot Integration**: I have created a chatbot using NLTK and PyTorch which is trained on intents.json file. I have the trained model from the `training.py` script  in `Chatbot/` and saved it in the `finalProject/website/media/Chatbot/` directory along with intends.json.I used my knowledge from CS50AI course to create this chatbot. I have implemented this in `finalProject/website/disease_detector/utils.py`.
- **User-Friendly Interface**: I have created the HTML templates for the web pages in the `finalProject/website/disease_detector/templates/` directory. I have used CSS for styling the web pages in the `finalProject/website/disease_detector/static/` directory. I have used JavaScript for handling the chatbot interactions in the `finalProject/website/disease_detector/static/` directory. I have also made the web application responsive by using media queries in the CSS files.
- **User Authentication**: I have implemented the user authentication using Django's built-in authentication system. I have created the login and register pages in the `finalProject/website/disease_detector/templates/` directory. I have implemented the login and register functionality in the `finalProject/website/disease_detector/views.py` file.

## File Descriptions

### Main Directory

- **LICENSE**: Contains the MIT license for the project.
- **README.md**: This file, providing an overview and instructions for the project.

### `finalProject/Chatbot/`
This directory contains the files related to the testing chatbot feature.
**Note**: The chatbot files are only for testing and not used in actual website.All of the chatbot functionality is implemented in the `finalProject/website/disease_detector/utils.py`. and trained model and intents are present in `finalProject/website/media/Chatbot/` directory.

- **chatbot.js**: JavaScript file for handling chatbot interactions.
- **index.html**: HTML file for the chatbot interface.
- **styles.css**: CSS file for styling the chatbot interface.
- **training.py**: Python script for training the chatbot model.
- **intents.json**: JSON file containing the intents and responses for the chatbot.

### `finalProject/image_detection_and_segmentation_model/`

This directory contains the files related to the image detection and segmentation model.

**Note**: This directory only contains the files related to the model training and weights and only weights are used in the actual website. This model is trained on the plant disease dataset: [https://universe.roboflow.com/plantdoc-xztat/proposed]

The model weights are saved in the `finalProject/website/media/models/` directory.

- **model.ipynb**: Jupyter notebook for building and training the image detection and segmentation model.
- **weigths_and_bias/**: Directory containing the trained model weights.

### `finalProject/website/`

This directory contains the Django project for the AgriTech web application. 

- **manage.py**: Django management script.
- **db.sqlite3**: SQLite database file for storing all the models.
- **disease_detector/**: Django app for disease detection.
  - **models.py**: Defines the database models.Here I have defined the model for storing the uploaded images.
  - **views.py**: Handles the web requests and responses.
  - **urls.py**: URL routing for the app.
  - **utils.py**:
    - Contains the functions for image processing, disease detection, and chatbot integration.
    - Implements the machine learning models for image detection and segmentation.
    - Integrates the chatbot functionality for user interaction.
  - **static/**: Contains static files like CSS and JavaScript. Also contains the images for the web pages.
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
