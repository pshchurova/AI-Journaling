# Reflective Journaling Chatbot

This is a Python-based chatbot that uses OpenAI's GPT-4 model to generate reflective journaling responses. The chatbot
takes user input and generates a response based on the conversation history.

## Setup

To set up and run the chatbot, follow these steps:

1. Install the required packages:

```bash
pip install openai
```

2. Obtain an API key from OpenAI. You can sign up for an API key at https://beta.openai.com/signup/.

3. Save your API key in a file named `key_openai.txt` in the same directory as the chatbot script.

4. Run the chatbot script:

```bash
python chatbot.py
```

## High-Level Description

The chatbot script consists of the following functions:

- `open_file(filepath)`: Opens and reads the content of a file, returning the content as a string.

- `chatbot(messages, model="gpt-4", temperature=0)`: Takes a list of messages as input and generates a response using
the specified model and temperature. The function handles API errors and retries up to a maximum number of attempts.

The main part of the script initializes the chatbot by setting the OpenAI API key and loading the system message from
the `system_reflective_journaling.txt` file. It then enters a loop where it takes user input, generates a response using
the `chatbot()` function, and prints the response.

The conversation history is maintained in the `conversation` list, which is passed to the `chatbot()` function to
generate context-aware responses.
