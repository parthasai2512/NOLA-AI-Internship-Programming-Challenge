# NOLA-AI-Internship-Programming-Challenge

Overview:
We need to accept uploads of photos of people's driver's licenses and extract their name and
the expiration date. If the license has expired, we need to warn the user and reject the
submission.

Challenge:
Create a python 3.10+ proof of concept script using whatever module(s) or APIs work best (do
not use anything that costs you money) to extract the required information from the sample
image. You do not need to accept uploads for this proof of concept. Print a warning or raise an
error about expiration.

Example output:

Run with img1.png
John Sample
Expires: 02/15/2027
Accepted

Run with img2.jpg (may be harder to extract name, so any piece of a name works here)
License Sample
Expires:10/01/2016
Warning: Expired

///////////////////**** work flow of code and case scenario based outputs****////////////////

# Introduction:

All the images which are used for validation in the code are in the folder of "NOLA-AI-Internship-Programming-Challenge\DL Images", I request NOLA AI code testers to download the images from this location or from their respective testing environment. 

# Required libraries to be installed before running the code(requirements):

     !pip install easyocr torchvision keras-ocr paddleocr paddlepaddle
     
# Necessary libraries to be imported and their libraries purpose:

    # re- for regular experssion operations used in finding the text patterns.
    # cv2- for image processing like reading, converting into the grayscale, reducing the noise.
    # thresholding into binarize the image, and saving the grayscale images.
    # os- is for interacting with the os for file path operations etc.
    # datetime- For date and time operations.
    # matplotlib.pyplot- for displaying the images which are uploaded(this process is for validation.
    #purpose only and completely optional).
    # PaddleOCR- required package, for optical character recognition for extracting the information or text.
    # from the uploaded images. 

# Run the code:

 NOLA_AI_Programming_challenge.ipynb

 NOLA AI testers are requested to run above mentioned jupyter environment file to check the output and further validation of the code.

 Images paths are to be passed in the list format, and images are available from this path "NOLA-AI-Internship-Programming-Challenge\DL Images" or they can upload from their local environment as well. 

# Class and functions naming conventions used: 

below code has single class("DateProcessor") and several functions("_clean_text","_find_dates", _parse_dates,_handle_two_digit_year, process, extract_names_by_patterns,extract_names_by_special_cases,preprocess_image,recognize_text_from_image,) for image to be processed and extract text from it and 
all the functions are then passed to one "main" function.


# output from the code:

The code is satisfying the requirements of NOLA-AI Internship Programming Challenge(Example output) and also I have tested the additional special cases as well which is satisfying the requirements of the programming challenge:

1. Challenge output: Here the date and name are extracted from the image, here the name is annotated(1,2) so code logic is designed as to satisfy the requirements of the challenge.
   
Run with: /content/drive/MyDrive/NolaImages/img1.png
	John Sample
	Expires: 02/15/2027
	Accepted
 
2. Challenge output: Here the date and name are extracted from the image, here the name is annotated with special character(",") hence the code logic for name extraction using regular expressions so as to staisfy the requirements.
 
Run with: /content/drive/MyDrive/NolaImages/img2.jpg
	License Sample
	Expires: 10/01/2016
	Warning: Expired

Run with: /content/drive/MyDrive/NolaImages/dl_12.jpeg
	License Sample
	Expires: 12/30/2016
	Warning: Expired

Run with: /content/drive/MyDrive/NolaImages/dl_21.jpg
	Marie Michelle
	Expires: 10/31/2029
	Accepted
 
3. Challenge output: Here the date and name are extracted from the image, and the name is annotated with some numeric values '1' and '2' hence the code logic is articulated accordingly to statisfy the reqirements.

Run with: /content/drive/MyDrive/NolaImages/dl_234.png
	Jane Q Public
	Expires: 11/14/2023
	Warning: Expired

Run with: /content/drive/MyDrive/NolaImages/dl_993.png
	John Lewis Sample
	Expires: 10/27/2028
	Accepted
 
4. Challenge output: The date and name are extracted from the image, and this is special case of the name variable where there is no annotation by any kind which is referring to the one of the example output(Run with img2.jpg (may be harder to extract name, so any piece of a name works here) instructions, which are used to satisfy the challenge requirements.
   
Run with: /content/drive/MyDrive/NolaImages/dl_13.jpeg
	License Sample
	Expires: 10/17/2026
	Accepted

5. Challenge output: Date and name are extracted from the image of my driver's licenses, we can say that this is satisfying the latest driver's licenses format as well here the name is annotated as "1." and "2" for first name and last name.
   
Run with: /content/drive/MyDrive/NolaImages/my_dl.jpg 
  Munivenkataparthasai Madallapale
  Expires: 12/12/2024
  Accepted


  # Note: Here the code is satisfying the programming challenge as per the Example output. Also, I have tested above additional special cases as well in order to satisfy the NOLA AI internship programming challenge. 





