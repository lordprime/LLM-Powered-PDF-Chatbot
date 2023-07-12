# LLM Powered PDF ChatBot

This is a demostration on how we can use a LLM model to create an interactive version of a PDF.
This system has an added advantage of making it even more usable.

## Requirements
- The components from the requirements.txt file
- A OpenAI API key.

## Working

![Working](https://github.com/lordprime/LLM-Powered-PDF-Chatbot/assets/93172671/cea0ec35-62d7-48ad-b278-cb2da41d5827)

The system uses 3 Modules:
- ChatGPT Embeddings 
- LangChain
- Streamlit

### ChatGPT Embeddings
ChatGPT embeddings are a fundamental component of the language model that enable it to understand and process text. Embeddings are numerical representations of words or phrases that capture their semantic and syntactic properties. In the case of ChatGPT, the model uses contextual embeddings, which means that the representation of a word depends on its surrounding context. This allows ChatGPT to capture the nuances and meaning of words within the specific context of a conversation. By leveraging these embeddings, ChatGPT can generate responses that are coherent, relevant, and aligned with the input it receives. The embeddings serve as a bridge between the raw text and the underlying neural network, enabling the model to effectively learn and generate human-like responses.

These embeddings can be stored within a vector database to be used with LangChain.

### LangChain
LangChain is a python module that mainly focusses on connecting LLM models with a much more systems for better integrations.
LangChain in our case uses the OpenAI embeddings and then converts all the text into chunks and then adds them to the Vector Database.
The embeddings are then checked with the AI and then the data is analyzed accordingly based on the querys asked.

### StreamLit 
Streamlit is a GUI interface which uses markdown and and HTML to make developing interfaces easy and fast. Working with it is also really simple as all of the major code and backend routing and request handeling is done automatically making development quick and simple.

### Core Working
The core working can be explained in steps:
- **Step 1 Taking Inputs:** The Inputs that are taken are the PDF files and the API key.
- **Step 2 Assign and Extract:** The API key is kept in the session enivorment and the PDF text data is extracted.
- **Step 3 Chunks and Embeddings:** The Text data extracted is generated into chunks of 1000 tokens and then this list of text is converted into embeddings.
- **Step 4 Prompting and conversation:** The generated embeddings are then conversed with OpenAI API key with the prompt or question asked by the user to check for an answer.
- **Step 5 Return the answer:** After finding the answer its sent back to the user.

## Result

This is a result image:
![image](https://github.com/lordprime/LLM-Powered-PDF-Chatbot/assets/93172671/2d38fcd1-d9eb-415a-a7be-976760ced129)
![image](https://github.com/lordprime/LLM-Powered-PDF-Chatbot/assets/93172671/3867ac87-67c3-4df6-8092-94fe07a1db1b)

