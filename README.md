# predict_DigitalLiteracy
This repository contains a trained Random Forest (RF) model for predicting the digital literacy of individuals using the best 7-item survey module (referred to as platform-neutral module) described in the paper, _"Validated Digital Literacy Measures for Populations with Low Levels of Internet Experiences."_

- __Paper Authors__: Dr.Ayesha Ali, Dr.Agha Ali Raza, and Dr.Ihsan Ayyub Qazi (LUMS)
- __R code__: This code provides a trained Random Forest (RF) model in the R language
- __Note__: For any questions or comments, please email ihsan.qazi@lums.edu.pk

The repository contains the following files:
- "DL_model.rmd": R file for making predictions from the trained model. It has contains an example.
- "rf_model.rds": Trained RF model
<br>

__The 7 items/questions in the survey module and their response options are as follows:__
 1. _Are you able to search/google things online?_ [Response Options: Yes(1); No(0)]
    
 _How familiar are you with the following computer and Internet-related items? Please choose a number
   between 1 and 5, where 1 represents no understanding and 5 represents full understanding of the item:_
 
 2. _Internet_ [Response Options: 1-5]
 3. _Browser_ [Response Options: 1-5]
 4. _PDF_ [Response Options: 1-5]
 5. _Bookmark_ [Response Options: 1-5]
 6. _URL_ [Response Options: 1-5]
 7. _Torrent_ [Response Options: 1-5]
<br>

__Model Card__
- Input: one or more observations, where each observation correponds to responses to the 7 questions above
- Input Order: (term_pdf, term_internet, term_browser, term_bookmark, term_url, research, term_torrent)
- Output: for each observation the model predicts a digital literacy score between 0 and 1
- Model: A random forest model trained using 100,000 trees. We used the randomForest library in R and employed default values for other hyperparameters.
- Model Performance: R^2 over OOB samples was 0.8 and MSE was 0.019
- Data: The model was trained over a sample of 143 individuals from Pakistan with different levels of digital literacy (please refer to the paper for a detailed description of the model)
- Suitability: The model is best suited for populations with either low levels of Internet experiences or populations compriseing a mix of low and high digital literacy users
