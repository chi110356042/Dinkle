# Dinkle

This project is NCCU cooperation with Dinkle, which used LSTM to predict product quality.

## Description

### model

Complete model that can be directly loaded for use.

- set α, β = 0.1

> Test:

`prediction = model(test_data, alpha=0.1, beta=0.1)`

### model_code

Complete model development program.

- DataonlyNet is a model that does not contain a RULE

- Net is a model that contain a RULE

### model_train_and_test

The complete prediction process, including data pre-processing, model training, testing, and output of scatterplots & confusion matrices. 

Data Preprocessing

> Input:

沖壓機&瞬測儀資料

>>  **data pre-processing**
>>  get X_train: training data (data_num*rate, sequence_num, feature_num)
>>      Y_train: training label (data_num*rate, output_num)
>>      X_valid: validation data (data_num*rate, sequence_num, feature_num)
>>      Y_valid: validation label (data_num*rate, output_num)
>>      X_test: testing data (data_num*(1-rate), sequence_num, feature_num)
>>      Y_test: testing label (data_num*(1-rate), output_num)
>>>Convert the above data into tensor form to feed the model training     

