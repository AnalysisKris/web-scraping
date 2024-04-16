# P6: Web Scraping and NLP with Requests, BeautifulSoup, and spaCy
## Completed by: Kristen Finley
#
### Github Repository Link: [https://github.com/AnalysisKris/web-scraping](https://github.com/AnalysisKris/web-scraping)
### Class: 44620- WEB MINING & APPLIED NLP 8081SP24
#

## Rubric

* (Question 1) Article html stored in separate file that is committed and pushed: 1 pt
* (Question 2) Article text is correct: 1 pt
* (Question 3) Correct (or equivalent in the case of multiple tokens with same frequency) tokens printed: 1 pt
* (Question 4) Correct (or equivalent in the case of multiple lemmas with same frequency) lemmas printed: 1 pt
* (Question 5) Correct scores for first sentence printed: 2 pts (1 / function)
* (Question 6) Histogram shown with appropriate labelling: 1 pt
* (Question 7) Histogram shown with appropriate labelling: 1 pt
* (Question 8) Thoughtful answer provided: 1 pt


#
## Objectives:
 This exercise is used to practice web scraping (fetching and extracting information) and processing the content from a web page.

#
## Introduction:
Complete the tasks in the Python Notebook in this repository.
Make sure to add and push the pkl or text file of your scraped html (this is specified in the notebook):
#
### Task 1. Get Started
Copy the base repository into your GitHub account by selecting the "Use this Template" button on GitHub and specifying yourself as the owner.  The base repository is available at: https://github.com/wmnlp-materials/web-scrapingLinks to an external site.
Clone YOUR new repo down to your machine.
 

### Task 2. Open Notebook and Complete Tasks 
On your machine, open the Jupyter Notebook for editing. 
Required: In your Markdown introduction, add a viewable, clickable link to your GitHub repo after your name. Build your brand and make your Markdown introduction clear and professional. 
Required: Use Markdown headings  (e.g. Question 1) to clearly show your content by each question number. 
Complete the first task.
Execute the notebook. Commit and push to GitHub. Verify your notebook appears correctly.
Complete the second task.
Execute the notebook. Commit and push to GitHub. Verify your notebook appears correctly.
Work this way until all tasks have been completed. 
 

### Task 3. Export to HTML and Finalize Repo
Execute each notebook.
After executing, export each notebook to HTML.
Commit and push your HTML files to your GitHub repo along with the executed notebooks. 
Verify you have a professional README.md that introduces your GitHub repository and provides helpful information about your project. 
 
#
## Requirements
Markdown introduction with name and clickable link is required.
Markdown Section Headings for each Question are required. 
Execute your code before exporting HTML and pushing notebooks. (See FAQ for help.)  
Unexecuted code is not eligible for credit.

#
## Reflections 
If any of these are unfamiliar, do a quick search or ask your favorite AI assistant to fill you in. 
Use your resources to grow your vocabulary and exposure - there's way too much to memorize, but understanding key terms can make us much more productive.

(Note: The following are AI generated responses)
## What is a token?
    In the context of spaCy NLP (Natural Language Processing), a token refers to a single atomic unit of text that has been segmented from the input text. It can be a word, punctuation mark, whitespace, or any other meaningful unit identified during the tokenization process.

    When you process text using spaCy, one of the initial steps is tokenization, where the text is split into tokens. These tokens serve as the basic building blocks for further NLP tasks such as part-of-speech tagging, named entity recognition, dependency parsing, and more.

    For example, consider the sentence: "The cat sat on the mat."

    After tokenization, the tokens in this sentence might include:
- "The"
- "cat"
- "sat"
- "on"
- "the"
- "mat"
- "."
    Each of these tokens represents a separate unit of meaning within the sentence. SpaCy's tokenization process also handles complex cases like contractions, hyphenated words, and punctuation marks, ensuring that each token accurately represents a meaningful segment of the text for downstream NLP tasks.

## What is a lemma?
    In linguistics and natural language processing (NLP), a lemma refers to the base or dictionary form of a word. It is the canonical, or dictionary, form of a word, which may include its root form or its infinitive form for verbs, singular form for nouns, and so on. For example:
- The lemma of the word "running" is "run".
- The lemma of the word "mice" is "mouse".
- The lemma of the word "was" (the past tense of "is") is "be".

    Lemmatization is the process of reducing words to their lemma forms. It is commonly used in NLP tasks to normalize text, allowing for better analysis by collapsing inflected or derived forms of words into a single canonical representation. This helps to reduce the vocabulary size and improve the accuracy of downstream tasks such as text classification, sentiment analysis, and information retrieval.

## What is BeautifulSoup?
    Beautiful Soup is a Python library used for web scraping HTML and XML documents. It provides tools for parsing HTML and XML documents, navigating the parse tree, and extracting data from these documents in a simple and intuitive way.

    With Beautiful Soup, you can parse HTML or XML documents obtained from the web and extract information such as tags, attributes, and text content. It offers features like:

1. **Parsing**: Beautiful Soup parses HTML and XML documents and creates a parse tree that you can navigate and manipulate.

2. **Tag Navigation**: You can navigate the parse tree using methods like `.find()`, `.find_all()`, `.select()`, etc., to locate specific tags or elements based on their attributes, classes, or other criteria.

