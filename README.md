
CHATBOT USING FLASK AND LANGCHAIN
This repository includes a chatbot application that makes use of the Hugging Face models for conversational AI and was developed with the LangChain framework. The program runs in a Google Colab environment and has a RESTful API created with Flask. The chatbot's purpose is to retrieve and reply to user inquiries using information that has been taken from a designated website.

Table of Contents
Overview
Features
Installation
How to Use
Technical Details
Dependencies
Notes
License


Overview
This chatbot responds to user inquiries using web-scraped data by utilizing LangChain's Conversational Retrieval Chain. A RESTful API is available for access to the application, which is hosted on a Flask server. The chatbot is exposed to the internet over ngrok and is intended to operate within a Google Colab environment.


 
Features
Web scraping with WebBaseLoader from LangChain.
Sentence Transformers are used for text splitting and embedding generation.
Vector storage using FAISS.
AI conversational utilizing the GPT-2 model from Hugging Face.
RESTful API for chatbot interactions based on Flask.
Ngrok integration to expose a public URL.


Installation
Clone the repository:
git clone https://github.com/yourusername/your-repository.git
cd your-repository

Configure the surroundings: The intended setting for this application is Google Colab. Make sure a Colab notebook is prepared to run the ensuing tasks.
Install the required packages: In the Colab notebook, execute the following commands to install the necessary Python packages:
!pip install flask-ngrok
!pip install langchain sentence_transformers faiss-cpu flask flask_restful requests beautifulsoup4 transformers torch

How to use
Launch the chatbot: Run the script by copying it into a Google Colab notebook cell. This will launch a Flask server and use ngrok to expose it.
Engage with the chatbot: You can type your questions into the Colab notebook to engage with the chatbot directly. To end the chat, type "exit."

Technical Specifics
Data Extraction: Using WebBaseLoader, the bot extracts data from a given URL.
Text Processing: CharacterTextSplitter is used to divide the scraped data into digestible portions.
Embeddings: The "all-MiniLM-L6-v2" model is used to generate embeddings using HuggingFaceEmbeddings.
Hugging Face's GPT-2 model, which is incorporated into LangChain as a HuggingFacePipeline, powers the chatbot.
API: To communicate with the chatbot, use the single endpoint /chat that is exposed by the Flask RESTful API.

Dependencies
Python 3.x
Flask
Flask-RESTful
ngrok
LangChain
Hugging Face Transformers
Sentence Transformers
FAISS

Notes
Your code will run much faster on Google Colab with a GPU runtime, which will improve the chatbot's response time.
Every time you launch the notebook, the ngrok URL will change, thus if needed, be sure to inform any clients of the new URL.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

