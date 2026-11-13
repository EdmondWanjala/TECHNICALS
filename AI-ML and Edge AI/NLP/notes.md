            NATURAL LANGUAGE PROCESSING (NLP)
Natural Language Processing (NLP) is a field of AI concerned with enabling computers to interact with human languages such as English, Kiswahili, French and other languages.
It allows machines to process written and spoken communication and extract meaningful information.
  Main objectives;
- Understand human language.
- Extract meaning and information from text.
- Identify language patterns and relationships.
- Translate between languages.
- Recognize speech and convert it into text.
- Generate human-like text.
- Classify and summarize documents.
- Enable conversational AI systems.
  Major applications;
- Chatbots and virtual assistants.
- Machine translation.
- Sentiment analysis.
- Speech recognition.
- Text summarization.
- Spam detection.
- Information retrieval.
- Question-answering systems.
- Document classification.
- Large Language Models (LLMs).
  NLP vs NLU vs NLG;
Natural Language Processing (NLP): The broader field of processing and working with human language.
Natural Language Understanding (NLU): Focuses on interpreting meaning, intent, context and relationships in language.
Natural Language Generation (NLG): Focuses on producing meaningful human-language output from data or internal representations.

 LEVELS OF LANGUAGE PROCESSING
NLP systems may analyse language at several levels.
  Phonetics and Phonology;
Study the physical properties and sound patterns of spoken language.
Applications:
- Speech recognition.
- Pronunciation analysis.
- Speech synthesis.
  Morphology;
Studies how words are formed from smaller meaningful units called morphemes.
Example:
"Unhappiness" = un + happy + ness.
Applications:
- Word analysis.
- Language modelling.
- Translation.
  Lexical Analysis;
Examines individual words, their forms and possible meanings.
  Syntax;
Studies grammatical structure and relationships between words in sentences.
Example:
"The engineer designed the robot."
A syntactic parser identifies the grammatical relationships among the words.
  Semantics;
Studies the meaning of words, phrases and sentences.
Example:
"Bank" can refer to a financial institution or the side of a river.
  Pragmatics;
Studies how context and real-world circumstances influence meaning.
Example:
"Can you open the window?" is grammatically a question but pragmatically a request.
  Discourse Analysis;
Studies relationships between sentences and larger sections of communication.
Example: Understanding what a pronoun such as "it" refers to in an earlier sentence.

 TEXT PREPROCESSING
Raw text often contains noise, inconsistent formatting and irrelevant information. Preprocessing prepares it for NLP algorithms.
  Tokenization;
Divides text into smaller units called tokens.
Types:
- Sentence tokenization: Splits text into sentences.
- Word tokenization: Splits text into words.
- Subword tokenization: Splits words into smaller units.
- Character tokenization: Splits text into individual characters.
Example:
Input: "Machine learning is powerful."
Tokens: ["Machine", "learning", "is", "powerful", "."]
Modern language models commonly use subword tokenization.
  Lowercasing;
Converts text into lowercase to reduce differences caused by capitalization.
Example:
"Machine Learning" → "machine learning".
This is not always appropriate because capitalization can carry meaning, such as names and acronyms.
  Stop-word removal;
Removes frequently occurring words considered less informative for a particular task.
Examples: "the", "is", "and", "of".
Important: Stop-word removal is task-dependent. It can remove important information, especially in sentiment analysis and language modelling.
  Stemming;
Reduces words to approximate root forms by removing prefixes or suffixes.
Example:
- Playing → play
- Connected → connect
- Studies → studi (depending on the algorithm)
Stemming may produce words that are not valid dictionary words.
  Lemmatization;
Converts words into their meaningful dictionary base forms using linguistic information.
Examples:
- Running → run.
- Better → good.
- Studies → study.
Lemmatization is generally more linguistically accurate than stemming.
  Removing noise;
May involve removing:
- Unnecessary punctuation.
- HTML tags.
- Irrelevant symbols.
- Duplicate content.
- Unwanted formatting.
- Unnecessary whitespace.
Cleaning must preserve information relevant to the task.

 TEXT REPRESENTATION AND VECTORIZATION
Machine learning algorithms generally require numerical input. Text must therefore be converted into numerical representations.
  One-Hot Encoding;
Represents each word using a binary vector in which one position is 1 and all others are 0.
Example vocabulary:
[cat, dog, car]
Cat = [1,0,0]
Dog = [0,1,0]
Car = [0,0,1]
Limitation: Produces sparse, high-dimensional vectors and does not represent semantic similarity.
  Bag of Words (BoW);
