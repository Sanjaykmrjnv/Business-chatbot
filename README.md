# Chatbot UI

This project provides a minimalistic chatbot UI that allows users to interact with a chatbot using Flask and MistralAI. The chatbot uses an indexed PDF document to provide responses to user queries. If a query is outside the scope of the document, the chatbot directs users to contact the business directly.

## Features

- Minimalistic user interface for seamless interaction
- Conversational history maintenance
- Handles out-of-scope questions by directing users to contact the business

## Installation

Follow these steps to set up and run the chatbot:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Sanjaykmrjnv/Business-chatbot.git
   cd Business-chatbot
	```
2. **Install Dependencies:**

Create a virtual environment (optional but recommended):
```bash
	python -m venv venv
	source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
 Install the required packages:
```bash
	pip install -r requirements.txt
```
 
3. **Set Up the Environment:**
 Change directory to src
```bash
 cd Business-chatbot/src
```
Ensure you have a PDF file named **Corpus.pdf** in the src directory. This file will be processed to extract text for the chatbot to use.

4. **Run the Application:**
a. Run extract_text.py for extract text from pdf
```bash
python extract_text.py
```
b. Run the chatbot.py for start the server
```bash
python chatbot.py
```
Open your web browser and navigate to http://127.0.0.1:5000/ to interact with the chatbot.
## Configuration
1. **API Key:**
- Update the **api_key** variable in python app.py with your MistralAI API key.
- To get started, create a Mistral account or sign in at [mistral.ai](https://console.mistral.ai/ "console.mistral.ai").{[doc](https://docs.mistral.ai/ "doc")}

2. **PDF File:**
Place your PDF file as Corpus.pdf in the root directory. The file should contain the content that the chatbot will reference.

## Code Overview
- **chatbot.py**: The main Flask application file that handles routes, processes PDF files, and interacts with MistralAI for querying.
- **templates/index.html**: The frontend HTML file providing a minimalistic user interface for the chatbot.
- **requirements.txt**: Lists all the Python packages required to run the application.

## Troubleshooting
**Dependency Issues:** Ensure all dependencies listed in **requirements.txt** are installed correctly.
**API Key Errors**: Verify that your MistralAI API key is correct and has the necessary permissions.
**PDF Issues**: Make sure** Corpus.pdf** is correctly formatted and located in the root directory
## Future Scope
Here are some ideas for enhancing the chatbot:

- **Enhanced Error Handling:** Implement better error handling and user feedback for more robust interactions.
- **User Authentication:** Add user authentication to personalize interactions and maintain user-specific data.
- **Conversation History:** Implement persistent conversation history to allow users to review previous interactions.
- **Additional Features:** Introduce features like support for multiple languages, improved NLP capabilities, and integrations with other business tools.
