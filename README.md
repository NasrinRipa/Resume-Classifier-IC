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
python script.py "path/to/directory"  <br>




