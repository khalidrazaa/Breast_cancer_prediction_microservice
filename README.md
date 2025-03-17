# Welcome to my ML model deployement project
* ML model to detect Breast Cancer
* An ensemble of three model is used and exported as *dat.gz
    - Logistic Regression
    - Decision Tree Classifier
    - Support Ventor Classifier

* /data hold the dataset
* code_model_training/train.py has program to :
    - load the dataset 
    - split for training and testing
    - train the models
    - create emsemble
    - print confusion metrix
    - Finaly save the model to use for deployement 
* / app.py has program to run back-end flask app
    - '/info', returns details of the model like name and version
    - '/health', returns ok as app health confirmation
    - '/predict', will take json data and predict the result

* Docker file is configured to create a container image to install the package listed in requirement.txt and run this flask app on 'gunicorn' WSGI engine as production app.