Represents a document using the frequency of words, ignoring their order.
Example:
Document: "AI is useful. AI is powerful."
Vocabulary: [AI, is, useful, powerful]
Vector: [2,2,1,1]
Applications:
- Text classification.
- Spam detection.
- Document analysis.
  Term Frequency (TF);
Measures how frequently a term occurs in a document.
    TF(t,d) = Number of occurrences of t in d / Total terms in d
  Inverse Document Frequency (IDF);
Measures how rare or informative a term is across a collection of documents.
    IDF(t) = log(N/df(t))
Where:
- N = Total number of documents.
- df(t) = Number of documents containing term t.
  TF-IDF;
Combines term frequency and inverse document frequency to estimate the importance of a word in a document relative to a collection.
    TF-IDF(t,d) = TF(t,d) × IDF(t)
Frequently used for:
- Information retrieval.
- Search engines.
- Document classification.
- Keyword extraction.
  Word Embeddings;
Represent words as dense numerical vectors that capture semantic and contextual relationships.
Words with related meanings may have similar vector representations.
Examples:
- Word2Vec.
- GloVe.
- FastText.
Advantages:
- Represent semantic relationships.
- Reduce sparse dimensionality.
- Support similarity calculations and downstream ML tasks.
  Contextual Embeddings;
Unlike traditional static word embeddings, contextual embeddings represent a word according to its surrounding context.
Example:
"I deposited money at the bank."
"We sat on the river bank."
The word "bank" receives different representations depending on its context.
Used in transformer-based language models.

 IMPORTANT NLP TASKS
  Text Classification;
Assigns text to predefined categories.
Examples:
- Spam or legitimate email.
- Positive, negative or neutral sentiment.
- News category classification.
- Topic classification.
Algorithms:
- Naive Bayes.
- Logistic Regression.
- Support Vector Machines.
- Neural Networks.
- Transformers.
  Sentiment Analysis;
Identifies opinions, emotions or attitudes expressed in text.
Common classes:
- Positive.
- Negative.
- Neutral.
Applications:
- Customer feedback analysis.
- Product reviews.
- Social media monitoring.
- Market research.
Advanced sentiment analysis may identify emotions such as happiness, anger and frustration.
  Named Entity Recognition (NER);
Identifies and classifies important entities in text.
Common entity types:
- PERSON: Names of people.
- ORGANIZATION: Companies and institutions.
- LOCATION: Places.
- DATE: Dates.
- MONEY: Monetary values.
- PRODUCT: Product names.
Example:
"Microsoft opened an office in Nairobi in 2025."
Entities:
- Microsoft → ORGANIZATION.
- Nairobi → LOCATION.
- 2025 → DATE.
  Part-of-Speech Tagging (POS);
Assigns grammatical categories to words.
Examples:
- Noun.
- Verb.
- Adjective.
- Adverb.
- Pronoun.
- Preposition.
- Conjunction.
Example:
"The engineer designs robots."
Engineer → Noun.
Designs → Verb.
Robots → Noun.
  Machine Translation;
Automatically translates text from one language into another.
Example:
English → Kiswahili.
Applications:
- Multilingual communication.
- Document translation.
- International information access.
  Text Summarization;
Produces a shorter representation of a longer document while preserving important information.
Types:
Extractive summarization: Selects important sentences directly from the original text.
Abstractive summarization: Generates new sentences that express the main ideas.
  Question Answering;
Processes a question and generates or retrieves an appropriate answer from available information.
Applications:
- Intelligent assistants.
- Educational systems.
- Document search.
- Customer support.
  Information Extraction;
Automatically identifies structured information from unstructured text.
Example: Extracting names, dates, addresses and transaction details from documents.
  Language Generation;
Produces human-readable text based on an input, prompt or internal representation.
Applications:
- Chatbots.
- Report generation.
- Email drafting.
- Code generation.
- Automated documentation.
  Speech Recognition;
Converts spoken language into written text.
Also called Automatic Speech Recognition (ASR).
Applications:
- Voice assistants.
- Voice-controlled robots.
- Dictation systems.
- Automated transcription.
  Text-to-Speech (TTS);
Converts written text into synthesized speech.
Applications:
- Accessibility systems.
- Navigation assistants.
- Voice interfaces.
- Human-machine interaction.

 LANGUAGE MODELS
A language model is a computational model that learns statistical or contextual patterns in language to estimate the likelihood of sequences of tokens and support language-related tasks.
  N-gram models;
