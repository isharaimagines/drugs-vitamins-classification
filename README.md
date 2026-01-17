# Drugs & Vitamins Classification using Deep Convolutional Neural Networks and Transfer Learning

<img src="https://images.pexels.com/photos/159211/headache-pain-pills-medication-159211.jpeg" alt="drugs-image">

**Important Note:** This project is not affiliated with any research study or peer-reviewed article that has undergone extensive review and been formally accepted by recognized medical institutions. The dataset has not been evaluated by any pharmaceutical authority or by professionals with expertise in the relevant field. Utilization of this dataset is strongly encouraged solely for educational purposes, as improper use may present ethical concerns or potentially cause harm to individuals. It is advisable to refrain from employing this dataset for personal machine learning applications or services without prior peer review by a qualified expert in the medical field or by a regulatory authority responsible for the ethical deployment of medical datasets. Please take these considerations into account.

## Data Preprocessing

The data is divided into three categories: Training, Validation, and Testing. The training data is used to train the CNN model, while the validation data is used to fine-tune its parameters. The performance of the model is evaluated with the test data, which the model has not encountered before.

## Training the model

The model images will be processed using the pre-trained MobileNetV2 CNN. Three callbacks—Model Checkpoint, Early Stopping, and Tensorboard—will monitor the training. Below is a summary of the model's hyperparameters:

- Batch size : 32
- Epochs : 100
- Input Shape : (224, 224, 3)
- Output layer : 10

## Model Evaluation

The test dataset evaluates model performance, focusing on accuracy, which measures the fraction of correct predictions. Other metrics will also be tested.

- Precision(P): P=TP/(TP+FP) 
- Recall(R): R=TP/(TP+FN) 
- F1 score(F1): F1=2∗(TP∗FP)/(TP+FP)

## Plotting the Classification Reports and Confusion matrix

``` bash
              precision    recall  f1-score   support

      Alaxan       0.79      0.86      0.82       202
    Bactidol       0.83      0.85      0.84       201
      Bioflu       0.89      0.87      0.88       175
    Biogesic       0.74      0.77      0.75       211
     DayZinc       0.82      0.87      0.84       208
    Decolgen       0.91      0.90      0.90       192
    Fish Oil       0.90      0.85      0.88       212
    Kremil S       0.81      0.76      0.78       186
     Medicol       0.94      0.95      0.94       209
      Neozep       0.83      0.76      0.79       204

    accuracy                           0.84      2000
   macro avg       0.85      0.84      0.84      2000
weighted avg       0.84      0.84      0.84      2000

```

<img src="https://raw.githubusercontent.com/isharaimagines/drugs-vitamins-classification/refs/heads/main/confusion_matrix.png" alt="confusion_matrix">
