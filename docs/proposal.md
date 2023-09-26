# DATA606 - Capstone Project Proposal
## 1. Proposal Title: Household Garbage Classification for Recycling
- **Author Name** - Narala Alekhya
- Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang
- [GitHub](https://github.com/AlekhyaNarala28)
- [LinkedIn](linkedin.com/in/alekhyanarala)
- Link to your PowerPoint presentation file - in progress
- Link to your YouTube video - in progress

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