Predict a word based on a fixed number of preceding words.
Types:
- Unigram: One-word probabilities.
- Bigram: Depends on one preceding word.
- Trigram: Depends on two preceding words.
General probability:
    P(w₁,w₂,...,wₙ) ≈ ∏ᵢ P(wᵢ | preceding context)
N-gram models are relatively simple but struggle with long-range dependencies and unseen word sequences.
  Neural Language Models;
Use neural networks to learn language patterns.
Examples:
- Feedforward language models.
- Recurrent Neural Networks.
- LSTM and GRU networks.
- Transformer models.
  Large Language Models (LLMs);
Large Language Models are neural language models trained on extensive text datasets, commonly using transformer architectures.
They can perform:
- Text generation.
- Summarization.
- Translation.
- Question answering.
- Reasoning-like language tasks.
- Code generation.
- Information extraction.
LLMs generate responses based on learned patterns and provided context. Their outputs may contain factual errors or fabricated information and should be verified when accuracy matters.

 RECURRENT NEURAL NETWORKS (RNNs)
RNNs are neural networks designed to process sequential data by maintaining information from previous time steps.
They are useful for language, speech and time-series applications.
Basic RNN equation:
    hₜ = f(Wₓxₜ + Wₕhₜ₋₁ + b)
Where:
- hₜ = Current hidden state.
- xₜ = Current input.
- hₜ₋₁ = Previous hidden state.
- Wₓ and Wₕ = Weight matrices.
- b = Bias.
- f = Activation function.
  Limitations of basic RNNs;
- Vanishing gradients.
- Exploding gradients.
- Difficulty learning long-range dependencies.
- Sequential computation can limit parallelism.
  LSTM (Long Short-Term Memory);
An improved RNN architecture designed to retain important information over longer sequences.
Uses:
- Forget gate.
- Input gate.
- Output gate.
- Cell state.
  GRU (Gated Recurrent Unit);
A simplified gated recurrent architecture using:
- Update gate.
- Reset gate.
Both LSTM and GRU help address limitations of traditional RNNs.

 TRANSFORMERS AND ATTENTION MECHANISMS
Transformers are neural network architectures that process sequences using attention mechanisms rather than relying primarily on sequential recurrent processing.
They form the foundation of many modern language models.
  Attention mechanism;
Allows a model to determine which parts of an input sequence are most relevant when processing a particular token.
  Self-attention;
Computes relationships between tokens within the same sequence.
Scaled dot-product attention:
    Attention(Q,K,V) = softmax(QKᵀ/√dₖ)V
Where:
- Q = Query matrix.
- K = Key matrix.
- V = Value matrix.
- dₖ = Dimension of keys.
  Multi-head attention;
Uses multiple attention operations in parallel to capture different relationships within the input.
  Positional encoding;
Provides information about token positions because attention alone does not inherently represent sequence order.
  Transformer components;
- Token embeddings.
- Positional information.
- Multi-head attention.
- Feedforward neural networks.
- Residual connections.
- Layer normalization.
- Output projection.
  Transformer architectures;
Encoder-only: Designed mainly for understanding and representing input.
Example: BERT.
Decoder-only: Designed mainly for autoregressive text generation.
Examples: GPT-style models.
Encoder-decoder: Uses an encoder to represent input and a decoder to generate output.
Example: Original Transformer and T5-style architectures.

 NLP MODEL TRAINING
  Training data;
NLP models may use:
- Books.
- Articles.
- Websites.
- Conversations.
- Technical documents.
- Transcribed speech.
- Specially labelled datasets.
Data quality, diversity and representativeness influence model performance.
  Tokenization;
Converts text into token IDs that the model can process.
Common approaches:
- Byte Pair Encoding (BPE).
- WordPiece.
- SentencePiece.
- Unigram language-model tokenization.
  Pretraining;
Trains a model on large datasets to learn general language patterns.
Common objectives:
- Next-token prediction.
- Masked-token prediction.
  Fine-tuning;
Continues training a pretrained model on task-specific or domain-specific data.
Example: Fine-tuning a language model on engineering documents.
  Instruction tuning;
Trains a model on examples of instructions and appropriate responses to improve its ability to follow instructions.
  Evaluation;
Common NLP metrics:
Accuracy: Proportion of correct predictions.
Precision: Proportion of predicted positives that are correct.
Recall: Proportion of actual positives correctly identified.
F1-score: Harmonic mean of precision and recall.
BLEU: Commonly used to compare machine translation output against reference translations.
ROUGE: Commonly used to evaluate text summarization against reference summaries.
Perplexity: Measures how well a probabilistic language model predicts a sequence of tokens. Lower perplexity generally indicates better predictive performance on comparable data.
No single metric captures all aspects of language quality.

 NLP AND LARGE LANGUAGE MODEL APPLICATIONS
