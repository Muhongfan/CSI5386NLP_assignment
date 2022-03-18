# CSI5386NLP_assignment

## A1: 
Part 1: Corpus processing: tokenization, and word counting [50 points]

 

Implement a word tokenizer that splits texts into tokens and separates punctuation marks and other symbols from the words. Please describe in your report all the decisions you made relative to pre-processing and tokenization.  Implement a program that counts the number of occurrences of each token in the corpus.

 

You can use any tools for tokenization, and write programs only if you need to put the data in the right format or to compute additional information. There are many NLP tools that include tokenizers. Some of them are adapted to social media texts.

 

Use this corpus of 100,000 forum posts as input to your tokenizer. The format is one post per line. Provide in your report the following information about the corpus:

a)     Submit a file output.txt with the tokenizer’s output for the whole corpus. Include in your report the output for the first 10 posts in the corpus.

b)    How many tokens did you find in the corpus? How many types (unique tokens) did you have? What is the type/token ratio for the corpus? The type/token ratio is defined as the number of types divided by the number of tokens.

c)     For each token, print the token and its frequency in a file called tokens.txt (from the most frequent to the least frequent) and include the first 20 lines in your report.

d)    How many tokens appeared only once in the corpus?

e)     From the list of tokens, extract only words, by excluding punctuation and other symbols, including forum-specific symbols, if any. Please pay attention to end of sentence dot (full stops). How many words did you find? List the top 20 most frequent words in your report, with their frequencies. What is the type/token ratio when you use only words (called lexical diversity)?

f)     From the list of words, exclude stopwords. List the top 20 most frequent words and their frequencies in your report. You can use this list of stopwords (or any other that you consider adequate). Also compute the type/token ratio when you use only word tokens without stopwords (called lexical density)?

g)    Compute all the pairs of two consecutive words (bigrams) (excluding stopwords and punctuation). List the most frequent 20 pairs and their frequencies in your report. 

Part 2: Evaluation word embeddings  [50 points]

 

Word embeddings are dense representations of the meaning of words, build via neural language models. Chose at least 5 pre-trained word embeddings. If they have different parameters, you can experiment with them, but choose one for your report. Also make sure to include BERT or another similar model large-scale pre-trained language model.

 

Use the code from https://github.com/kudkudak/word-embeddings-benchmarks to access 12 benchmark datasets and possibly the evaluation script. Select word similarity and word analogy questions (no categorization datasets). Using other code or your own is ok to, as long as you use the required benchmark datasets. [1]

 

Please use the following 11 datasets for evaluation:

Similarity tasks:

MTurk

MEN

WS353

Rubenstein and Goodenough

Rare Words

SimLex999

TR9856

 

Analogy tasks:

MSR WordRep

Google_analogy

MSR

SEMEVAL 2012 Task 2

 

Include in your report details about what word embeddings you chose (with what parameters and what mechanism is behind them), and add in the tables below with the results of their evaluations on the above-mentioned benchmark datasets (if you used more than 5 embeddings, mention in the report but out the best 5 results in the tables). Also include the average score over all the datasets. We will have a mini-competition for the best average score over the benchmark datasets for your best word embedding results. For the similarity task the evaluation score is the Spearman correlation. For the analogy relations, use accuracy.

## A2：
In this assignment, you will classify shorts texts describing happy moments. Your system will predict agency and sociality for happy moments in the test set, based on a small labeled and large unlabeled training data. The classes to predict for each text will be: agency label (0 or 1, where 1 means that the person who wrote the text was actively involved as an agent) and social label (0 or 1, where 1 means that the text describes a social activity).

This is a mini-competition to see which team can achieve the best accuracy scores.

 

The dataset was used in the CL-AFF SHARED TASK: IN PURSUIT OF HAPPINESS. See all the papers form the work shop here.

The data is available here, and it contains the following:

·       Labeled training set: Single-sentence happy moments from the available HappyDB corpus, annotated with labels that identify the 'agency' of the author and the 'social' characteristic of the moment, as well as concept labels describing its theme

·       Unlabeled training set: The remaining single-sentence happy moments with no labels.

·       Test set: Previously unreleased, labeled, single-sentence happy moments, freshly collected in the same manner as the original HappyDB data that is used as training set.

 

In the labelled data, each line contains the following information: an id, the text of the happy moment, a set of concepts manually assigned, the agency label,  the social label, the age of the writer, her/his country, her/his gender, her/his marital status, her/her parenthood status, and two timing fields. You should use the text of the happy moment, and the two labels. Feel free to use other information. If you want to use the concepts, be aware that for the test data they need to be predicted, since they were manually added in the training and test data, so they are not normally available at test time. 
