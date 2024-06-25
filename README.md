# N-Gram Language Model

**The program is designed to generate text based on n-gram language models, specifically using bigram (2-gram) and trigram (3-gram) models.** An n-gram model uses sequences of words in the text to predict the next word in the sequence. This is a common approach in natural language processing (NLP) tasks such as text prediction, auto-completion, and language generation.

## How It Works

### 1. N-Gram Models:
- **Bigram Model**: This model predicts the next word in a sequence based on the previous word. It considers pairs of consecutive words (bigrams) from the training data to calculate the probability of a word following another.
- **Trigram Model**: This model extends the bigram approach by considering sequences of three words. It predicts the next word based on the previous two words, allowing for more context in the predictions and generally resulting in more coherent and contextually appropriate output.

### 2. Text Generation:
- **Using either a bigram or trigram model**, the program generates text by starting with a known word (or words, in the case of trigrams) and repeatedly choosing the next word based on the probabilities learned during the training phase until the desired length of text is generated.

## Techniques Applied

### a. Tokenization:
The text is broken down into manageable pieces called tokens (usually words). This involves removing punctuation and converting all text to lower case to ensure uniformity.

### b. Probability Calculation:
- **For bigrams**, the probability of each word following a preceding word is calculated based on their frequency of occurrence together in the training data.
- **For trigrams**, the probability of a word is conditioned on the sequence of the two preceding words.

### c. Model Storage:
The probabilities are stored in a data structure (such as an unordered map) where each key is a word or pair of words, and the value is a list of potential subsequent words with their corresponding probabilities.

## Training the Model

1. **Data Collection**: Compile a large corpus of text data that is representative of the language or style you wish to generate.
2. **Preprocessing**: Apply tokenization to clean and prepare the data.
3. **Frequency Counting**: Count how often each bigram or trigram occurs in the corpus.
4. **Probability Estimation**: Calculate the conditional probabilities for each bigram or trigram based on their frequencies. This often involves some form of smoothing technique to deal with low-frequency occurrences and to estimate the probability of unseen n-grams.

## Using the Program

- **Load the Model**: Start by loading a pre-trained n-gram model from a file. This file contains the probabilities of word sequences as learned from the training data.
- **Generate Text**: Provide a starting word (or two words for trigrams) and specify the length of the text you want to generate. The program uses the loaded model to predict each subsequent word based on the previously generated words.
- **Output**: The program outputs generated text, which can be used for various applications such as simulating conversation, generating creative writing, or even for educational purposes in understanding language patterns.

## Practical Applications

This tool can be extremely useful in various domains:
- **Autocompletion**: Improving user experience in text editors and search engines by predicting subsequent words during typing.
- **Chatbots**: Generating human-like responses in conversational agents.
- **Content Creation**: Assisting in creative writing by suggesting sentence completions and ideas.

**Overall, this program provides a practical implementation of n-gram language models, demonstrating fundamental concepts of NLP while offering a base for more complex linguistic modeling and text generation tasks.**
