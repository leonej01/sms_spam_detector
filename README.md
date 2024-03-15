## SMS Spam Detector ##
Module 21

**Background**

You'll be refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, you will create a Gradio app to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.
Files

**Challenge Instructions**

The starter files consist of the following files: gradio_sms_text_classification.ipynb, sms_text_classification_solution.ipynb, and SMSSpamCollection.csv.

**Create the SMS Classification Function**

1. Using the code in the sms_text_classification_solution.ipynb file, create the sms_classification function in the gradio_sms_text_classification.ipynb by doing the following:
- Set the features variable to the text message column of the DataFrame.
- Set the target variable to the "label" column of the DataFrame.
- Split data into training and testing and set the test_size to 33%.
- Build a pipeline to transform the test set to compare to the training set.
- Fit the model to the transformed training data and return model.
2. Load the SMSSpamCollection.csv into a DataFrame and call the sms_classification function with the DataFrame, and set the result to the "text_clf" variable.

**Create the SMS Prediction Function**

Use the sms_prediction function to predict the classification of a new text by doing the following:
1. Create a variable that will hold the prediction of a new text.
2. Use a conditional statement that determines if the text message is "ham" or “spam”.
- If the message is “ham”, the function should return the following message: f'The text message: "{text}", is not spam.'
- If the message is spam, the function should return the following message: f'The text message: "{text}", is spam.'

**Create the Gradio Interface Application**

1. Create a Gradio Interface application that takes a textbox for the inputs and has a textbox for the output. The textboxes should have labels that describe what each textbox contains.
2. Launch the application and provide the URL to share the application. Your application should look like the following:
<img width="777" alt="image" src="https://github.com/leonej01/sms_spam_detector/assets/148738322/4f1fe5b6-3e1f-47a3-a65b-634a716a38e3">

The SMS prediction Gradio application interface

Use the following text messages to test your application.
<img width="811" alt="image" src="https://github.com/leonej01/sms_spam_detector/assets/148738322/af042d9a-ab26-401b-bf13-458c16d32130">


