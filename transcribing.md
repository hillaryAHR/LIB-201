# Introduction to Transcribing Documents

Why do we transcribe documents? On one level, transcribing something allows you to become intimately familiar with the contents of a document. By the end of this semester, you may be invested in a family that isn't your own! <!-- Link to article in History Newsletter--> 

Furthermore, transcribing makes physical documents, especially handwritten documents, **machine readable**. In other words, it allows computers to recognize text. Think about it -- scanned letters are pictures of text, which is something a machine cannot translate. Even though there are programs that can attempt to read handwriting (like Transkribus) and even typed text<!--link to Explain that stuff "What is OCR-->, computers aren't smart enough to read things humans are! 

**Transcribing something bridges the gap between reading a document, and storing a picture of one.**

<hr>

In this module, you will learn:
* Basic transcribing guidelines
* How to create and edit text regions in Transkribus
* How to use style and metadata tags in Transkribus

## Lessons
1. [Transcribing Guidelines](#1-transcribing-guidelines)
2. [Text Regions in Transkribus](#2-text-regions-in-transcribus)
3. [Handwritten Text Recognition](#3-handwritten-text-recognition)
4. [Metadata Tags](#4-metadata-tags)
5. [Exporting Files in Transkribus](#5-exporting-files-in-transkribus)

## Required before beginning the lesson
### Reading
* Woodford, Chris. 2021. "Optical Character Recognition," _Explain that Stuff_, https://www.explainthatstuff.com/how-ocr-works.html. 
* <a href="https://docs.google.com/document/d/1Vo_YCCW18aam14CnAG8KyYYDlV37zODsFaqP_6_Flgk/edit?usp=sharing">"About the Smith Papers Collection."</a> This document gives context for the letters and describes the main contributors. Read this before you begin transcribing. 

### Installations
* Transkribus: https://readcoop.eu/transkribus/?sc=Transkribus (<a href="https://readcoop.eu/transkribus/wiki/download-and-installation/">Installation Instructions here.</a> *Be sure you have Java 8 installed before installing Transkribus.* This is in the instructions, but not in the first step. If you run into an issue, email your instructor!)

## Further reading (optional)
*  Transkribus Transcribing Conventions, 2021. Read Co-op,  https://readcoop.eu/transkribus/howto/transkribus-transcription-conventions/.
* Smithsonian, "General Instructions for Transcription and Review," https://transcription.si.edu/instructions
* YouTube video of Hillary introducing Transkribus: https://youtu.be/szGPn0K_WWE
* YouTube video of Hillary transcribing a letter from beginning to end: https://youtu.be/-cDD9P0rnLw 
* Interview with Bridget and Steve Pieschel about the contents of the Smith Papers letters: https://youtu.be/zPynkw9V-Q8

# 1. Transcribing Guidelines

In order to maintain the integrity of your original document while you are translating it for the computer, consider a few things while you're transcribing.

## Stay as true to the document as you can!
* Include all text as it is written. This includes errors in spelling and grammar, and words you might not be familiar with. Transcribing is NOT editing!
* If there are images in the text, describe them in brackets (e.g. "[doodle of a curly-haired smiling face]").
* Keep it simple! You want people to be able to read the transcription without looking at the original letter. Your transcriptions will be plain text files (e.g. files with no formatting), so, without editorializing, keep the text readable as possible.

## If you have trouble reading the text...
  * Take a break and come back. Fresh eyes make a difference!
  * Try to read the words in context. The word might look like "fhe," but it doesn't make sense to read "And then fhe called her sister." You would realize the word is "she."
  * Ask for help. Send a screenshot to your classmates, or post it in the Teams channel.
  * If you've tried all these things, and it's just not possible to figure out, write ```[illegible]``` in brackets and tag that text with the "gap" tag (more on tags in section IV!).

## Take notes while you are transcribing
* Make note of things you don't understand, and Google them to see if you can make sense of the reference.
* You might find something interesting that you want to come back to! Take notes of the letters you transcribe, and what you find interesting about them.

While it is long, I highly recommend watching <a href="https://youtu.be/-cDD9P0rnLw">this video</a> of transcribing a letter from start to finish. Feel free to follow along in corresponding sections! 

## Check-in

Practice transcribing a few lines, staying true to the original text with the <a href="https://muw.instructure.com/courses/19030/quizzes/75438">0.Transcribing Check-in</a>. 


# 2. Text Regions in Transkribus

Before we get started actually transcribing, we have to tell Transkribus what parts of the page have text on them, and what order to read that text! (Remember, computers aren't smart enough to read like humans!)

The text regions we will work with are:

The page (or "text region"), where text is:
![screenshot of green text region](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/text-region-screenshot.png)

The line of text, as in the full, left-to-write line:
![screenshot of light blue line highlighted](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/line-screenshot.png)

And the baseline, which underlines the words themselves:
![dark-blue dashed line within the light blue outline](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/baseline-screenshot.png)

## Run a Layout Analysis

Transkribus does a pretty good job of identifying these text regions for us. The quickest way to do this is to run a layout analysis on the document, then correct any mistakes that Transkribus makes. Here's how you run the analysis:

1. Double click the document you’ve uploaded, and click on the Tools tab. 
2. Under Layout Analysis, make sure you’ve selected all pages.
3. Click Run

![screenshot of layout analysis](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/layout-analysis-screenshot.png)

4. A notification that the layout analysis is in progress will pop up. After a few moments (between 3 and 10 seconds), the layout (green squares, blue rectangles, and dark blue lines) will appear over the letter’s text.
5. Correct errors in the layout (e.g. delete text regions or lines that don’t cover text, resize regions that cut off text, reorder line numbers, or merge lines that have been split). Screenshots of example corrections:

     - Delete text regions that don't actually contain any transcribe-able text. 
     ![Screenshot of a layout analysis that has created a line where there isn't text](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/no-text-layout-error.JPG)
     - This layout analysis split a line in two, and needs merging. (Sometimes, though less frequently, it will merge something that should be two lines. For this, use the scissor tools above the merge tool.) Holding control, click each region that needs joining (usually the baseline and the line) and then click merge.
     ![Screenshot of a text region split](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/merge-error-screenshot.png)
     - Sometimes the software will number things in a different order than we'd actually read them. Click on the eye in the top toolbar, and select ```show lines reading order```. If the lines are out of order, click on the numbers to change them.
     ![screenshot of lines reading order](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/line-reading-order-screenshot.JPG)

## Check-in
Complete <a href="https://muw.instructure.com/courses/19030/quizzes/75443">2.Transcribing Check-in</a> here.

# 3. Handwritten Text Recognition

We are using the Transkribus software because it allows you to create Handwritten Text Recognition (HTR) models. Over the past 2 years that we've worked on this project, we have transcribed over 100 letters and trained the program to begin to recognize Pauline Smith's handwriting. This allows us to run the model on letters in the collection and start with a more complete transcription to correct, rather than having to transcribe the letter from scratch. 

1. To transcribe with the HTR model, click on the Tools tab, and under Text Recognition, select the model called “Pauline Smith 2.0.” You might have to navigate to the next page to find the Pauline Smith model.

![screenshot of the Text recognition tool](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/htr-step1.png)

![screenshot of Pauline Smith's HTR model](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/htr-step2.png)

2. Click Run. The HTR analysis may take anywhere from 20 seconds to 2 minutes. A notification that the “job” is done will pop up when analysis is complete. From there, correct the transcription.
3. Transcribe each page as you see it, following Smithsonian and Transkribus transcription guidelines. You may have a few errors on a page or there may be significant errors. It depends on several things - the quality of the scan, the quality of the document, the handwriting and what utensil they used, etc.!

![screenshot of HTR errors](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/htr-corrections-example.png)

4. Mark your progress as you complete each page.

![screenshot of progress menu](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/transcribing-progress.png)

5. After you've completed editing the transcription, go back over the letter, making sure you didn't miss typos, and you can simultaneously begin tagging the document, which will be explained in the next lesson! 

## Check-in
Complete the <a href="https://muw.instructure.com/courses/19030/quizzes/75448">3.Transcribing Check-in</a> here.

# 4. Metadata Tags

Tagging, annotating, or marking-up a document is a common practice for text analysis. Why is this? Think about the things someone might talk to you about in a letter. They might mention people they talked about, places they went, or a book they read. Now think about the contents of 6,000 letters, and all of this information together! Tagging will allow us to use the information in the collection of thousands of letters to track these trends over time, explore topics, and find people. 

Think of tagging the letter like highlighting categories of information with a different color highlighter. All of the people's names are blue, the places are purple, etc. Transkribus does the same thing.

## Categories of metadata tags

It is tempting to tag everything, but not necessary! You only need to tag:
1. Important words (e.g. people and places)
2. When you add something for clarity that isn't there originally (e.g. "[illegible]"). 
3. If you want to provide further information as context. 

## Metadata tags, defined.

Here are the tags we have, to this point, decided to use for the Smith Collection, and their definitions. (For the info below in a Google Doc, click <a href="https://docs.google.com/document/d/1zpzWtUEvXBDhJAt9xNxpp4Kif2ov4V-y1nGntZbPqyo/edit?usp=sharing">here</a>. And for more info about how Transkribus feels about tags, click <a href="https://readcoop.eu/transkribus/howto/how-to-enrich-transcribed-documents-with-mark-up/">here</a>.) 

1. **person** - when any person’s name is mentioned within the body of the letter (e.g. “Daddy,” Martha, Gilbert, etc.)
2. **place** - when a place name is mentioned within the body of the letter. This does not usually include general places like Sunday school or hospital. Examples would be town names like Bruce or Memphis.
sender - The person who sent the letter, either in the return address, or in the letter’s closing.
3. **recipient** - The person the letter is addressed to, either on the envelope, or in the salutation.
4. **address** - The address the letter was sent to.
5. **return-address** - the address the letter came from (not always included)
6. **organization** - a specific group, corporation, or entity (e.g. the Senate, the T.V.A., or Ole Miss), not a generic place like hospital or school.
7. **sic** - for an error in the original letter (i.e. spelling, grammar, etc.) that you include it in the transcript for accuracy, tag it with “sic,” showing that it’s “as is,” and you didn’t make the error in transcribing.
8. **title** - the title of a book, play, radio show, government decision, etc. Anything that is published, for example. Specifications may include full title, author, and publication date.
9. **date** - a specific date (e.g. January 15th, 1948). This does not include general references to days of the week or years (e.g. “Saturday nite” or “next year.”)
10. **unclear** - when you write something in the transcription, but aren’t sure of what it actually says in the letter: a guess.
11. **gap** (formerly supplied) - when you include something (i.e. [illegible], a note, etc.) that isn’t in the original letter to give clarity, but to prevent the HTR from picking up the note.

## How to tag something

1. To tag something, highlight the text you want to tag, right-click, and from “All tags,” select the relevant tag.

![Screenshot of how to tag something](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/tag-screenshot.png)

2. If the tag isn’t in the list, go to the metadata menu, then the Textual menu, and click Customize. 

![Screenshot of customize tag](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/customize-tag.JPG)

3. Click “Create new tag,” then type in the name of the tag, lowercase, like it’s shown in the Tag definitions document. 

![Screenshot of creating a new tag](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/create-new-tag.JPG)

## Check-in
Tags are sort of tricky! Let's go over the different scenarios in the next <a href="https://muw.instructure.com/courses/19030/quizzes/75454">4.Transcribing Checkin</a>.>

As a reminder, there is a video of transcribing a letter from beginning to end, which you can watch as a refresher: https://youtu.be/-cDD9P0rnLw.

At the end of this lesson, you should be able to fill out the full transcription and tags in your letters, and turn them in in Canvas.

# 5. Exporting files in Transkribus
After you have transcribed (or corrected a transcription of) a letter, tagged it, and proofed it, it has been digitally transformed, and we can now do fun things with the transcriptions and metadata. But before you can do that, you have to export the files. 

Before the step-by-step, I recommend watching the 3-minute video on this process: https://youtu.be/k21t3jGL4LM. 

## Export

Click the export button (a manila folder with a green, right-facing arrow), and you will choose the following files to export:
* .docx - to give you a formatted version of the transcript
* .txt - to give a non-formatted version of the transcript
* .xlsx (tag export) - to give you structured lists of the tags you created

_If you would like to export more than one document, select the radio button that says "Current Collection," and choose which letters to export._

![Screenshot of Export Document option](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/export.JPG)

## Extract zipped files
When you click OK, Transkribus emails you a temporary link where you can access the compressed files you just created. Compressing them allows them to send large amounts of data over email. When you click the link, it will ask you to save the compressed files (.zip).

![Screenshot of saving compressed folder](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/extract-files-1.JPG)

Saving them as compressed files stores them to your computer, but does not let you access them until you extract them. Right-click your compressed folder and click ```Extract All...``` then tell your computer where you want to extract them to. I recommend saving them to a folder where you're keeping files for this class. (We will also store them on a cloud server, e.g. Google Drive or our Institutional Repository at some point.)

![Screenshot of extracting files to a destination](https://github.com/hillaryAHR/LIB-201/blob/main/transcribing-images/extract-files-2.JPG)

After you extract the files, you should notice that your folder no longer has a zipper on it, and you have 3 files that represent digital versions of the letter you prepared. You are now ready to start playing with these digital artifacts!

<!--Link to upload exported letters in Canvas-->

