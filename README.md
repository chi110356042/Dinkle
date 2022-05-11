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
>Input : Stampers & Transient Testers Data
>>**Get Data**  
>>    X_train: training data (data_num*rate, sequence_num, feature_num)  
>>    Y_train: training label (data_num*rate, output_num)  
>>    X_valid: validation data (data_num*rate, sequence_num, feature_num)  
>>    Y_valid: validation label (data_num*rate, output_num)  
>>    X_test: testing data (data_num*(1-rate), sequence_num, feature_num)  
>>    Y_test: testing label (data_num*(1-rate), output_num)  
>>>_Convert the above data into tensor form to feed the model training_      
>>>_Create TensorDataset by DataLoader_   

>Output :
> - training data
> - validation data
> - testing data  

**2.Model training**
>Input : Training data & validation data   
>Output : model.pt   

**3.Testing**
> Input : Testing data  
>> - If you didn't run testing right after training model, then you need to load model first  
>> `model_eval=torch.load(model.pt)`  
 
> Output : 
> - test.csv : Include data, true value, predicted value, true good/bad product, predicted good/bad product
> - Accuracy : Include accuracy rate, yield accuracy rate, defective accuracy rate  
> - X_test_correct & X_test_wrong : Predict correct/incorrect testing data 
> - Scatterplots  
> - Confusion matrices  




     

