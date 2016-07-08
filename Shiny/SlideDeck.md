Data Science Specialization Capstone: Swiftkey Text Prediction
========================================================
author: Shaun Wesley Que
date: July 2016

Introduction
========================================================
This application predicts the next word by looking at previous 1, 2, or 3 words from the text input by the user. The application builds an n-gram model from an English text corpus consisting of the following:
* Around 900,000 blog posts
* Around 80,000 news articles
* Around 2,000,000 Twitter feeds

The datasets comes from [HC corpora](http://www.corpora.heliohost.org/), which is a collection of corpora for various languages. The files have been filtered based on languages and can be downloaded from the Coursera Data Science Specialization [Capstone Page](https://d396qusza40orc.cloudfront.net/dsscapstone/dataset/Coursera-SwiftKey.zip).

Algorithm
========================================================
**NGram Models**:
* Clean the dataset
* Generate unigrams, bigrams, and  trigrams, along with their "confidence level"
* "Confidence level" is calculated by taking the probability that the next word will follow out of all the possible words that may follow
* Export the ngram models to rds files

Algorithm
========================================================

**Prediction**:
* If the last 3 words from the input exist in the trigram model, return the word and confidence.
* If the last 2 words from the input exist in the bigram model, return the word and confidence.
* If the last word from the input exist in the unigram model, return the word and confidence.
* Else, return the most commonly occuring word: "the"


Using SwiftKey Text Prediction Application
========================================================
The application is available here

**Input Panel**
* *Text Input*: Enter the text in input box
* *Complexity*: Select ngram complexity as trigram (default), bigram, or unigram. 

**Text Prediction Output**
* *Prediction*: Prediction of next word for the input text
* *Full Sentence*: Full sentence by concatenating input text with prediction
* *Confidence*: Confidence percentage of the word prediction

Useful Links
========================================================

You can find more about the dataset here:
* Application GitHub link
* Application (shiny server) link
* Milestone Report link
