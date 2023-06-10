# MVQA_ViLT
This is a medical visual question answering model that uses Vision-and-Language Transformers (ViLT) to answer questions about medical images. It was trained on a on radiology-related data using the VQA-RAD dataset. 
![image](https://github.com/daliazh/MVQA_ViLT/assets/85033378/af200b34-9097-488e-b2d6-f4400fc5ac4f)

## Requirements
* Download the VQA-RAD data in Data/osfstorage-archive/Processed and Data/osfstorage-archive/VQA_RAD Dataset Public.json.
* Download the pretrained ViLT model in Model/vilt_acc87.pt.

## Implementation Details
* All images have been cleared of noise, such as markings and text using the Keras-ocr package for text detection.
* The dataset is split for training and testing, with 0.8 for training and 0.2 for testing.
* Adam optimizer is used with a 5e-5 learning rate. 
* The model is trained for 50 epochs with a batch size of 10.

## Results
| **Model** | **Accuracy** | **BELU**  |
| :---:   | :---: | :---: |
| ViLT  | 87%      | 79% |

## Predictions
|![Screenshot 2023-05-29 203421](https://github.com/daliazh/MVQA_ViLT/assets/85033378/96fd16f0-2407-4d3f-8955-ac9c034a647f)| ![Screenshot 2023-05-29 203942](https://github.com/daliazh/MVQA_ViLT/assets/85033378/454215de-cfc5-464c-88d2-c3750f3c5d69) |
| :---:   | :---: | 
|![Screenshot 2023-05-29 204020](https://github.com/daliazh/MVQA_ViLT/assets/85033378/335d0c62-10d4-41f7-b5b8-ef118443172b)| ![Screenshot 2023-05-29 204047](https://github.com/daliazh/MVQA_ViLT/assets/85033378/0b73ff27-eab1-4a79-aa3c-84a36db98e72) |
