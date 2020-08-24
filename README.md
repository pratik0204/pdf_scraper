# pdf-scraper

pdf-scraper is an open source API for :

- extracting text from PDFs
- extracting filtered-text from LinkedIn resumes

## Demo

You can try the [demo](http://ashutoshpanda01.pythonanywhere.com/).

### Installation(Ubuntu)

```bash
git clone https://github.com/aashutoshPanda/pdf_scraper.git
apt-get install python-dev libxml2-dev libxslt1-dev antiword unrtf poppler-utils pstotext tesseract-ocr
pip install -r requirements.txt
python3 app/main.py
```

##Tasks
Code for each task is present in seperate folders
Task 4 is the repo itself.

##### Task 1

- Downloaded 50 LinkedIn resumes and added to task_1 folder.
- Screenshot of 50 files is present in task_1 folder to reduce space

##### Task 2

- Used 'textract' library to get text from all the pdfs
- pdf_to_text.csv is generated by running the main.py script present in task_2 folder

Instruction to run

```bash
git clone https://github.com/aashutoshPanda/pdf_scraper.git
apt-get install python-dev libxml2-dev libxslt1-dev antiword unrtf poppler-utils pstotext tesseract-ocr
pip install -r requirements.txt
python3 task_2/main.py
```

##### Task 3

- For Removing stop-words from a given text NLTK's stop-word list
- Some words are not present in the NLTK's stop-word list so calucated count of unique words across 50 PDF's and the words which were present in 85% of the PDF's were added to the stop-word list
- Then for each word present in the given text we can whether it is present in our updated stop-word-list or not

Instruction to run

```bash
git clone https://github.com/aashutoshPanda/pdf_scraper.git
apt-get install python-dev libxml2-dev libxslt1-dev antiword unrtf poppler-utils pstotext tesseract-ocr
pip install -r requirements.txt
python3 task_3/main.py
```

##### Task 4

- Using our functions from Task 2 & Task 3 we can make the required API
- Running the flask app we are presented with two forms to get
  text from PDFs
  filtered text from linkedIn resumes (PDF)
- The routes namely 'text' & 'text_without_stopwords' perform these tasks
- The API is hosted at pythonanywhere at [pdf-scraper](http://http://ashutoshpanda01.pythonanywhere.com/ "pdf-scraper")