3. **Data Extraction**: Once you've located the desired tags or elements, Beautiful Soup provides methods to extract data from them, such as `.text`, `.get()`, `.find_next_sibling()`, etc.

4. **Modifying Documents**: Beautiful Soup also allows you to modify the document by adding, modifying, or removing tags and attributes.

Here's a simple example of using Beautiful Soup to scrape data from a web page:

```python
from bs4 import BeautifulSoup
import requests

# Fetch the HTML content of a web page
url = 'https://example.com'
response = requests.get(url)
html_content = response.text

# Parse the HTML content using Beautiful Soup
soup = BeautifulSoup(html_content, 'html.parser')

# Extract information from the parsed HTML
title = soup.title.text
paragraphs = soup.find_all('p')
for paragraph in paragraphs:
    print(paragraph.text)
```

    In this example, Beautiful Soup is used to parse the HTML content of a web page obtained through a HTTP request (`requests.get()`). Then, it extracts the title of the page and prints out the text content of all paragraphs (`<p>` tags) found in the page.

## What is spaCy?

    In spaCy, a pipeline refers to a sequence of processing steps that are applied to a text when it is processed using the spaCy library. Each step in the pipeline performs a specific task, such as tokenization, part-of-speech tagging, named entity recognition, dependency parsing, and more.

    The default spaCy pipeline typically includes the following components:

1. **Tokenizer**: The text is first tokenized into individual words, punctuation, and other meaningful units known as tokens.

2. **Part-of-Speech (POS) Tagger**: Each token is tagged with its part-of-speech category, indicating whether it is a noun, verb, adjective, etc.

3. **Dependency Parser**: The syntactic structure of the sentence is analyzed, and dependencies between words are determined, showing the relationships between tokens in the sentence.

4. **Named Entity Recognizer (NER)**: Named entities such as persons, organizations, locations, dates, and more are identified within the text.

5. **Text Classifier (Optional)**: In some pipelines, a text classification component may be included to perform tasks such as sentiment analysis, topic classification, or intent detection.

6. **Entity Linker (Optional)**: If included, this component links named entities in the text to entries in a knowledge base or database, providing additional context or information about the entities.

    Each component in the spaCy pipeline is designed to be modular and efficient, allowing you to customize the pipeline by adding, removing, or modifying components to suit your specific NLP tasks. You can also create custom pipelines tailored to your application's needs by selecting and combining different components in the desired order.

## What is a spaCy pipeline?
    In spaCy, a pipeline refers to a sequence of processing steps that are applied to a text when it is processed using the spaCy library. Each step in the pipeline performs a specific task, such as tokenization, part-of-speech tagging, named entity recognition, dependency parsing, and more.

## What are stop words and how are they used to improve results?
    Stop words are common words that are often filtered out during the preprocessing of natural language text due to their high frequency and lack of meaningful semantic content. These words typically include common words such as "the," "is," "and," "in," "of," "to," etc.

    Stop words are removed from text before further processing or analysis in tasks such as text mining, information retrieval, and natural language processing. Removing stop words can improve the performance and efficiency of these tasks in several ways:

1. **Reducing Noise**: Stop words often occur frequently in text but carry little semantic meaning. By removing them, we can reduce the amount of noise in the data and focus on the more informative words.

2. **Improving Efficiency**: Stop words occupy space in memory and can increase the computational complexity of text processing tasks. Removing them can improve the efficiency of algorithms by reducing the size of the data to be processed.

3. **Improving Relevance**: In information retrieval tasks, removing stop words can help improve the relevance of search results by focusing on the more meaningful terms in the query or document.

4. **Improving Accuracy**: In some NLP tasks, such as sentiment analysis or text classification, removing stop words can help improve the accuracy of the model by reducing the impact of common, non-discriminative words on the classification or analysis results.

    However, it's essential to note that the list of stop words may vary depending on the specific task, domain, or language being analyzed. Additionally, in some cases, retaining certain stop words may be beneficial, depending on the context or requirements of the task at hand. Therefore, stop words should be handled with care and tailored to the specific needs of the analysis or application.
## What is whitespace?
    Whitespace refers to any sequence of space characters, tabs, newline characters, or other non-printable characters that are used to separate words, symbols, or other elements in a document or piece of text. In programming languages and markup languages, whitespace is often used for formatting and readability purposes and is typically ignored by compilers, interpreters, or parsers.

Common examples of whitespace characters include:

1. **Space**: The space character (``) is the most common whitespace character, used to separate words and symbols in text.

2. **Tab**: The tab character (`\t`) is used to indent text or align elements in a document or code.

3. **Newline**: The newline character (or line break) is used to start a new line of text. It can be represented by various escape sequences depending on the programming language, such as `\n` in Python or `\r\n` in some other languages.

4. **Carriage Return**: The carriage return character (`\r`) moves the cursor to the beginning of the current line without advancing to the next line. It is often used in combination with the newline character to represent line breaks.

    Whitespace is essential for human readability and code formatting but is typically ignored or treated as a delimiter by computers during text processing, unless specifically required for the task at hand. However, in certain contexts, such as within string literals or when processing structured data formats like XML or JSON, whitespace may carry semantic meaning and need to be preserved or handled accordingly.