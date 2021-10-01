# Introduction to Text Analysis

In addition to the important things to analyze in the letters, like places, people, and themes, there's also _the text_. In this lesson, we will use our transcriptions, some textual cleaning methods, and the digital tools that have been developed to analyze the content of a text (or texts) to explore the Smith Papers en masse.

### Objectives
* Understand the purpose of distant reading when analyzing a text or texts
* Understand the processes by which computers "read" text (specifically stemming, lemmatization, stop words, and tokenization)
* Define text analysis methods, specifically n-gram analysis, topic modeling, and sentiment analysis
* Select a data set from Smith Papers to clean, perform select text analysis methods on, and analyze.

### Lessons
1. [Distant Reading](#1-distant-reading)
2. [Select Distant reading methods](#2-select-distant-reading-methods)
3. [Text cleaning methods](#3-text-cleaning-methods)

### Required Reading

- Caulfield, Jack. <a href="https://www.scribbr.com/methodology/textual-analysis/">"A quick guide to textual analysis,"</a> _Scribbr.com_, 2020.
- Underwood, Ted. <a href="https://tedunderwood.com/2016/08/01/a-more-intimate-scale-of-distant-reading/">"A More Intimate Scale of Distant Reading,"</a> _The Stone and the Shell_, 2016. 
- Sculley and Pasanek, <a href="https://login.libprxy.muw.edu/login?url=https://search.ebscohost.com/login.aspx?direct=true&db=hlh&AN=37562266&site=eds-live&scope=site">"Meaning and mining: the impact of implicit assumptions in data mining for the humanities"</a> _Literary and Linguistic Computing, 23_(4), 2008. *This link will take you to MUW Library databases. Sign in with your 950# if you are off campus!*
<!-- section from Drucker's Intro to DH or Ketchley's dh101 course guide? -->

<!--check-in/reading response for the readings?-->

Required Tools
- <a href="https://libguides.muw.edu/DSL">Gale Digital Scholar Lab</a>

Optional tools 
- <a href="http://lexos.wheatoncollege.edu/">Lexos</a> - web-based text-cleaning app
- <a href="https://voyant-tools.org/">Voyant</a> - web-based text analysis app
- <a href="https://mimno.infosci.cornell.edu/jsLDA/">jsLDA: In-browser Topic Modeling</a>  
- <a href="https://databasic.io/en/">dataBASIC</a> - various web-based text analysis tools for different purposes

### Acknowledgements
- "Distant Reading, Modeling, and Concordances," Brandon Locke and Thomas Padilla, NEH Textual Data Institute, 2018
- CUNY DH Institutes, <a href="https://curriculum.dhinstitutes.org/glossary">DHRI Curriculum Glossary</a>
- Screenshots from projects:
    - Froehlich, Heather. <a href="https://blog.oup.com/2015/11/shakespeare-language-gender/">"Analysing what Shakespeare has to say about gender."</a>. _OUP Blog_, 11/28/2015.
    -  King, Lindsay and Leonard, Peter. <a href="http://bookworm.library.yale.edu/">Robots Reading Vogue</a>. _Digital Humanities at Yale University Library_, 2014.
    - Blei, David M., Andrew Y Ng., and Michael I. Jordan. <a href="https://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf">"Latent Dirichlet Allocation,"</a> _Journal of Machine Learning Research 3_, 2003. p. 1009. 
    - Healey & Ramaswamy, <a href="https://www.csc2.ncsu.edu/faculty/healey/tweet_viz/tweet_app/">Visualizing Twitter Sentiment,</a> 2019.
    - Emory Digital Scholarship Commons, <a href="https://lincolnlogs.digitalscholarship.emory.edu/">"Lincoln Logarithms: Finding Meaning in Sermons,"</a> 2013.
    - Jockers, Matthew L. <a href="https://www.matthewjockers.net/2014/06/05/a-novel-method-for-detecting-plot/">A Novel Method for Detecting Plot, "</a> 2014.
- Screenshots from the Gale Digital Scholar Lab

# 1. Distant Reading

## Distant v. Close Reading
If you have been in an English class before, you are familiar with the phrase "close reading." If you have not, close reading refers to choosing part of a text - a word, a symbol, an image - to closely analyze the context of the whole work. In other words, why did the author make these word choices? What factors (e.g. historical, intellectual, subliminal, etc.) have gone into influencing the text that show up in this text over and over again? Close reading is one method used analyze a text. Distant reading, which uses computer assistance to process large amounts of text, is the method we are going to use!

Distant reading with computers is not a way to replace the levels of interpreting that humans are able to do. The work of the computer and the work of the text are often at odds, and while our brains will operate differently than a computer's, we are going to explore using the 2 together. In fact, distant reading <a href="https://en.wikipedia.org/wiki/Index_Thomisticus">is possible without a computer</a>--the work of the computer just saves time!  Additionally, computationally distant reading loses its impact without the context and interpretation from human eyes. (Here's <a href="https://critinq.wordpress.com/2019/04/03/computational-literary-studies-participant-forum-responses-day-3-5/">a controversial opinion</a> that even says it is a failure in the humanities! Gasp!) Countless distant reading projects have enhanced, adjusted, or even changed the ways we look at entire works of a specific collection, an author, or even genre. <!--cite these?--> Like close reading, though, distant reading will allow us to address a hypothesis about a text, and through analysis and interpretation, address that hypothesis with textual evidence.

Unlike close reading, distant reading allows us to:
* Link specific words to the context in which they were used throughout a text (as in a <a href="https://www.corpusthomisticum.org/it/index.age">concordance</a> or <a href="https://cather.unl.edu/">scholarly digital edition</a>)
<!--image-->
* Visualize a single text (or a collection of texts, allowing us to 
    - interact with it graphically and dynamically
    - compare patterns up close and zoomed out
    - gain new insight
    - See <a href="http://www.cameronblevins.org/posts/topic-modeling-martha-ballards-diary/">patterns or changes in a text(s)</a> over time
<!--image-->
* Compare one author's body of work to another, as in to identify distinctive vocabulary (i.e. This person used this word more than that person)
<!--image-->
* Structure a text with
    - hyperlinks
    - other metadata
<!--* Model or predict an explanation-->
<!--* unsupervised modeling-->
* and more!

## How does this work?

    "The difference between the almost right word and the right word is the difference between lightening and a lightening bug" -Mark Twain

Words are so messy! You and I can understand them only after growing up and speaking a language for many years, and even then, we all have different ways of saying and understanding things! So how does a computer begin to "understand" words? With most tools, this is something that goes on automatically in the background, often using a pre-defined list of rules or dictionaries. Let's take a peek behind the curtain!

## Tokenizing

Computers can recognize characters in sequence. But what words say, and what they mean, aren't always so clear! So in order to have a computer "read" something and pull information from it, you have to "tokenize" a text. Tokens can be separated by spaces, but they can also be punctuation (hyphens, commas, parentheses), they could be differently capitalized, and they can have different meanings, even though they're spelled the same way. Tokenizing splits words in a sentence into their individual units. <!--use example from letters?-->

    Hello, I am the all-knowing magician!
 
 To a computer, this is just a series of characters. A computer might separate ```all``` from ```knowing``` when tokenized, simply because they are joined by a hyphen. But that changes the meaning of the sentence. By tokenizing, we can tell the computer what and how we want it to read.

* Hello
* ,
* I
* am
* the
* all-knowing
* magician
* !

If this sentence were a part of a larger corpus, we might also want to make everything the same case and take out punctuation so all linguistic units (aka words) are treated similarly! 

## Lemmatizing and Stemming

Lemmas are root words, or common base words for different variations of a word. Lemmatizing a word is a Natural Language Processing process, which groups words by their roots and parts of speech for analysis. Stemming a word removes part of words (plurals, suffixes, alternate endings, etc.) to collapse them into a common word. For example: 

| Word | Lemma/Stem |
|------|--------|
| good, better, best | good |
|library, librarian, libraries | librar |
| sounding (v.), sounds (n.) | sound |

You can look at all of the instances of the sentiment "good" by lemmatizing the words that mean "good" (i.e. better and best) at their root.

## Stop Words
In a large text, <a href="https://www.ranks.nl/stopwords">stop words</a> are words like "the," "some," "of," "these," etc. that you would like to exclude from analysis because they are determined to be of less value than the other words. But be warned! Sometimes these little words mean a lot! See this blog post about <a href="https://onezero.medium.com/how-data-science-pinpointed-the-creepiest-word-in-macbeth-3150995d3808">"the creepiest word in Macbeth"</a> to see why!

These methods - tokenizing, lemmatizing, stop words (there are more) - are still not perfect! Think of these methods as formulas that you are performing on a text en masse, and the English language often resists a formula. Think of all of the "exceptions to the rule" you have had to learn about. Furthermore, consider texts that are not in English. We use these formulas to help us read a corpus distantly, but that won't replace our abilities to read closely.

<b>These methods are automatic for many tools, but let's not forget them!</b> When we encounter errors or strange findings, it might be that we need to tweak them!

## Check-in
Complete the <a href="https://muw.instructure.com/courses/17249/quizzes/67634">1.Text Analysis check-in</a> here. HO 303 students can complete the <a href="https://muw.instructure.com/courses/16930/quizzes/67639">1.Text analysis check-in</a> here.
<!--examples of what it lets us do (with pictures? Matching??)-->

# 2. Select Distant Reading Methods

In this class, we're going to use specific text analysis methods that are available in the <a href="https://libguides.muw.edu/DSL">Digital Scholar Lab</a>. (Hint: click Databases from the <a href="https://www.muw.edu/library">MUW Library Homepage</a>, and find it under "D."). You'll need to link your Google MyApps account to this database to get started. These are the tools we'll explore...

## N-gram analysis

![Screenshot of a word cloud of William Wordsworth's distinctive vocabulary words in his poems, from Ted Underwood](https://github.com/hillaryAHR/LIB-201/blob/main/text-analysis-images/ngram-wordsworth.JPG)

N-grams are more commonly known as word clouds. You see words of different sizes, indicating the number of times that word is used throughout the text. The "N" in n-gram stands for number of words you are counting or highlighting in a corpus, so you can also do this with phrases. 

N-grams also show the patterns of those words as they're used throughout the text over time (time can be literal - as in, throughout the years, as seen in the screenshot below, or it can be relative to the text itself, as in how the word is used throughout the course of the corpus.)

![Screenshot of Robots Reading Vogue, showing the uses of corset, girdle, bra, bustier, and hosiery over time](https://github.com/hillaryAHR/LIB-201/blob/main/text-analysis-images/ngram-RRV.JPG)

N-grams can also be used to collocate words or phrases and to determine relationships between word pairs. The example below shows how words with positive connotations are more often associated with gendered words.

![Screenshot of Heather Froehlich's analysis of Shakespeare texts, where male-gendered words have more positive connotations (i.e. Man - young) than female-gendered words (i.e. Woman - wretched)](https://github.com/hillaryAHR/LIB-201/blob/main/text-analysis-images/ngram-shakespeare.JPG)

__You'll use an n-gram analysis to explore word pairs, frequencies, and their use over time.__

## Topic Modeling

Topic Modeling is one of the more difficult text analysis methods because it is based on probability. Topic Modeling uses an algorithm (<a href="https://towardsdatascience.com/latent-dirichlet-allocation-lda-9d1cd064ffa2">Latent Dirichlet Allocation</a>) to find probabilities of words that co-occur. When you run this algorithm on a body of text, it puts the words that are _more likely_ to occur together in categories, or "bags of words." The idea is that each category represents a topic of discussion in the text. 

![Screenshot of Lincoln Sermons Topic keywords split into 10 columns labeled "topic 1," "topic 2," and so on](https://lincolnlogs.digitalscholarship.emory.edu/wp-content/uploads/2013/02/mallet.png)

Topic modeling requires some inference on behalf of the person running the algorithm - how are these groups of words related? How are they used in the text? Do they signify a distinct theme? For instance, all of the words in topic #1 in the image above are probabistically related to each other. At first glance, it looks like they are related to law and policy. It is not always clear what distinct topics are, but knowing about the contents of the text helps! 

In another example, the column labels below were chosen to reflect the commonalities among the words below them.

![Screenshot of topic modeling results with columns labeled Arts, Budgets, Children, and Education, in colors corresponding to highlighted words within a paragraph](https://i.imgur.com/9UesuuB.png)

## Sentiment Analysis

![Screenshot of sentiment analysis of tweets using #nationalsonsday](https://github.com/hillaryAHR/LIB-201/blob/main/text-analysis-images/SA-sons.JPG)

_Sentiment analysis of tweets using #nationalsonsday from https://www.csc2.ncsu.edu/faculty/healey/tweet_viz/tweet_app/_

![Screenshot of sentiment analysis of tweets using #nationaldaughtersday](https://github.com/hillaryAHR/LIB-201/blob/main/text-analysis-images/SA-daughters.JPG)

_Sentiment analysis of tweets using #nationaldaughtersday from https://www.csc2.ncsu.edu/faculty/healey/tweet_viz/tweet_app/._ 

A sentiment analysis uses natural language processing to "score" words according to a positive or negative scale. Sentiment analyses are trained on a pre-determined set of words (such as the <a href="http://corpustext.com/reference/sentiment_afinn.html">AFINN lexicon</a>), and show (or attempt to show) the overall positive or negative emotions at any given moment within a corpus. 

![Screenshot of the plot of James Joyce's Portrait of the Artist as a Young Man in a sentiment analysis](https://www.matthewjockers.net/wp-content/uploads/2014/06/poa2.png)

Note: Sentiment analyses have limits! Like toddlers, sentiment analyses **do not** detect sarcasm! :laughing: They also commonly do not account for the change in meanings of words over time (i.e. sick = ill v. sick = slang for cool).

<!--link to Becky's project?-->

<!-- ## Named Entity Recognition -->

## Check-in
Complete the <a href="https://muw.instructure.com/courses/17249/quizzes/67635">2.Text Analysis check-in</a> here. HO 303 students can complete the <a href="https://muw.instructure.com/courses/16930/quizzes/67637">2.Text analysis check-in</a> here.

# 3. Text Cleaning Methods

Remember our discussion of tokenization, lemmas, and stop words? In order to remove the inconsistencies and "noise" for a computer to analyze texts, you will judicially employ and tinker with some of these processes. Also remember the words of advice from Muñoz and Rawson in <a href="http://curatingmenus.org/articles/against-cleaning/">"Against Cleaning!"</a> when employing these methods!

![Screenshot of text cleaning configurations in the Digital Scholar Lab](https://github.com/hillaryAHR/LIB-201/blob/main/text-analysis-images/DSLAB_CreateCleanConfig_Corrections.jpg)
<!--https://go.gale.com/ps/helpCenter?userGroupName=mag_u_muw&inPS=true&nspage=true&prodId=DSLAB&docId=GVOFKU762720149-->

## Upper v. lower case
In some cases, a text analysis tool will treat words differently if they are in different cases. Remember, computers see strings of characters, and are as frustratingly literal as possible! This cleaning method eliminates the possibility of the computer treating the words ```Mother``` and ```mother``` differently. There could be a scenario when you'd like them to be different (i.e. maybe they say "Mother" as her name, but refer to her as "mother" to each other), so keep that in mind!

## Character removal, or "Scrubbing"
This method allows you to programmatically remove or replace characters, words, or lemmas. This is common for a text that is read through OCR recognition (when you scan a document instead of transcribe it, and a computer tries to recognize the characters). Often OCR will substitute characters or images with non-letter symbols, like Ê, §, ¶, ¥, or %. This is less likely to happen with transcriptions.

However, removing punctuation might be helpful, especially since letter writers use punctuation differently! Furthermore, if you are analyzing the body of the letter, you will want to remove the part of the text that includes the envelope and letter head. Consider the different ways to do this (stop words, cutting the beginning of all the letters, removing line breaks, etc.) <!--Check-in question?-->

## Replacements
Like the ctrl+F function, replacing items across the board is another way to clean a text. (Remember doing this for the network analysis?) This could be helpful with things like abbreviations, nicknames, inconsistencies in spelling, etc.

## Stop words
In the previous section, we talked about removing words with "little value" (poor little words!), which you can alter according to the specifications of the text you're dealing with. This also applies to words that are endemic to the colleciton. For instance, you might see the word "Mississippi" over and over again, and think, well duh! If your analysis reveals "Mississippi" as a significant word that you aren't really interested in, add it to your stop words.

In different tools, you will separate these words differently (spaces, commas, or line breaks). 

## Check-in
<!--post a screenshot of an uncleaned doc and make suggestions? Scenarios of cleaning something? Errors when cleaning?-->