# Life Through Letters
This project takes a look at life in Mississippi in the early part of the twentieth century by looking at what people wrote in their letters, which were the primary form of communication at the time.  In particular, we will look at the Smith family, whose letters have been donated to the Mississippi University for Women.

In this narrative, we are specifically looking at:
1. [The network of correspondence](##network-of-correspondemnce), which shows us the links between people writing letters to each other, 
2. [Victory Mail during World War II](##correspondence-during-wwii), or the progression of "v-mail," and how it was considered a civic duty to write letters to soldiers, and
3. [How people wrote about religion in letters to each other](##writing-about-religion), and whether or not these letters speak to how they felt about church

<!-- Write description of the project here-->

## About the Project
<!-- describe the letter collection-->
The Murphree-Ellard-Pilgreen-Smith collection is a collection of objects, including letters, belonging to the Mississippi University for Women, that were created by members of the Smith family between 1908 and 1977.  This collection is located at MUW Library's Beulah Culbertson Archives, and digitized via [Athena Commons](https://athenacommons.muw.edu/smithpapers/) at the MUW website.

This project looks at letters written between 1929-1944 (those that are digitized). In this collection, there are 343 letters. The majority of these letters (54%) were written between 1943-1944.

![Line graph of letter frequency by date](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/lettersbydate_29-44.png)

Most of the letters were written by members of the Smith Family, with Sonny Boy writing the most letters (97, or 28%), closely followed by Pauline (77, or 22%). The letters that were from people outside the immediate Smith Family totaled 69, or 20% of the letters.

![bar graph of the letter frequencies by sender](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/lettersbysender_29-44.png)

This project was created by Amanda Shinn and Hillary H. Richardson.  Amanda Shinn is a student at the MUW, class of 2023, majoring in Public History.  She is the writer, lead researcher, and lead curator of this project.  Hillary Richardson is the instructor of LIB 201, editor and coordinator of the Smith Papers Project, and the Coordinator of Undergraduate Research at MUW.

## Network of Correspondence
![Screenshot of Palladio](image.png)

The nodes represent individuals who are writing and recieving letters and the lines represent the connections between them and the people that they are writing letters to or recieving letters from. These screenshots tell us that Edith Pauline Smith, or "Pauline", the mother of the family, was the person with the highest number of connections to other people.  

The people with the most "betweenness" or the most connections to nodes not connected to other people are her daughters Edith Christine Faust, "Christine", and Martha Josephine Womble, "Martha", both of whom had very active social lives, as revealed by reading the letters they wrote. Her other daughter, Annie Bernice Smith, "Bernice", has a relatively small node and is the only family member with no direct connection to her father.  

The father of the family, Pauline's husband, Sam Hawkins Smith, "Daddy", was a U.S. senator and had connections to other Mississippi politicians, such as Dennis Murphree and Theodore Bilbo, as is shown in the image above. 

The final large node belongs to Pauline's son, Sam Ellard Smith, "Sonny Boy", who was a soldier in World War II. Although the data needs more cleaning, it does a fair job of showing who had the most connections and to whom.

You can see the data in spreadsheet form [here](https://docs.google.com/spreadsheets/d/1rw3uXL9gaA_cAW0DIuUtDsSeRH6GhucZB7iPvNeetRA/edit#gid=453660900).

## Correspondence during WWII

[![Image of first slide of timeline](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/timline-first-slide.PNG)](https://cdn.knightlab.com/libs/timeline3/latest/embed/index.html?source=1nXufDzi3g0QI_wcI3mvl0HvMIz3tkIwxdFw5N-5Hdxw&font=Default&lang=en&initial_zoom=2&height=650)

This timeline is about the history of v-mail from its creation in 1942 to its discontinuation in 1945.  It uses some of Sonny Boy's letters, which were written from basic training and army posts, using the v-mail stationary some of the time. This form of communication was a technological innovation that saved space on cargo shipments by reducing the paper letters to microfilm reels. V-mail made delivering mail to soldiers faster, as well. 

V-mail, short for "Victory Mail," was a preferred method of communication, as evidenced by corporate and government publications that touted it as a better way to communicate, but also as a patriotic duty to improve the morale of soldiers. The timelin includes a letter from Christine, in which she discusses her obligations to continue writing to men she knew overseas so they wouldn't be lonely.

## Writing about Religion

![Image of letter](https://drive.google.com/file/d/1cjLt8EPRB6hs6ahjePt0gg80Oaaw3Zvq/view)
*Pauline expresses regret that fewer people are going to church: "It seems that now above all others everybody would want to go to church. I went back last night and there were about 20 there I guess. Poor Bro. McKee is in so much trouble..." Letter from Pauline Smith to Martha Smith, February 16, 1942. From the Ellard-Murphree-Pilgreen-Smith Collection.*

For this mini-project, I wanted to know if I could find out anything about religion from analyzing Smith Papers Letters that inclded the words ```church```, ```S. School```, and ```preacher``` and running a sentiment analysis and a topic modeling analysis using the Digital Scholar Lab.  There were 65 letters in all.  I cleaned them by removing the words used in the letterhead.  I also removed ```&``` and ```-```.  

![Image of Topic Modeling](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/topic-model-church.png)
This is an image of the results of the topic modeling.  The bars represent different topics, or groups of words likely to be found together in the dataset.  The only topic clearly related to church is number 9, which includes the words, "Pauline," "Meridian," "reason," "need", "Vicksburg", "Sam", "kids", "FORT," "fellow," and "preacher."

![Image of sentiment analysis of letters about church, with an overall neutral-to-positive score](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/religion-SA.png)
This is an image of the sentiment analysis results.  Most of the results are in the "slightly positive" or "neutral" sections, indicating the overall tone of the letters.

![Image of sentiment analysis of letters not about church, with an overall neutral-to-positive score]()

In another sentiment analysis that includes letters that did not match the search criteria, using the same cleaning configuration, letters scored a similar overall score of neutral-to-positive (0.733 out of 5). While letters in this content set are more widely distributed, the overall score is similar. This may be due to the fact that like other topics discussed in the letters, church appears sporadically and briefly. 

Though it may not be possible to measure the Smith family's feelings about church in their letters, it is also clear that this content set needs more cleaning. In future iterations, this hypothesis would need more focus and testing.

## Sources consulted

* [Smithsonian National Postal Museum.  "Victory Mail."  n.d. Smithsonian Institute.  Accessed October 3, 2022.](https://postalmuseum.si.edu/exhibition/victory-mail)
* ["V-Mail: Letters Home." 2015. _History Magazine_ 16 (5): 17-22.](https://login.libprxy.muw.edu/login?url=https://search.ebscohost.com/login.aspx?direct=true&db=khh&AN=102930021&site=eds-live&scope=site) (requires MUW login to access)
* Harper, Keith.  _The Quality of Mercy: Southern Baptists and Social Christianity 1890-1920._ Tuscaloosa, Alabama: The University of Alabama Press. 1996.
* Queen, Edward L.  _In the South the Baptists Are the Center of Gravity._  Brooklyn, New York: Carlson Publishing, Inc. 1991.
