# NBA-PAR-LSTM
This GPT-4 assisted project predicts the next game performance of an NBA player using a simple LSTM model. 


NBA PAR Prediction using LSTM

Description

This project uses a simple LSTM model to predict the next number in a series of NBA player performance statistics, such as points, assists, rebounds, and three-pointers made. The program fetches the required data for a specific player by scraping a webpage and then trains the LSTM model on the data to make predictions.

Dependencies

Python 3.x
Requests
BeautifulSoup
NumPy
Matplotlib
TensorFlow

How it works:

Web scraping: The program fetches the required data for a specific player from a webpage using the requests library and BeautifulSoup. The user needs to provide the URL of the webpage and the CSS selectors for the elements containing the data. The fetch_data function scrapes the data and returns a dictionary containing the player's points, assists, rebounds, and three-pointers made.

Data preparation: The program processes the fetched data and combines it with the existing data for each performance statistic (points, assists, rebounds, and three-pointers made). The input data is then split into input and output sequences using the prepare_data function.

LSTM model training and prediction: The LSTM model is trained using the input and output sequences. The train_and_predict_next_number function defines the LSTM model, compiles it with the Adam optimizer and Huber loss, fits the model to the input and output sequences, and makes a prediction for the next value in the input sequence.
Output: The predicted next numbers in the sequence sets are printed to the console, showing the player's predicted performance in the next game.

Usage:

Install the required dependencies using pip:

pip install requests beautifulsoup4 numpy matplotlib tensorflow

Update the url, player_name, and appropriate CSS selectors in the code to match the webpage you want to scrape.

Run the script:

python nba_player_performance_prediction.py

The program will output the predicted next numbers in the sequence sets, representing the player's predicted performance in the next game.
