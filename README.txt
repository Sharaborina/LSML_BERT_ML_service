Project documentation
1. problem statement
2. model
3. architecture for the resulting service
4. how to use the service



1.This ML-service uses a pretrained BERT model (BertForMaskedLM), which predicts a masked word.
(BERT: Bidirectional Encoder Representations from Transformers. It’s a language representation model created by Google researchers)

Problem statement: to find out what word can be hidden behind the word "MASK" (a special token).


2. Model: BertForMaskedLM.
Input and output description: input - text (type: str); the output would be several words with weights (how likely a particular word can be used in that sentence).

Model loss: 0.8769 


3. Architecture for the resulting service: A python telegram bot framework based on Flask (a light-weight Python web framework that gets use of Werkzeug toolkit and Jinja2 template engine).
This bot acts as a relay between server and Telegram.
Docker: synchronous projects (Flask)
Client: Telegram Bot


4. Chat Bot name: LSML2_final_project_Sharaborina
To run the bot: 1) clone the repository 2) open folder LSML_BERT_ML_service 3) run this command: docker-compose build && docker-compose up  
4) find the bot  5) type command /start 6) type sentence (for example, "My [MASK] is so cute.")
