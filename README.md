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

We finally used a GRU model that recorded higher performance than RNN.

### Setting

aaa

### Hyper parameter
vocab size : 3771<br>
sequence length : 500<br>
embedding size : 100<br>
dropout : 0.2<br>
num of layers : 1





## Result


**Accuracy for each attribute**

|     | precesion | recall | f1-score | accuracy |
| --- | --------- | ------ | -------- | -------- |
| E/I | 0.91      | 0.93   | 0.92     | 0.94     |
| S/N | 0.97      | 0.89   | 0.93     | 0.98     |
| T/F | 0.95      | 0.85   | 0.90     | 0.93     |
| P/J | 0.93      | 0.93   | 0.93     | 0.93     |

**Accuracy of combined model**

Correct : 17,153

Incorrect : 4,061

Accuracy : 80.86%


```GRU_EI , GRU_SN, GRU_TF, GRU_PJ, Model_Result``` of model folder contains a series of processes.

## Configuration

``` 
python == 3.7
pytorch == 1.9.0
torchtext == 0.9.0
```