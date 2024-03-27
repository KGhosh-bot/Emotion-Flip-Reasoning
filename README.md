# Emotion-Flip-Reasoning
Emotion Discovery and Reasoning its Flip in Conversation (EDiReF), SemEval 2024 Task 10 SUBTASK iii (English dialogues only) 

The data contains 4000 short English dialogues: from 5 to 17 utterances

## Data
"emotions":
[
   "neutral",
   "surprise",
   "neutral",
   "surprise",
   "neutral",
   "anger"
],

"utterances":
[
   "Yes that's right.",
   "Why?",
   "I tired attacking two women, did not work.",
   "What?!",
   "No, I mean it's okay, I mean, they're-they're my friends.",
   "In fact, I-I-I was married to one of them."
],

"triggers":
[
   0.0,
   0.0,
   1.0,
   0.0,
   1.0,
   1.0
]

## Modeling

We train and evaluate a BERT `bert-base-uncased` baseline on two different settings:

     - Freezed: we freeze the BERT embedding layer weights and fine-tune the classifier heads on top
     
     - Full: we fine-tune the whole model architecture. Make sure you set a small enough batch size. 
                We recommend 1.

We also evaluate a random and a majority classifier for emotions and triggers and report a comparison with the selected model(s) and the baselines.

## Metrics

We report the following metrics for model evaluation.

     Sequence F1: compute the f1-score for each dialogue and report the average score.

     Unrolled Sequence F1: flatten all utterances and compute the f1-score.

We compute the above metrics for emotions and triggers labels.

To assess model robustness and report a sound evaluation, we train and evaluate your model(s) on 5 different seeds.

We report all metrics' average and standard deviation computed over the 5 seeds.


