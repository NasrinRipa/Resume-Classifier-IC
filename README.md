<<<<<<< HEAD
# Resume-Classifier-IC
This work presents a resume-classifier ML model which can categorize resumes from a input directory containing pdf files of resumes. I used "Blurr" to train the model and the script.py file can be run directly from the commandline terminal to get the output. 
# MultiLabel-Book-Genre-Classifier

A text classification model from data collection, model training, and deployment. <br/>
The model can classify 141 different types of book genres <br/>The keys of `deployment\genre_types_encoded.json` shows the book genres

 ## Data Collection

Data was collected from a Goodreads Website Listing: https://www.goodreads.com/list/show/264.Books_That_Everyone_Should_Read_At_Least_Once <br/>The data collection process is divided into 2 steps:

1. **Book URL Scraping:** The book urls were scraped with `scraper\book_url_scraper.py` and the urls are stored along with book title in `scraper\book_urls.csv`
2. **Book Details Scraping:** Using the urls, book description and genres are scraped with `scraper\book_details_scraper.py` and they are stored in `data\book_detils.csv`

In total, I scraped 6,313 book details

## Data Preprocessing

Initially there were *640* different genres in the dataset. After some analysis, I found out *499* of them are rare (probably custom genres by users). So, I removed those genres and then I have *141* genres. After that, I removed the description without any genres resulting in *6,104* samples.

## Model Training

Finetuned a `distilrobera-base` model from HuggingFace Transformers using Fastai and Blurr. The model training notebook can be viewed [here](https://github.com/msi1427/MultiLabel-Book-Genre-Classifier/blob/main/notebooks/multilabel_text_classification.ipynb)

## Model Compression and ONNX Inference

The trained model has a memory of 300+MB. I compressed this model using ONNX quantization and brought it under 80MB. 

## Model Deployment

The compressed model is deployed to HuggingFace Spaces Gradio App. The implementation can be found in `deployment` folder or [here](https://huggingface.co/spaces/msideadman/multilabel-book-genre-classifier) 

<img src = "deployment/gradio_app.PNG" width="800" height="400">

## Web Deployment
Deployed a Flask App built to take descprition and show the genres as output. Check `flask ` branch. The website is live [here](https://multilabel-book-genre-classifier.onrender.com) 

<img src = "deployment/flask_app_home.PNG" width="800" height="400">
<img src = "deployment/flask_app_results.PNG" width="800" height="200">
=======
# Resume-Classifier
📁📄 Welcome to the Resume Classifier Repository 

This repository showcases a machine learning model designed to categorize resumes from an input directory containing PDF files of resumes. The model utilizes the power of the "Fastai" and "Blurr" library and can be effortlessly executed using the `script.py` file from the command-line terminal.

## Data Collection

The dataset was sourced from [Kaggle](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset), consisting of a total of 3447 resume entries stored in the "Resume.csv" file.

## Model Selection

The Fastai library in conjunction with the "distilroberta-base" model was chosen due to its user-friendly nature and time-efficient capabilities.

## Model Training

The "distilroberta-base" model from HuggingFace Transformers was fine-tuned using Fastai and Blurr. The model training notebook can be explored in the "notebooks" folder of this repository. The trained model achieved an impressive accuracy of approximately 96%.

Since the dataset size was limited, it was split into two sets: the training dataset and the validation dataset, and, later the validation dataset was utilized as the test dataset.

## Model Performance

The F1 scores for this model are as follows:

- F1 Score (Micro) = 0.5473145780051151
- F1 Score (Macro) = 0.37185516078339154

## Model Compression and ONNX Inference

The initial memory footprint of the trained model exceeded 300MB. However, by employing ONNX quantization techniques, the model's size was drastically reduced to 80MB.

## Model Deployment and Running the Script

To deploy the model, utilize the `script.py` file. This Python script is executable from the command line using the following command:
```bash
python script.py "path/to/directory" 




>>>>>>> 265ae53525b67a2cdb678e593fb6af3a758624d8
