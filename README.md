# README.MD


## Data Analytics with Python Course - Final Assessment
submitted by: Ramon (Monch) Mercader

This repository is a submission as part of the Data Analytics course final assessment<br>
submitted to: Ramon Perez / Coder Academy - ramon.perez@coderacademy.edu.au<br>

Project folder contents<br>
    - Collect_and_Clean.ipynb (File 1 of 2)<br>
    - Analyzing.ipynb (File 2 of 2)<br>
    - README.md<br>
    - Project_Background.md (markdown file with project documentation and results)<br>
    - datasets (empty folder for collected datasets)<br>
    - images (folder containing images for notebooks)<br>
    - Youtube_scraper (folder containing youtube data collection script, credits in README.md)<br>
    
### Project Title: Youtube - Trending Video Analytics Reviewer

### Summary: 
This Repository is part of the Data Analytics with Python Course submission at Coder Academy. Please read the Project_Background.md file for further reading into the submitted work.
Files contained have been divided into the data gathering python script(folder), data collection and cleaning Jupyter Notebook, Analysis notebook, and folders for the datasets and relevant images. 
The intention of this repo is to allow other users to download and use the methods outlined in the Project background in case they wish to conduct the same research or iterate over it.
This is not meant to be an extensive Youtube statistics and analytics review, the intent of this project is to purely see the relationships between trending youtube video views vs. the likes, dislikes, and comments. And other relevant data around these. Again, more info and context around this and the results can be found in the Project_Background.md file. 

IMPORTANT NOTE: The datasets folder is intentionally empty to allow other users to collect their own data. If you wish to see the data collected for this project, please refer to the Project_Background.md file  for a link. 

### Data (How to get the data to reproduce for this project):
Acknowledgement: The data collection is possible through a Python Youtube Scraper which was slightly modified from this user Mitchell J (This is his Kaggle link to his project) - <a href="https://www.kaggle.com/datasnaek/youtube-new">https://www.kaggle.com/datasnaek/youtube-new</a><br>
Direct link to the Github repository for the code - <a href="https://github.com/mitchelljy/Trending-YouTube-Scraper">https://github.com/mitchelljy/Trending-YouTube-Scraper</a><br>

This scraper grabs Top trending Youtube links from the Youtube API V3 service and writes the code to a CSV file. The Python file can be found inside the Youtube_scraper folder. Please read the README.md file inside that folder for more information. <br>

IMPORTANT NOTE: Once you run the file, it will write the CSV files inside the "output" folder. When done, you will need to copy these CSV files into the datasets folder if you wish to use them with this project. Also, the file currently reads the US(American), AU(Australian), PH(Philippine), SG(Singapore), NZ(New Zealand), and GB(United Kingdom) Youtube top trending videos. 


### Results:
The project was successful in gathering the relevant Youtube data from the identified countries. And was able to collect, clean, and isolate the required elements of the data. 