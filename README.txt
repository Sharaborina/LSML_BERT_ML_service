Project documentation
1. problem statement
2. model
3. architecture for the resulting service



1.This ML-servise uses a pretrained BERT model, which predicts a masked word.
(BERT: Bidirectional Encoder Representations from Transformers. It’s a language representation model created by Google researchers)

Problem statement: to find out what word can be hidden behind the word "MASK" (a special token).


2. Model: BertForMaskedLM.
Input and output description: input - text (type: str); the output would be several words with weights (how likely a particular word can be used in that sentence).

Model loss: 0.8769 


3. Architecture for the resulting service: A python telegram bot framework based on Flask (a light-weight Python web framework that gets use of Werkzeug toolkit and Jinja2 template engine).
This bot acts as a relay between server and Telegram.
Docker: synchronous projects (Flask)
Client: Telegram Bot

