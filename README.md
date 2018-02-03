# chat-bot
Seq2seq chatbot model trained on pytorch, character by character on the movie dialog corpus.

Model can be trained by batches, and use embeddings for each character.

Find notebook on: https://github.com/manuelsh/chat-bot/blob/master/notebooks/chatbot_model.ipynb

On greedy search his main answer is "I don't know". If we change the decision of the next character by randomly taking a character using the output softmax as a distribution, some funny answers arise, which are mostly grammatically correct.

Note that the model is trained only with 45k parameters, which is possibly too little for a word by word model.

# TODO
- Try beam search.
- Increase the number of parameters, current bottleneck is GPU memory. Maybe use gradient checkpointing.
