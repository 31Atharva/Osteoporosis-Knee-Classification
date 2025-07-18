# Osteoporosis_knee_Classification
![man-knee-pain-he-puts-260nw-2476578973 jpg](https://github.com/PATRICK079/Osteoporosis_knee_Classification/blob/main/man-knee-pain-he-puts-260nw-2476578973.jpg.jpg)

# Introduction
This project aims to predict whether a patient has a healthy knee or one affected by osteoporosis. By using advanced machine learning techniques, the application offers two prediction modes to assess knee health.

The focus of this project is to develop a user-friendly tool that helps identify individuals at risk of osteoporosis, a condition that weakens bone density and increases the likelihood of fractures. Osteoporosis often leads to mobility issues and other health complications. The application combines data analysis and prediction models to provide valuable insights into an individual’s bone health, offering a clearer picture of their risk for osteoporosis-related knee problems.
# Business Statement
As a machine learning expert in a healthcare organization, one of the orthopedic doctors has approached me to leverage my expertise. He has requested that I develop a machine learning model capable of identifying healthy knees and those affected by osteoporosis using knee X-rays and patient data. The goal is to enhance and expedite his decision-making process. Additionally, the models will be deployed using Streamlit to ensure a user-friendly interface for practical application.

# Dataset Dictionary
This app is designed to predict whether a patient has a healthy knee or an osteoporosis-affected knee. Leveraging cutting-edge machine learning techniques, the app offers two prediction modes:

1. Patient Data Analysis: Input patient data to get a prediction based on a Logistic Regression Model.

• Joint Pain: Indicates whether the individual experiences joint pain, with options "Yes" or "No."

• Gender: Gender of the individual, with options "Male" or "Female."

• Age: The individual's age in years, ranging from 0 to 120 years.

• Menopause Age: The age at which menopause occurred (applicable only for females), ranging from 0.0 to 100.0 years. Male = 0

• Height (meters): The height of the individual in meters, ranging from 0.0 to 3.0 meters.

• Weight (kg): The weight of the individual in kilograms, ranging from 0.0 to 300.0 kg.

• Smoker: Indicates whether the individual smokes, with options "Yes" or "No."

• Diabetic: Indicates whether the individual has diabetes, with options "Yes" or "No."

• Hypothyroidism: Indicates whether the individual has hypothyroidism, with options "Yes" or "No."

• Number of Children: The total number of pregnancies or children the individual has had, ranging from 0 to 20.

• Seizure Disorder: Indicates if the individual has a seizure disorder, with options "Yes" or "No."

• Estrogen Use: Indicates whether the individual uses estrogen (applicable only for females), with options "Yes" or "No."

• History of Fracture: Indicates if the individual has a history of fractures, with options "Yes" or "No."

• Dialysis: Indicates whether the individual is undergoing dialysis, with options "Yes" or "No."

• Family History of Osteoporosis: Indicates if there is a family history of osteoporosis, with options "Yes" or "No."

• Maximum Walking Distance (km): Maximum distance the individual can walk without significant discomfort, ranging from 0.0 to 10.0 km.

• Medical History: Indicates whether the individual has any notable medical history, with options "Yes" or "No."

• T-Score Value: The T-score value used for bone density analysis, ranging from -20.0 to 10.0.

• Z-Score Value: The Z-score value used for bone density analysis, ranging from -20.0 to 10.0.

• BMI (Body Mass Index): Body Mass Index of the individual, ranging from 0.0 to 50.0.

• Obesity: Indicates whether the individual is considered obese, with options "Yes" or "No."

2. Knee X-ray Image Analysis: Upload a knee X-ray image to utilize a Convolutional Neural Network (CNN) model trained on the Osteoporosis Knee X-ray Dataset from Kaggle. Incorporates offline image augmentation for enhanced accuracy and robustness.

# Tools used 
1. Tensorflow
2. Git
3. Streamlit
4. python
5. scikit-learn

# Python Version
3.11.1

# Path 
atharvadumbre@Atharvas-MacBook-Air ~/Osteoporosis_knee_Classification-main
$ source ~/myenv/bin/activate
$ streamlit run main.py

# Problems encountered in this project and solutions

1. Insufficient Dataset for CNN Model: The initial dataset of only 372 images was too small for training a CNN model effectively. To address this, I performed offline image augmentation, generating new transformed images and expanding the dataset.

2. Memory Issues During Image Augmentation: Saving the augmented images overwhelmed the memory on my local machine. To resolve this, I transitioned to Saturn Cloud, which provided the necessary resources for handling the dataset efficiently.

3. GitHub Upload Limit for Model: The CNN model file was about 290 MB, which exceeded GitHub's 100 MB upload limit. I overcame this by uploading the model to an AWS S3 bucket, enabling me to deploy it via Streamlit.

# Key Learnings from the Project 
Throughout the process of building, training, and deploying the CNN model for knee image classification, I gained valuable insights and practical experience in several key areas:

1. Data Augmentation Techniques: I learned the importance of data augmentation when working with small datasets. By generating additional images through transformations, I was able to effectively increase the dataset size, which improved the performance and generalization of the model.
   
2. Model Deployment Challenges: I encountered practical challenges related to file size limitations when deploying models. By using AWS S3 for storing large model files, I learned how to work around restrictions like GitHub's file size limit and gained experience in integrating cloud storage with deployment tools like Streamlit.
 
3. Adaptability and Problem-Solving: The project required me to think creatively and quickly adapt to overcome technical hurdles. These experiences strengthened my problem-solving skills and deepened my understanding of how to handle real-world challenges in machine learning and model deployment.

# How it works 
The app utilizes two machine learning models: Logistic Regression for patient data and Convolutional Neural Networks (CNN) for knee X-rays.

1. Patient Data Classification:
Users provide relevant medical information such as age, gender, lifestyle, and other health indicators. The app then uses a Logistic Regression Model to predict whether the knee is healthy or affected by osteoporosis. For a better understanding of the input data, please refer to the Data Dictionary section above.

2. Image Classification:
Users can upload a knee X-ray image, which is processed and analyzed using a Convolutional Neural Network (CNN). This model is trained to detect signs of osteoporosis in the knee. For sample X-ray images for testing, check out the Sample Image Folder in this repository or click on this link https://github.com/31Atharva/Osteoporosis_Knee_Classification/tree/main/sample%20images

# package list
$ pip list
Package                      Version
---------------------------- -----------
absl-py                      2.1.0
altair                       5.5.0
appnope                      0.1.4
asttokens                    3.0.0
astunparse                   1.6.3
attrs                        25.1.0
blinker                      1.9.0
cachetools                   5.5.1
certifi                      2025.1.31
charset-normalizer           3.4.1
click                        8.1.8
comm                         0.2.2
contourpy                    1.3.1
cycler                       0.12.1
debugpy                      1.8.12
decorator                    5.1.1
executing                    2.2.0
flatbuffers                  25.1.24
fonttools                    4.55.8
gast                         0.6.0
gitdb                        4.0.12
GitPython                    3.1.44
google-pasta                 0.2.0
grpcio                       1.70.0
h5py                         3.12.1
idna                         3.10
ipykernel                    6.29.5
ipython                      8.32.0
jedi                         0.19.2
Jinja2                       3.1.5
joblib                       1.4.2
jsonschema                   4.23.0
jsonschema-specifications    2024.10.1
jupyter_client               8.6.3
jupyter_core                 5.7.2
keras                        3.8.0
kiwisolver                   1.4.8
libclang                     18.1.1
Markdown                     3.7
markdown-it-py               3.0.0
MarkupSafe                   3.0.2
matplotlib                   3.10.0
matplotlib-inline            0.1.7
mdurl                        0.1.2
ml-dtypes                    0.4.1
namex                        0.0.8
narwhals                     1.25.0
nest-asyncio                 1.6.0
numpy                        2.0.2
opt_einsum                   3.4.0
optree                       0.14.0
packaging                    24.2
pandas                       2.2.3
parso                        0.8.4
pexpect                      4.9.0
pillow                       11.1.0
pip                          22.3.1
platformdirs                 4.3.6
prompt_toolkit               3.0.50
protobuf                     5.29.3
psutil                       6.1.1
ptyprocess                   0.7.0
pure_eval                    0.2.3
pyarrow                      19.0.0
pydeck                       0.9.1
Pygments                     2.19.1
pyparsing                    3.2.1
python-dateutil              2.9.0.post0
pytz                         2025.1
pyzmq                        26.2.1
referencing                  0.36.2
requests                     2.32.3
rich                         13.9.4
rpds-py                      0.22.3
scikit-learn                 1.6.1
scipy                        1.15.1
seaborn                      0.13.2
setuptools                   65.5.0
six                          1.17.0
smmap                        5.0.2
stack-data                   0.6.3
streamlit                    1.41.1
tenacity                     9.0.0
tensorboard                  2.18.0
tensorboard-data-server      0.7.2
tensorflow                   2.18.0
tensorflow-io-gcs-filesystem 0.37.1
termcolor                    2.5.0
threadpoolctl                3.5.0
toml                         0.10.2
tornado                      6.4.2
traitlets                    5.14.3
typing_extensions            4.12.2
tzdata                       2025.1
urllib3                      2.3.0
wcwidth                      0.2.13
Werkzeug                     3.1.3
wheel                        0.45.1
wrapt                        1.17.2

