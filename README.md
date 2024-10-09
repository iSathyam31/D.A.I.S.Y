# D.A.I.S.Y: Digital Assistant for Information and Symptom Yielding
**D.A.I.S.Y.** is a Generative AI-powered medical assistant that helps users identify symptoms and get valuable medical information based on their inputs. With a combination of Generative AI techniques, D.A.I.S.Y. can engage in meaningful conversations with users, providing helpful and informative responses in real-time.

## Project Setup
### Step 1: Creating a Virtual Environment
To set up the project, we recommend using a virtual environment to manage dependencies. Follow the steps below to create and activate your virtual environment.
```
# Create a virtual environment
conda create -p venv python=3.xx -y

# Activate the virtual environment (Windows)
conda activate venv/
```
### Step 2: Project Structure
Here is an overview of the project structure:
```
MEDICAL CHATBOT
│
├── Data
│   └── Medical_book.pdf        # Reference material for medical data.
│
├── src
│   ├── __pycache__             # Python cache folder.
│   ├── __init__.py             # Initial setup file for the src package.
│   ├── helper.py               # Helper functions for the project.
│   ├── prompt.py               # Contains prompts and responses for the chatbot.
│
├── static
│   └── style.css               # CSS file for frontend styling.
│
├── templates
│   └── chat.html               # HTML file for the chatbot's interface.
│
├── venv                        # Virtual environment folder.
├── .env                        # Environment variables (not tracked by Git).
├── .gitignore                  # Files and folders to ignore in version control.
├── app.py                      # Main application file to run the chatbot.
├── LICENSE                     # License for the project.
├── README.md                   # Project documentation (you're reading this!).
├── requirements.txt            # List of dependencies.
├── setup.py                    # Setup file for project dependencies.
├── store_index.py              # Script to store embeddings in Pinecone.
├── template.py                 # Template for chatbot's input/output structure.
└── README.md                   # Project README file (this file).
```
### Step 3: Installing Requirements
Install the required dependencies listed in `requirements.txt`.
```
pip install -r requirements.txt
```
This will install all necessary packages, including frameworks like Flask, Gen AI frameworks, and Pinecone for embedding storage.
### Step 4: Configuring Environment Variables (`.env file`)
You need to set up your `.env` file to store your API keys for Pinecone and the Groq API. Here's how you can configure it:
1. Create a file named `.env` in the project root directory.
2. Add the following environment variables to the `.env` file:
```
PINECONE_API_KEY=<Your_Pinecone_API_Key>
grow_api_key=<Your_Groq_API_Key>
```
###  Step 5: Understanding `template.py`
The `template.py` file is a key component for the bot’s interaction process. It defines the structure of how the chatbot processes user input and returns the appropriate responses.

Make sure you review this file for any customization needed for handling specific medical inputs or responses.
### Step 6: Project Setup (`setup.py`)
The `setup.py` file is used to handle the project’s configuration and installation. Make sure you run the following command to properly set up the project:
```
python setup.py install
```
This will ensure that the project is correctly installed, and all necessary dependencies and modules are linked.
### Step 7: Storing Embeddings with `store_index.py`
Before running the application, you need to store the embeddings in Pinecone, which will allow the chatbot to access and retrieve information efficiently.

Run the following command to index the embeddings:
```
python store_index.py
```
This script will process the medical data and store the embeddings in Pinecone, enabling the chatbot to perform semantic searches and retrieve medical insights based on user queries.
### Step 8: Running the Application (`app.py`)
Once all the previous steps are completed, you can run the application by executing:
```
python app.py
```
This will launch D.A.I.S.Y. chatbot, and you can start interacting with it via the web interface provided by `chat.html`.
