# Spam Classifier
### Description
In this project, our goal is to build a predictive model which will determine whether a text message in English is spam or ham (not spam).

We will be using nltk library. The Natural Language Toolkit, or more commonly NLTK, is a suite of libraries and programs for symbolic and statistical natural language processing for English written in the Python programming language.

SMS Spam Collection Dataset has been used, which tags 5,574 text messages in English based on whether they are “spam” or “ham” (not spam).

The project steps includes:
* Data cleaning: 
    This reduces noise, groups terms with similar semantic meanings and reduces computational costs by giving us a smaller matrix to work with.
    * Case Normalization: Spam messages tend to use more upper case words to capture the readers’ attention. However, it makes no difference in spam detection and that all words are reduced to the same case.
    * Removing Stop Words: Stop words are commonly used words that do not add predictive value because they are found in most sentences. So they are removed.
    * Removing Punctuations and Special Symbols: Importance of punctuation and special symbols to classifier’s predictive capabilities cannot be overlooked. The importance of each symbol’s functionality, for example, the apostrophe allows us to define contractions and differentiate between words like it’s and its.
    * Stemming/Lemmatizing: Stemming is the process of reducing inflected words to their word stem, base or root form. Lemmatization is grouping together the inflected forms of a word so they can be analysed as a single item, identified by the word's lemma, or dictionary form. Stemming and Lemmatization both generate the root form of the inflected words. The difference between lemmatising and stemming is that lemmatising performs 
    this reduction by considering the context of the word while stemming does not.

* Vectorizing Text: We will use the TF-IDF vectorizer (Term Frequency — Inverse Document Frequency), an embedding technique which takes into account the importance of each term to document. TF-IDF vectorizes documents by calculating a TF-IDF statistic between the document and each term in the vocabulary. The document vector is constructed by using each statistic as an element in the vector.

* Building and Testing Classifier: Naive Bayes methods are a set of supervised learning algorithms based on applying Bayes’ theorem with the “naive” assumption of conditional independence between every pair of features given the value of the class variable. We use Multinomial Naive Bayes. MultinomialNB implements the naive Bayes algorithm for multinomially distributed data, and is a classic naive Bayes variant used in text classification (where the data are typically represented as word vector counts).


### Data Source
Data has been taken from freely available resource on the Web.
URL: http://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection 

The SMS Spam Collection is a public set of SMS labeled messages that have been collected for mobile phone spam research.
	
It has one collection composed by 5,574 English, real and non-enconded messages, tagged according to being legitimate (ham) or spam.

### Data Set Information

This corpus has been collected from free or free for research sources at the Internet: 

* A collection of 425 SMS spam messages was manually extracted from the Grumbletext Web site. This is a UK forum in which cell phone users make public claims about SMS spam messages, most of them without reporting the very spam message received. The identification of the text of spam messages in the claims is a very hard and time-consuming task, and it involved carefully scanning hundreds of web pages. The Grumbletext Web site is: [http://www.grumbletext.co.uk/].

* A subset of 3,375 SMS randomly chosen ham messages of the NUS SMS Corpus (NSC), which is a dataset of about 10,000 legitimate messages collected for research at the Department of Computer Science at the National University of Singapore. The messages largely originate from Singaporeans and mostly from students attending the University. These messages were collected from volunteers who were made aware that their contributions were going to be made publicly available. The NUS SMS Corpus is avalaible at: [http://www.comp.nus.edu.sg/~rpnlpir/downloads/corpora/smsCorpus/].

* A list of 450 SMS ham messages collected from Caroline Tag's PhD Thesis available at [http://etheses.bham.ac.uk/253/1/Tagg09PhD.pdf].

* Finally, we have incorporated the SMS Spam Corpus v.0.1 Big. It has 1,002 SMS ham messages and 322 spam messages and it is public available at: [http://www.esp.uem.es/jmgomez/smsspamcorpus/].

### Statistics

The table below lists the provided dataset in text file format, the amount of samples in each class and the total number of samples.

Application  |  File format   |   Spam     |    Ham     |   Total
-------------|----------------|------------|------------|-----------
General      |     Text       |   747      |    4827    |   5574

The collection is composed of just one file, where each line has the correct class (ham or spam) followed by the raw message.

ham   What you doing?how are you?
ham   Ok lar... Joking wif u oni...
ham   dun say so early hor... U c already then say...
ham   MY NO. IN LUTON 0125698789 RING ME IF UR AROUND! H*
ham   Siva is in hostel aha:-.
ham   Cos i was out shopping wif darren jus now n i called him 2 ask wat present he wan lor. Then he started guessing who i was wif n he finally guessed darren lor.
spam  FreeMsg: Txt: CALL to No: 86888 & claim your reward of 3 hours talk time to use from your phone now! ubscribe6GBP/ mnth inc 3hrs 16 stop?txtStop
spam  Sunshine Quiz! Win a super Sony DVD recorder if you canname the capital of Australia? Text MQUIZ to 82277. B
spam  URGENT! Your Mobile No 07808726822 was awarded a L2,000 Bonus Caller Prize on 02/09/03! This is our 2nd attempt to contact YOU! Call 0871-872-9758 BOX95QU

### Reference

http://dcomp.sor.ufscar.br/talmeida/smspamcollection/

The SMS Spam Collection has been created by Tiago Agostinho de Almeida [http://www.dt.fee.unicamp.br/~tiago] and José María Gómez Hidalgo [http://www.esp.uem.es/jmgomez]. 

