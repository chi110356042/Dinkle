# Dinkle

This project is NCCU cooperation with Dinkle, which used LSTM to predict product quality.

## Description

### model

Complete model that can be directly loaded for use.

- set α, β = 0.1

`prediction = model(test_data, alpha=0.1, beta=0.1)`

### model_code

Complete model development program.

- DataonlyNet is a model that does not contain a RULE

- Net is a model that contain a RULE

### model_train_and_test

The complete prediction process, including data pre-processing, model training, testing, and output of scatterplots & confusion matrices. 

**1.Data pre-processing**
>Input : 沖壓機&瞬測儀資料
>>**Get Data**  
>>    X_train: training data (data_num*rate, sequence_num, feature_num)  
>>    Y_train: training label (data_num*rate, output_num)  
>>    X_valid: validation data (data_num*rate, sequence_num, feature_num)  
>>    Y_valid: validation label (data_num*rate, output_num)  
>>    X_test: testing data (data_num*(1-rate), sequence_num, feature_num)  
>>    Y_test: testing label (data_num*(1-rate), output_num)  
>>>Convert the above data into tensor form to feed the model training      
>>>Create TensorDataset by DataLoader   

>Output : train_loader&validation_loader&test_loader  

**2.Model training**
>Input : Training data  
>Output : Model.pt   

**3.testing**
> Input : Testing data  
>> - If you didn't run testing right after training model, then you need to load model  
>> `model_eval=torch.load(model.pt)`  
 
> Output : 
- test.csv : Include data, true value, predicted value, true good/bad product, predicted good/bad product
- Accuracy : IncludeAccuracy Rate, Yield Prediction Accuracy Rate, Defect Prediction Accuracy Rate  
- X_test_correct & X_test_wrong : 預測正確/錯誤的testing data  
- scatterplots  
- Confusion matrices  




     