1. Conversational AI: Intelligent chatbots and virtual assistants.
2. Document intelligence: Extracting information from reports, contracts and technical documents.
3. Search engines: Understanding queries and retrieving relevant content.
4. Engineering: Analysing technical manuals, specifications and engineering reports.
5. Education: Intelligent tutoring, note generation and question answering.
6. Business: Customer feedback analysis, document processing and automated communication.
7. Programming: Code completion, explanation, debugging assistance and documentation.
8. Healthcare: Processing clinical text and supporting information extraction under appropriate safeguards.
9. Robotics: Interpreting voice commands and translating instructions into structured actions.
10. IoT: Analysing text-based sensor alerts, logs and operational reports.

 NLP IN EDGE AI AND EMBEDDED SYSTEMS
Edge NLP executes language-processing tasks locally on devices instead of relying entirely on remote cloud services.
  Applications;
- Offline voice assistants.
- Voice-controlled robots.
- Smart home command recognition.
- Local speech-to-text.
- Intelligent industrial interfaces.
- Embedded keyword detection.
- On-device text classification.
  Typical edge NLP pipeline;
1. Microphone captures speech or an application receives text.
2. Audio preprocessing and noise reduction are performed where necessary.
3. Speech recognition converts speech to text, if required.
4. Text is tokenized and processed.
5. An NLP model identifies intent or generates an output.
6. The output is converted into a command, response or action.
7. The system responds locally or communicates selected information to the cloud.
  Edge NLP optimization;
Quantization: Reduces numerical precision to lower memory and computation requirements.
Pruning: Removes less important model parameters or structures.
Knowledge distillation: Transfers useful behaviour from a large model to a smaller model.
Vocabulary reduction: Restricts or simplifies the vocabulary for specialized applications where appropriate.
Model selection: Uses compact architectures suitable for available hardware.
  Useful tools and frameworks;
- NLTK: Natural language processing fundamentals and text analysis.
- spaCy: Industrial-strength NLP pipelines.
- Hugging Face Transformers: Pretrained transformer models and NLP tools.
- Gensim: Topic modelling and word embeddings.
- Scikit-learn: Traditional ML-based text classification.
- PyTorch: Neural NLP model development.
- TensorFlow: Neural network development and deployment.
- Vosk: Offline speech recognition on supported platforms.
- Whisper: Speech recognition and transcription.
- ONNX Runtime: Inference using compatible exported models.

 NLP CHALLENGES AND LIMITATIONS
1. Ambiguity: Words and sentences may have multiple meanings.
2. Context understanding: Meaning can depend on previous statements and real-world knowledge.
3. Language diversity: Different languages have different grammatical structures.
4. Sarcasm and irony: Literal meanings may differ from intended meanings.
5. Data quality: Incorrect or biased training data affects results.
6. Low-resource languages: Limited training data can reduce model performance.
7. Computational requirements: Large models require substantial memory and processing power.
8. Hallucination: Generative models may produce convincing but incorrect information.
9. Privacy: Text may contain confidential or personally identifiable information.
10. Security: Systems may be vulnerable to prompt injection and malicious inputs.
11. Domain adaptation: General models may perform poorly on specialized technical language.
12. Edge limitations: Limited memory, energy and processing capacity constrain local deployment.

 RESPONSIBLE NLP AND AI
- Protect personal and confidential information.
- Evaluate language models for bias.
- Verify generated information.
- Use representative multilingual datasets.
- Maintain human oversight for important decisions.
- Protect models and communication channels.
- Monitor performance and changes in language usage.
- Clearly distinguish generated content from verified information.

 IMPORTANT EXAM AND PRACTICAL TIPS 
1. Understand the relationship between NLP, NLU and NLG.
2. Know the levels of language processing: morphology, syntax, semantics, pragmatics and discourse.
3. Differentiate tokenization, stemming and lemmatization.
4. Understand Bag of Words, TF-IDF and word embeddings.
5. Differentiate text classification, sentiment analysis, NER and summarization.
6. Understand the difference between speech recognition and text-to-speech.
7. Know the principles of RNN, LSTM and GRU.
8. Understand self-attention and the Transformer architecture.
9. Differentiate encoder-only, decoder-only and encoder-decoder models.
10. Understand pretraining, fine-tuning and instruction tuning.
11. Know the purpose of BLEU, ROUGE and perplexity.
12. Understand how NLP can be deployed on edge devices.
13. Consider privacy, accuracy, latency, memory and energy consumption when developing NLP systems.