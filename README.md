About the Chatbot<br>
In this project, we are going to build a chatbot for pharmacy using deep learning techniques. The chatbot will be trained on the dataset which contains categories (intents), pattern and responses. We use a special recurrent neural network (LSTM) to classify which category the user’s message belongs to and then we will give a random response from the list of responses. Also, this chatbot uses the Excel file which contains assortment of the pharmacy to answer whether medicaments are available in the stock, if yes, provide the price, available quantity, due to and manufacturer.

We create a retrieval based chatbot using NLTK, Keras, Python, etc.

The dataset we will be using ‘intents_tj_ru.json’. This is a JSON file that contains the patterns we need to find and the responses we want to return to the user in three languages(english, russian and tajik).

How to Make Chatbot<br>
We build the chatbot using Python but first, let us see the file structure and the type of files.

ChatBot.ipynb - This file contains all the code in Jupyter Notebook.
Intents_tj_ru.json – The data file which has predefined patterns and responses in three languages.
Product.xlsx - This file contains the medicaments(products) in the pharmacy stock.

These files will be created after running the code.
Words.pkl – This is a pickle file in which we store the words Python object that contains a list of our vocabulary.
Classes.pkl – The classes pickle file contains the list of categories.
Chatbot_model.h5 – This is the trained model that contains information about the model and has weights of the neurons.

Here are the 5 steps to create a chatbot in Python from scratch:

Import and load the data file
Preprocess data
Create training and testing data
Build the model
Predict the response

1. Import and load the data file

We import the necessary packages for our chatbot and initialize the variables we will use in our project.

The data file is in JSON format so we use json package to parse the JSON file into Python.

2. Preprocess data

When working with text data, we need to perform various preprocessing on the data before we make a machine learning or a deep learning model. Based on the requirements we need to apply various operations to preprocess the data.

Tokenizing is the most basic and first thing you can do on text data. Tokenizing is the process of breaking the whole text into small parts like words.

Lemmatizing is the process of converting a word into its lemma form and then creating a pickle file to store the Python objects which we will use while predicting.


3. Create training and testing data

We create the training data in which we will provide the input and the output. Our input will be the pattern and output will be the class our input pattern belongs to. But the computer doesn’t understand text so we will convert text into numbers.


4. Build the model

When we have our training data ready, we will build a deep neural network that has 3 layers. We use the Keras sequential API for this. After training the model for 200 epochs, we will achieve 100% accuracy on our model. Let us save the model as ‘chatbot_model.h5’.


5. Predict the response (Graphical User Interface)

To predict the sentences and get a response from the user to let us code the following.

We will load the trained model and then use a graphical user interface that will predict the response from the bot. The model will only tell us the class it belongs to, so we will implement some functions which will identify the class and then retrieve us a random response from the list of responses.

We import the necessary packages and load the ‘words.pkl’ and ‘classes.pkl’ pickle files which we have created when we trained our model:

We read the medicaments from Excel file. The excel file was extracted using pharmacy software.

After predicting the class, we will get a random response from the list of intents.

We will develop a graphical user interface. Let’s use Tkinter library which is shipped with tons of useful libraries for GUI. We will take the input message from the user and then use the helper functions we have created to get the response from the bot and display it on the GUI.

The program will open up a GUI window within a few seconds. With the GUI you can easily chat with the bot.

Summary
In this project, we understood about chatbots and implemented a deep learning version of a chatbot in Python which is accurate. You can customize the data according to business requirements and train the chatbot with great accuracy. Chatbots are used everywhere and all businesses are looking forward to implementing bot in their workflow.


