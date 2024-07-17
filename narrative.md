# Narrative Projects
We have been focusing on "telling the story" of a collection thus far through mini-projects like network analyses, timelines, maps, and textual analyses. Now it is time to use _a story_ to tell the story! Thus, we will create a narrative, online project to weave together the items in the collection - and the artifacts we've created with them - with what we have learned through our prodding, research, and exploration.

Objectives:
- Identify the qualities of an accessible web narrative
- Identify elements that comprise Markdown formatting, and design a simple document with those elements
- Design a narrative project with a logical outline
- Create a website portfolio that compiles primary sources, secondary sources, and derived artifacts from previous course modules.

## Lessons

1. [Writing for the Web](#1-writing-for-the-web)
2. [Markdown](#1-markdown) 
3. [Creating a narrative project](#3-creating-a-narrative-project)

## Required Tools/Reading
- Text Editor software (comes installed on most computers). Suggestions for text editors:  
    - Visual Studio Code is the Microsoft Office equivalent of Notepad or TextEdit. VS Code is more user friendly, and works within your browser (by typing the period ```.``` in a github markdown page). To install, visit https://code.visualstudio.com/. Click "Download for..." your operating system.
    - PC users: Notepad comes already installed
    - Mac users: TextEdit comes already installed
    - If you are using an already-installed text editor, preview your markdown using something like https://dillinger.io/ or https://markdownlivepreview.com/
- Brannock, Jennifer. <a href="http://misslib.org/Resources/Documents/MLarchive/ML2009Summer.pdf">"Creating an Exhibit in Special Collections and Using it to Promote Collections and Educate Users,"</a> _Mississippi Libraries 73_(2), 2009. pp. 32-34.
- Ovadia, Steven. (2014). <a href="https://academicworks.cuny.edu/lg_pubs/7/">"Markdown for Librarians and Academics,"</a> _Behavioral and Social Sciences Librarian 33_, pp. 120-124.
- <a href="https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf">"Markdown Syntax"</a> - A cheatsheet for markdown syntax 

### Acknowledgements
- Lewis, Alison M. "Creating Online Exhibits with Omeka," _Library Juice Academy Course_, October 2017.
- DHRI Curriculum, "Introduction to Git and GitHub." https://curriculum.dhinstitutes.org/workshops/git/ 
- University of Iowa, "Accessibility 101," Canvas Commons, https://uiowa.instructure.com/courses/40.

# 1. Writing for the Web

Web-based narratives are great for sharing a variety of content in an open, public space. Let's remember some important things when writing for an online environment.

1. <b>Web-based writing should be concise.</b> Say what you're going to say with simple, direct sentences. This doesn't mean it has to be short (although that's preferred), but it does warrant a more economic attitude toward words.

2. <b>Web-based writing should be accessible.</b> Web-based writing should strive to be accessible for any and all users, no matter their intellectual levels or physical abilities. In other words, you're writing for a diverse public, and not a singular or specifically-trained audience. Remember the **POUR** acronym when you're writing your narrative:

- **Perceivable** - the user can engage with elements through various senses (primarily sound and sight, or touch for haptic screens). Example: If you include an image, thoroughly describe that image with alternative text. If you include a video, make sure it has captions. The image below contains a good example of thorough alt text:

![Screenshot of a letter from "Women's Stories, W.E.B. Du Bois Papers Data" via https://sway.office.com/jnwIZkrNCACbONhA with alternative text highlighted](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/alternative-text.JPG)

- **Operable** -  a user can successfully use controls, buttons, navigation, and other interactive elements. For many, this means identifying something visually, and then clicking, tapping, or swiping.  For others, using a computer keyboard or voice commands may be the only way they can operate and control the page. 

    Look at the differences in navigation between this site's <a href="https://sway.office.com/jnwIZkrNCACbONhA?accessible=true">accessibility view</a> and it's <a href="https://sway.office.com/jnwIZkrNCACbONhA">default view</a>.

- **Understandable** - content is consistent in its presentation and format, predictable in its design and organizing patterns, is concise, multimodal, and appropriate to the audience in its voice and tone. Anyone should be able to comprehend the content and use the page with relative ease. 

    Example: a website for children that uses complex, higher-level words without defining them is not very accessible. The website would need to introduce these words with pictures and definitions (or uses less complex synonyms).

- **Robust** - Users should be able to choose the technology they use to interact with websites, online documents, multimedia, and other information formats. If something only works in one browser or with a proprietary format, it is not very accessible. 

    Example: a website with a plug-in that is outdated or not supported on all devices or browsers isn't very accessible.

    ![Broken image icon - a page with an invisible line through it](https://www.thewindowsclub.com/wp-content/uploads/2018/06/Broken-image-icon-in-Chrome.gif)

3. <b>Web-based writing should use web elements.</b> Purposefully break up your text with formatting elements (see next section), use hyperlinks where appropriate (to cite, to refer to other content, etc.), and include media to enhance and solidify the meaning of something.

### Check-in: 
Check your accesibility comprehension with the <a href="https://muw.instructure.com/courses/19899/quizzes/78701">1.Narrative check-in</a>.

# 2. Markdown

Markdown is a very simple markup language (ha! did you catch that pun?!) used for writing for the web. Put simply, Markdown allows us to format our text using simple cues. All of our course lessons are written using Markdown, with some HTML here and there. Click the ```Raw``` button at the top of any lesson's screen to see what this looks like before being translated by your computer! It will show you the text-only version, resembling:

![Markdown file in a text editor with labels showing different kinds of formatting](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/markdown-example.JPG)

Most websites use HTML (Hyper Text Markup Language), another markup language, to structure web documents that use nested labels to tell a browser how you want something displayed. Markdown and HTML work together in many cases, so while we'll mostly use Markdown, you may see (or even use) some HTML elements while formatting our narrative project. 

## Common Markdown elements

### **Headings**
Headings are marked with 1) the #, 2) a space, 3) the text, and 4) a hard return. 

In markdown, you would type ```# Heading 1```, but the computer would read:
> # Heading 1

Examples of more headings and subheadings:
![Screenshot of markdown headings from https://www.markdownguide.org/basic-syntax/](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/markdown-headings.JPG)

### **Formatting Text**
Style your text to create emphasis with:
> ```**bold**``` --> **bold** or ```*italics*``` --> *italics*

Create an ordered or unordered list:

```1. Ordered list item```

```* unordered list item 1```

```- unordered list item 2```

> 1. ordered list item
> * unordered list item 1
> - unordered list item 2

Highlight quotes with a blockquote:

```> Let's highlight this quote``` turns into
> Let's highlight this quote

### **Adding links and images**
You can instantly hyperlink something with angle brackets, like this: 
> ```<hyperlinked-URL>```

To hyperlink text, put the text in square brackets [], immediately followed by the URL in parentheses. Like this:
> ```[This is the linked text](hyperlink-URL)```

_Alternatively, you can use a bit of HTML to hyperlink text. It is one of the most common and useful bits of code to learn! HTML uses the anchor element and the hypertext reference attribute, or ```<a href>```. A full link would look like this_:
> ```<a href="example.linkhere">Linked text here.</a>```

Inserting an image is similar, but add an exclamation point to the beginning, then include square brackets containing the alt text describing it, and parentheses with the image URL:
> ```![alternative text describing the image](Image URL)```

To hyperlink an image, put square brackets around the Markdown for the image, and immediately follow that with the URL in parentheses, like this:

>```[![alternative text](image-url)](hyperlinked-url)```

For more help with markdown elements, there are free, online cheat sheets, like <a href="https://www.markdownguide.org/basic-syntax/">Markdownguide.org</a>. **Bonus**: You can insert emoji with Markdown by putting the alt text in between two colons, like this: ```:rofl:```. Here's a full <a href="https://github.com/ikatyang/emoji-cheat-sheet">cheat sheet</a>. Have fun! :wink:

<!--
## Common HTML elements
Hyperlinking text, the most powerful and simple tool of HTML, is the most common way we'll use HTML. To create a hyperlink, use the anchor element (```</a>```) to structure your text like this:

> ```<a href="hyperlinked-URL">Text you are hyperlinking.</a>```

Hyperlinking images looks a little different. To share and link an image in html, nest the image element within the anchor element, like this: 

> ```<a href="hyperlinked-URL"><img src="hyperlinked-URL" alt="insert alt text here" width="" height=""></a>```

The width="" and height="" elements allow the size of the image to be responsive to the screen. In other words, it will be as visible on a mobile device as it will be on a desktop monitor.

For more help using HTML, there are free, online tutorials available through <a href="https://www.w3schools.com/html/html_intro.asp">W3Schools.com</a>
-->

### Check-in
Create a markdown file (save it as .md) in your text editor that uses elements above for the <a href="https://muw.instructure.com/courses/19899/quizzes/78695">2.Narrative check-in</a>.

# 3. Creating a narrative project

This is the tricky part! We're going to weave the writing and artifacts we've already created into a narrative project. Here are some examples to help you think about an end product:

- [Humboldt Redwoods Project](https://hsuredwoodsproject.omeka.net/) - exhibit highlighting 
- [Starkville Civil Rights Project](https://starkvillecivilrights.msstate.edu/wordpress/)
- [Mapping Marronage](http://mapping-marronage.rll.lsa.umich.edu/)
- [Performing Archive: Curtis + "the vanishing race"](https://scalar.usc.edu/works/performingarchive/index)
- [DASH Amerikan](https://dashamerikan.scholarslab.org/)

## Designing an Exhibit
What we are essentially doing through our narrative project is creating an online _exhibit_ using the sources we've gathered (both primary and secondary) _and_ the digital artifacts we've created. But first, in order to understand the fundamentals of online exhibits, we need to know what goes into the planning and design of one. 

As you think about taking your online audience through a tour of the collection, consider the following:

* <b>Who is this audience?</b> - Who are you writing this for? What do you want to say to them and how will you communicate? What is your tone? 
* <b>What is the purpose of your narrative?</b> Think about the items you have, the ones you want to highlight, and any themes that you want to use to guide your audience through the story. In other words, what is the thesis of this story? What is the central idea of the narrative?
* <b>What pieces will you use?</b> We have amassed quite a lot of data over the course of the semester. Think about all you have collected, and how it will help you tell the story you've sketched. You may curate anything you've created/collected so far, including: 
    - Letters from the Smith Project
    - External primary sources (photographs, etc.)
    - Secondary research (book chapters, articles, websites, etc.)
    - Metadata (<-- You will need this, regardless!)
    - Projects you've already created
    - Text you've already written
* <b>How will you organize your layout?</b> What system are you using to organize your layout? Is it going to be chronological? Will it be organized by topic? This will depend on the story you want to tell, and the artifacts you have to tell it.

![examples of a chronologically organized and topically organized exhibit](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/exhibit-layout.png)

## Keep in Mind
Designing digital exhibits and writing narratives are **recursive** acts, meaning they may be constantly redesigned from the beginning of the project to the end (just like a research paper!). You may not end up with what you started in your outline. Keeping an open mind, being flexible with your plan, and keeping (somewhat) organized notes will help you throughout this process!

![Example of an exhibit outline](https://github.com/hillaryAHR/LIB-201/blob/main/narrative-images/exhibit-outline.JPG)

## Additional sections to include
In addition to the story you're telling and the artifacts you're using, you'll want to give more context about yourself, the project, AND give your audience options for further exploration. (LIB 201 students will be primarily responsible for collecting and writing this.) Include the following sections in your narrative:

1. **Home**: This is the first thing your audience will see, so this is where you introduce your project. This is where you will explain the "so what" of the project, or the research question(s) that guided your inquiry, and give any other information that will help your audience decide how to interact with the narrative.
2. **About**: This includes information about YOU, about the collection you used, why you did the project, and your process. Sometimes, the about section can include navigation or "how to" help, if there are more complex interactive portions or if there are several ways to navigate the page. 
3. **Acknowledgements**: This of this as your works cited page. This will include hyperlinks to the sources you cited, but it can also include links to related archives or projects that gave you inspiration, and it can link to other archives or sources for further research.

### Check-in
For this check-in, you will need to do some brainstorming. Be ready to:
- write the central idea/thesis/purpose statement of your narrative in 1-2 sentences.
- Brainstorm a list of the items (letters, metadata, projects, research, etc.) you'd like to focus on
- sketch an outline of the narrative itself in 3-5 bullet points

After you've considered these things, click here to complete the <a href="https://muw.instructure.com/courses/19899/discussion_topics/199943">3.Narrative check-in</a>.


