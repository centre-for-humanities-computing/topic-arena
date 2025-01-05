# topic-arena
An arena for comparing topic model quality.

## What do we want from a topic model:

1. Sensible overview:
   - Should be **representative** of the documents: As many documents' content should be covered as possible. (Task 1)
   - Should be **informative**: You should gain as much information about the corpus as possible. (*TODO* find relevant task)
   - Should be **corpus specific**: You should gain information about *this* corpus, and preferably not just about general themes. (Task 3)
2. Getting into the weeds - Filtering/Retrieval
   - Should get **relevant** documents when retrieving based on one topic (Task 2)
3. Discourse analysis (dynamic models, optional)

## Tasks

### Task 1

You get a document annotated by two topic models. You are presented with the highest scoring topics and their topic descriptions. You should choose which model's output you prefer.
We should try accounting for *atypical* documents as well when doing this so that we see how representative models are.

### Task 2

Take a single topic model and sample four documents that rank sufficiently differently on the topic.
Rank the four documents in the order that you think they are relevant to the topic.
We can then use some reranking metric.

### Task 3

1. Fit two topic models on the same corpus.
2. Choose a very similar *intruder corpus* (perhaps an adjacent category in Wiki hierarchy).
3. Display the topic descriptions from both models.
4. Draw an intruder document from the intruder corpus.
5. Tell the participant to choose which model the document belongs to.
6. If one model gets more intruder documents assigned it means that it is less specific to that corpus.
