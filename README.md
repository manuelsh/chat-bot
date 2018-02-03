# Pytorch seq2seq chat-bot

Seq2seq chatbot model trained on pytorch, character by character on the movie dialog corpus.

Model can be trained by batches, and use embeddings for each character.

Find notebook on: https://github.com/manuelsh/chat-bot/blob/master/notebooks/chatbot_model.ipynb

On greedy search his main answer is "I don't know". If we change the decision of the next predicted character by randomly choosing it using the output softmax as a distribution, some funny answers arise, which are mostly grammatically correct. See notebook.

Note that the model is trained only with 45k parameters (due to GPU memory bottleneck), which is possibly too little for a character by character model.

## Some silly examples to the question: "Where is she?"

```
thanks father.<end>

a couple of tough thing tent scrotssides. found your table set my hair.<end>

i don't know. i just only tell us.  that cold dollars relaced with you. had me exactly all say in my reaction. 'anard bag --

oh oh gere.<end>

soon.<end>

i'm gonna be picked by where.<end>

are you going on??<end>
  
i love what i tell you...<end>

sorry.  i've got to beat you some lame with me--walter has nothing to do to you.<end>

look at you.<end>

early!  pu... i really said posesie ma.  jesus! take father t. thanks... corruction ...<end>
```

## To do
- Add beam search.
- Add attention mechanism.
- Increase number of parameters potentially using gradient checkpointing.

