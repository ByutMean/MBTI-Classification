# MBTI-Classification
In this project, we classify MBTI of text data through GRU

## Purpose

- MBTI consists of a total of 16 classes of E/I, N/S, F/T, and P/J for each of the four attributes.
However, the performance of multi-class classification, which classifies 16 classes, was very low.
Therefore, we aim to classify mbti by combining the four models after conducting binary classification on each attribute.

- The labeled kaggle dataset was used, and GRU was used as the classification model.


Team-project of 'Artificial Neural Networks and Deep Learning' lecture in 2022-1


## Data

We used the kaggle data.
There are a total of 106067 rows of data, and each row consists of text data and labels.
Text data is a sentence used by the user in 'Reddit' and consists of up to 500 words.

You can access at [here](https://www.kaggle.com/datasets/zeyadkhalid/mbti-personality-types-500-dataset)


## Data Pre-processing

We proceeded stopword removal, url removal, and lemmatization for text data.
<br>
In order to reduce the amount of learning, unnecessary words were removed through word frequency, and a total of 3,771 words were finally used.
<br>
Each word was converted into a vector form to input text data.
<br>
To keep the length between sentences constant, the length of the sentences was adjusted to 500 words (vectors) by adding padding.
<br>
Finally, we conducted label encoding for labels in the form of text.


It can be checked in ```preprocessing.ipynb```.

## Model

### Setting

### Hyper parameter


나중에 수정


## Result

표 집어 넣기


## Configuration

``` 
python == 3.7
pytorch == 1.9.0
torchtext == 0.9.0
```