
# Sentiment Analysis based on Instagram Image Posts (SAIIP)

This program analyzes sentiments of Instagram image posts about the person,  based on :
* Text Sentiment Analysis
* Face Recognition and matching with images
* Text Recognition and sentiment analysis on images
	 
Additionally, it compares and generates results of election based on sentiment analysis results of individuals.


## INSTRUCTIONS

The main required program is python 3 (the base version it was done is python 3.6.0)
-  [python 3](https://www.python.org/downloads/release/python-360/)

##  Python modules:
	
*   nltk
*   exifread
*   re
*   os
*   face_recognition
*   sys
*   pytesseract
*   argparse
*   cv2
*   os
*   pytesseract
*   nump
   
   for Installing modules run on the command line:
```  
   pip install nltk
   pip install exifread
   pip install re
   pip install os
   pip install face_recognition
   pip install sys
   pip install pytesseract
   pip install argparse
   pip install cv2
   pip install os
   pip install pytesseract
   pip install nump
```   


  ##### Downnload and install 
- [Tessaract OCR](https://excellmedia.dl.sourceforge.net/project/tesseract-ocr-alt/tesseract-ocr-setup-3.02.02.exe)
	set the path:  *C:/Program Files (x86)/Tesseract-OCR*  (or change the path in python code file)
	
You need to have nltk data (suggested path *C:\nltk_data*)
However running there python script automaticly doenlads it
```python
import nltk
nltk.download('words')
nltk.download('punkt')
nltk.download('stopwords')
```

	

## Run
run the command in the bash/cmd line
```
python main.py
```
In order to see full-color output please run any bash (Ex. Git Bash) 
*Note: There are separate scripts in the additional folder, but the main.py file already integrates them*

## Data Post Structure
All data of Instagram image post is encoded in the image file as **EXIF** which contains:
- Image itself
- Date and Time as filename (Ex. "2015-10-20 20.26.40 1100310046166809303_1834271085.jpg")
- Hashtags (as 'tag' Description tag)
- Autor (as 'Author'  description tag)
- Post Text (as description 'User Comment' tag)
![alt text](https://raw.githubusercontent.com/glaba13/ImageResources/master/readme-pictures.png)


## Parameters

* **ASCII_ART**  - Enable or Disable ASCII art Characters)
* **NEUTR_THRESHOLD**   - Threshold level of neutral when post results are discarded
* **DIFF_THRESHOLD**   - Difference threshold of negative and positive to include the post as a valid result
* **SCALE_MATCHED_FACE**  - Scaling factor of sentiment results when a face is matched
* **WIDTH_LINE**  - the number of characters of the line of the terminal
* **POPULARITY_H** - popularity factor of the H candidate
* **POPULARITY_T** - popularity factor of the T candidate


## Data collection
- The data is collected with Instagram Developer [API] https://www.instagram.com/developer/
- The ready application as an implementation API is [4k Stogtram] (https://www.4kdownload.com/products/product-stogram)
--  *Note that small and medium-size data already exist in the given files, for full download you will need non-free license*
but it takes lots of memory (700GB+) and time

## Datasets
The folder includes **Small Dataset** (~50 images) and **Medium Dataset** (5000 images)
for reducing error you need you to have all data **Large Dataset**(6 million) which takes 3 days processing and 
700+GB memory.


## Useful links and acknowledgment

Here are useful link and reused sub codes (for some helful funcitons) by suggestion of users and authors of different repositories:

* http://www.nltk.org/nltk_data/
* https://en.wikipedia.org/wiki/Stemming
* https://github.com/matchado/HashTagSplitter/blob/master/split_hashtags.py
* https://machinelearningmastery.com/clean-text-machine-learning-python/
* https://www.analyticsvidhya.com/blog/2018/08/a-simple-introduction-to-facial-recognition-with-python-codes/
* https://www.pyimagesearch.com/2017/07/10/using-tesseract-ocr-python/
* https://excellmedia.dl.sourceforge.net/project/tesseract-ocr-alt/tesseract-ocr-setup-3.02.02.exe
* https://github.com/bharathirajatut/python-data-science/blob/master/handwritten-digit-recognition/google-tes-text-ocr.py