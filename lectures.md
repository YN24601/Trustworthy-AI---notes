# TRUSTWORTHY AI

- [TRUSTWORTHY AI](#trustworthy-ai)
  - [Lecture 1: Introduction](#lecture-1-introduction)
    - [4 schools of thought](#4-schools-of-thought)
    - [Ethical AI principles for Trust \& Fairness](#ethical-ai-principles-for-trust--fairness)
    - [Guidelines of European Commission](#guidelines-of-european-commission)
    - [Laws of Robotics](#laws-of-robotics)
    - [Terminology](#terminology)
  - [Exercise 1](#exercise-1)
  - [Lecture 2: Basics of GenAI](#lecture-2-basics-of-genai)
    - [GenAI vs. Discriminative ML](#genai-vs-discriminative-ml)
    - [Prototypical architectures of current GenAI](#prototypical-architectures-of-current-genai)
      - [Supervised Learning: Logistic Regression](#supervised-learning-logistic-regression)
      - [Neural Networks](#neural-networks)
      - [Transformer](#transformer)
    - [LLM](#llm)
    - [Inference and Decoding Algorithms](#inference-and-decoding-algorithms)
  - [Exercise 2](#exercise-2)

## Lecture 1: Introduction

### 4 schools of thought

||humanly|rationaly|
|--|--|--|
|think|cognitive modelling|"laws of thought" and logical reasoning.|
|act|Turing Test|Focused on acting to achieve the best outcome given the circumstances.|

### Ethical AI principles for Trust & Fairness

AI4People group presented five core ethical principles in 2018 to guide the development of a "good AI society"

- Non-maleficence: AI should not cause harm, including allocational, representational, or psychological harms.
- Beneficence: AI should "do good" and its benefits should outweigh potential harms.
- Autonomy: AI should respect a person's ability to make their own decisions based on informed consent.
- Justice: AI should act in a just and unbiased way.
- Explicability: It should be possible to explain how an AI arrived at a conclusion, involving both intelligibility (human understanding) and accountability (responsibility).

### Guidelines of European Commission

Accroding to the guidline, Trusworthy AI should be:

- Lawful: Respecting all applicable laws and regulations.
- Ethical: Respecting ethical principles and values.
- Robust: Being technically sound while considering the social environment.

They put forward 7 key requirements that AI systems must meet to be deemed trustworthy:

- Human agency and oversight.
- Technical robustness and safety.
- Privacy and data governance.
- Transparency.
- Diversity, non-discrimination, and fairness.
- Societal and environmental well-being.
- Accountability.

### Laws of Robotics

1. First Law: A robot may not injure a human being or, through inaction, allow a human being to come to harm.

2. Second Law: A robot must obey orders given by humans, except where such orders conflict with the First Law.

3. Third Law: A robot must protect its own existence as long as it does not conflict with the First or Second Law

4. Zeroth Law: A robot may not harm humanity, or, by inaction, allow humanity to come to harm.

### Terminology

- **GenAI**:A computational system that acts intelligently, and is able to generate text, imaes, videos or other media.
- **AI Ethics** provides the moral principles.
- **Trustworthy AI**: Systems that translate moral principles into design requirements. e.g. [European Commission](#guidelines-of-european-commission)

- **AI Governance** refers to the institutions, policies, and regulatory mechanisms that ensure AI systems are developed and used responsibly.
- **AI Safety** ensures systems do not cause harm through failure or misalignment.
- **AI Alignment** focuses on ensuring AI systems behave in ways aligned with human intentions and values.
- **AI Security** ensures systems cannot be manipulated or abused by attackers.

## Exercise 1

1. Linear Algebra & Neural Representations
   - Dot Product & Cosine Similarity
   - Softmax Function
2. Probability & Language Modeling
   - Bayes’ Theorem
   - Markov Assumption
   - Chain Rule of Probability
3. Statistics & Significance Testing
   - Z-test
   - P-values
   - Confidence Intervals
   - Bootstraping
4. Information Theory & Optimization
   - Entropy ($H$)
   - Cross-Entropy
   - KL Divergence ($D_{KL}$)
   - Gradient Descent
5. Evaluation Metrics & Robustness
   - Confusion Matrix
   - Precision vs. Recall
   - F1 score

## Lecture 2: Basics of GenAI

### GenAI vs. Discriminative ML

- Discriminative ML: Given an input, predict the output (e.g. classification, regression). It focus on decision boundary and the probability $P(y|x)$.
- GenAI: Focus on the structure and patterns (or to say, the distribution) of the data. Focus on $P(x)$ or $P(x,y)$, to produce new data.

### Prototypical architectures of current GenAI

Gen AI is mainly based on ML，using algorithorm to discover Patterns and structure from data/example.

#### Supervised Learning: Logistic Regression
   - Sigmoid function (the standards logistic function): to output probability (0,1) (normolized)
   - Loss function (cross-entropy): measure the difference between the predicted probability and the true label.
   - use gradient descent to update w and b

#### Neural Networks

   Logistic regression only has one layer, and the input and output are linearly related. So we use neural networks to add more layers to make the model more complex (non-linear decision boundary).

- mutiple layers
- activation function (e.g. ReLU, Sigmoid, Softmax), to make the model non-linear

#### Transformer

- Input: sequence of tokens, embedding
- Encoder:
  - to find the best representation of the input
  - Self-attention, Feed Forward Neural Network
- Decoder:
  - to generate the output
  - Self-attention, Feed Forward Neural Network, Cross-attention (Encoder-Decoder attention)
- Output: sequence of tokens based on the calculated probability

**Self-attention** is a mechanism that allows the model to focus on different parts of the input sequence when making predictions. It is the **key component of the Transformer** model.
   > e.g. "The cat's name is Tom. He... ", the model should aware that 'He' refers to 'Tom'

- Input: a sequence of tokens
- Calculate query (Q), key (K), and value (V) vectors for each token
- Weight (Attention Score): calculate the similarity (dot product) between Q and K
- Output (Weighted Sum): calculate the weighted sum of the V vectors, as the output

### LLM

- Pretraining: autoregressive language modeling based on large corpus, to learn to predict next token
- Instruction tuning: supervised fine-tuning(SFT) the pre-trained model on a specific task (e.g. text classification, question answering, etc.), to make the model learn to follow the instruction.
- Alignment training: perference learning using RLHF

### Inference and Decoding Algorithms

There are some algorithms to generate the output sequence.

- greedy search
- beam search
- random sampling
  - temperature sampling
  - top-k samplinp

## Exercise 2

