# DATA606 - Capstone Project Proposal
# Alekhya Narala, 3rd Sem DS
## 1. Proposal Title: Household Garbage Classification for Recycling
- **Author Name** - Narala Alekhya
- Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang
- [GitHub](https://github.com/DATA-606-2023-FALL-TUESDAY/Narala_Alekhya/tree/main)
- [LinkedIn](linkedin.com/in/alekhyanarala)
- Link to your PowerPoint presentation file - (https://github.com/DATA-606-2023-FALL-TUESDAY/Narala_Alekhya/blob/main/docs/Garbage_Classification.pptx)
- Link to your YouTube video - https://youtu.be/z02oobgKhJY

## 2. Background
**What is it about?** - The topic revolves around the classification of household garbage into various categories, with the primary objective of improving and optimizing the recycling process. The dataset in question has images from 12 distinct categories of household waste, ranging from everyday items like paper and plastic to more specific items like clothes, shoes, and batteries. These images were largely sourced through web scraping, with some being borrowed from existing datasets.

**Why does it matter?** - Environmental Impact: Proper recycling reduces the need for raw material extraction, minimizing environmental degradation and harmful emissions from landfills and incinerators.

Waste Management Efficiency: Correctly categorized waste streamlines recycling processes, ensuring materials are recycled effectively without contamination.

Economic Benefits: Efficient recycling can lead to cost savings and potential revenue generation from recyclable materials.

Promotion of Sustainability: Emphasizing sorting and recycling fosters sustainable living habits, leading to reduced consumption and responsible waste disposal.

**Research questions** -

- Effectiveness of Image Classification: How effectively can machine learning models classify household garbage into the 12 categories based on the provided dataset?

- Real-world Application: How can the results of this classification be implemented in a real-world garbage sorting facility? What challenges might arise in a real-world setting compared to a controlled dataset?
  
- Image Resolution and Classification: Does the resolution(size) or quality of an image affect the accuracy of classification algorithms?

- Impact of Image Quality and Variation: How does the quality and variety of images (e.g., images of new clothes vs. discarded clothes) affect the classification accuracy?

- Transfer Learning: Can pre-trained models(eg. VGG16, ResNet)be fine-tuned to achieve better classification performance on this Dataset?

By addressing these research questions, one can gain a deeper understanding of the potential and challenges of using image classification techniques in the realm of waste management and recycling.

## 3. Data 
Describe the datasets you are using to answer your research questions.

- Data sources: [Dataset link](https://www.kaggle.com/datasets/mostafaabla/garbage-classification?resource=download)
- Data size: 251 MB
- Data shape: contains 15.5k .jpg file
- Data Dictionary
  | Column Name  | Data Type | Definition | Potential Values |
  |--------------|-----------|------------|------------------|
  | Image_ID | Integer  | Unique identifier for each image       | 1,2,3,...,15150           |
  | Image | Object     | The actual image data or path to the image       | File paths or image objects          |
  | Category          | String       | Type of garbage depicted in the image        | paper, cardboard, biological, metal, plastic, green-glass, brown-glass, white-glass, clothes, shoes, batteries, trash              |
  | Image_Size | Integer     | The size of the image       | Values in KB/MB, e.g., 500KB, 2MB           |
- Target/label for ML model: Category: This is the column that indicates the type of garbage, and it will be the primary target for classification tasks.
- Features/predictors for your ML models:
  - Image: This is the primary feature. The raw pixel data or processed features extracted from the images will be used to train the classification model.
  - Image_Size: Depending on the nature of the images, the size might provide some hints. For instance, high-resolution images of clothes might be larger than those of small items like   batteries.
 
## 4. Exploratory Data Analysis(EDA)
### Data Cleansing and Preparation:

- Data Extraction and Directory Structure:
The dataset was obtained by unzipping the "Project_A.zip" file, which contained image files.
The directory structure was analyzed using os.walk(), filtering and collecting image files with the '.jpg' extension.
Labels (garbage categories) were extracted from directory names, associating each image with its category.

- Data Organization:
The collected data was structured into a Pandas DataFrame named 'df,' comprising two essential columns: 'image_path' (storing file paths) and 'label' (representing category labels).

### Visualizations and Interpretations:

- Category and Image Size Analysis:
  
  The code included visualizations to explore the dataset further:

    A scatter plot to examine the relationship between 'image_size' and 'category.'
  
    A box plot to visualize the distribution of image sizes across different garbage categories.

    A pie chart to illustrate the distribution of garbage categories.

    A violin plot to showcase the distribution of image sizes by garbage category.

  <img src="https://github.com/AlekhyaNarala28/hi/blob/main/newplot.png">
  <img src="https://github.com/AlekhyaNarala28/hi/blob/main/newplot%20(1).png">


- Image Visualization:
  A function was defined to display both the original and resized images for specific image IDs.
  Sample images were displayed for visual inspection.

## 5. Model Training 

- We will be using the following deep-learning models for predictive analytics in the project:

  VGG16
  VGG19
  DenseNet
  Resnet50
  
  These models are commonly used for image classification tasks and are known for their effectiveness in learning complex patterns in large datasets.
- Generally, datasets are split into a training set and a testing set. I used the 80/20 ratio in this project.
- Some Python packages I used in the project: TensorFlow and Keras are used for building and training the deep-learning models. Other supportive packages I used are NumPy and Pandas,
  which are used for data manipulation. Also, Plotly and Seaborn are used for data visualization.
- The development environments I used are my Macbook, Google CoLab, and VSCode. 
- I measured and compared the performance of the models by the following metrics:

  Accuracy: The most straightforward metric, measuring the percentage of correctly classified images.

  Loss Function: This includes categorical cross-entropy loss for multi-class classification tasks, which is a common choice for these models.

## 6. Application of the Trained Models

I developed a web app for people to interact with the trained models. A potential tool for web app development I used is: Flask

## 7. Conclusion

- Summary of Work and Its Potential Application

  Project Focus: The project involves developing a machine-learning model for classifying garbage images into different categories.

  Data Preparation and EDA: The work includes collecting image data, constructing a data frame, resizing images, and performing exploratory data analysis (EDA). Tools like Plotly Express    were used for visualizing the data.

  Model Training and Testing: Various deep learning models like VGG16, VGG19, DenseNet, and Resnet50 were explored for image classification.

  Application: This project has significant potential in waste management and recycling, where accurate classification of waste types is crucial for effective sorting and recycling       
  processes.

- Limitations of the Work

  Data Quality and Diversity: There is a limitation related to the quality and diversity of the image data collected.

  Model Complexity and Resource Intensity: Deep learning models like Resnet50 and DenseNet, are resource-intensive and require substantial computational power.

  Generalization: The model's ability to generalize to different types of garbage images not included in the training set could be limited.

- Lessons Learned

  Importance of Data Preprocessing: The crucial role that data cleaning and preparation play in the success of a machine learning project.

  Model Selection: Insights into the strengths and weaknesses of different deep learning architectures for image classification tasks.

- Future Research Direction

  Data Augmentation: Exploring data augmentation techniques to increase the diversity of the training dataset, potentially improving the model's ability to generalize.

  Real-world Testing: Applying the models in real-world scenarios for further validation and to understand practical challenges.

  This overview provides a high-level understanding of my project, its value, the challenges faced, and where you might take this research in the future.

## 8. References 

  List articles, blogs, and websites that I have referenced in the project.

  https://dl.acm.org/doi/fullHtml/10.1145/3574318.3574345

  https://medium.com/analytics-vidhya/image-classification-with-vgg-convolutional-neural-network-using-keras-for-beginners-61767950c5dd

