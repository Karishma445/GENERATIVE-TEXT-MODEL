# GENERATIVE-TEXT-MODEL

"Company"= CODTECH IT SOULUTIONS

"Name"=Dudekula Karishma

"Intern ID"=CTO6DZ2134

"Domain"=Artificial Technologies

"Duration"=6 weeks

"Mentor"=Neela Santosh

Overview
This script demonstrates two approaches to generating coherent paragraphs on specific topics:

LSTM (Long Short-Term Memory) – A type of recurrent neural network trained on sequences of words to learn patterns in text.

GPT-2 – A transformer-based large language model (via Hugging Face) that can generate high-quality paragraphs from prompts without extensive training.

It’s written in a notebook-style Python script that can be run in any Python environment (or Jupyter notebook) with the required libraries installed.

Key Sections
1. Imports & Setup
The script imports:

TensorFlow/Keras for the LSTM model.

Hugging Face Transformers for GPT-2 model loading and text generation.

Utility libraries like numpy, re (regex), and tqdm (progress bars).

2. Data Preparation
The LSTM approach needs a dataset.
Here, we use a small sample corpus (5 short paragraphs on various topics like AI, climate change, healthy living, etc.).

clean_text() removes extra spaces and newlines.

load_sample_corpus() loads these cleaned example paragraphs.

For real results, you’d replace this with a large domain-specific dataset (e.g., articles, Wikipedia text, or a specific industry corpus).

3. LSTM Approach
Steps:

Tokenization:

Convert words into integer indices using Tokenizer.

Generate input sequences for training (e.g., "Artificial intelligence powers" → [12, 45, 92]).

Sequence Padding:

All sequences are padded to the same length so they can be processed in batches.

Model Building:

An Embedding layer maps integers to dense vectors.

An LSTM layer learns long-term dependencies in text.

A Dense softmax output layer predicts the next word.

Training:

The model learns to predict the next word given previous words.

Text Generation:

generate_with_lstm() takes a seed phrase and predicts the next N words, appending them one by one.

4. GPT-2 Approach
Uses Hugging Face Transformers for prompt-based text generation:

gpt2_generate():

Loads GPT-2 and its tokenizer.

Encodes the prompt.

Uses the model’s .generate() method with parameters:

temperature (controls creativity)

top_k / top_p (sampling control)

Decodes and returns generated text.

There’s also a gpt2_finetune_sketch() function to fine-tune GPT-2 on your dataset for topic-specific styles.

5. Example Workflows
example_lstm_workflow(): Trains the LSTM model on the small corpus and generates a paragraph starting with "Artificial intelligence powers".

example_gpt2_demo(): Uses GPT-2 to generate a paragraph on "the benefits of daily exercise".

Advantages of Each
LSTM:

Simpler and smaller, can be trained from scratch on a small dataset.

Good for very domain-specific text if enough training data exists.

GPT-2:

Pre-trained on massive datasets → high-quality results immediately.

Flexible: works with just prompts or can be fine-tuned for specialization.

Usage Notes
LSTM here is quick-trained for demo; more epochs and data improve coherence.

GPT-2 works out of the box for coherent paragraphs but benefits from prompt engineering.

For best internship results:

Train LSTM on a real dataset.

Show GPT-2 results for multiple topics.

Include performance metrics (perplexity, BLEU, human evaluation).

<img width="296" height="312" alt="Image" src="https://github.com/user-attachments/assets/b1ca5fb0-ceed-4ab5-9157-28cf3a66a991" />

