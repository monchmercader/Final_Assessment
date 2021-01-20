# Project Background


## Data Analytics with Python Course - Final Assessment
submitted by: Ramon (Monch) Mercader<br>
submitted to: Ramon Perez / Coder Academy - ramon.perez@coderacademy.edu.au<br>

Project folder contents:<br>
    - Collect_and_Clean.ipynb (File 1 of 2)<br>
    - Analyzing.ipynb (File 2 of 2)<br>
    - README.md<br>
    - Project_Background.md<br>
    - datasets (empty folder for collected datasets)<br>
    - images (folder containing images for notebooks)<br>
    - Youtube_scraper (folder containing youtube data collection script, credits in README.md)<br>


### 1. Project Title: Youtube - Trending Video Analytics Reviewer 

### 2. Project Description

<div>
    <img src="images/01_tracyliciouz_YTchannel.jpg", alt="Tracy's Youtube Channel", width="850">
</div>


Tracylizious Youtube Link - <a href="https://www.youtube.com/channel/UCWvdQQKH9LslKy2ZWnQDHLQ">http://www.youtube.com/channel/UCWvdQQKH9LslKy2ZWnQDHLQ<a/>
    
A friend of mine runs a Youtube channel, she creates content about fashion, travel, food, and hospitality.<br>
We both knew that there was a lot of similar content out there, so we were thinking that maybe a quick look into some trending Youtube videos could provide some ideas on how she could improve her own.<br>
And possibly either put her focus into content that's not so common or show her which styles work. So the main goal of this assessment is to look into trending Youtube video data and see if there are any patterns or similarities across them. And how she can improve her own content based on what we can see with trending videos.<br>
This project has been designed so it can be used continously, relying on the current trending data, and can be tweaked later if there are any changes to the Youtube API V3 service or changes in trends. The principles and questions should still hold in the future.<br>
    
The main objective of this is to get a snapshot and practice my skills in collecting data, cleaning, managing, reviewing, and visualizing the data. 
This is not an exhaustive project, it only focuses on the top trending videos for a certain timeframe and locations. 

During my initial research and consultations with a few friends in advertising and marketing, I found out that there are a lot of other platforms that can do something similar to this project. But unfortunately, these would be paid services. I also tried to review the Youtube stats and reporting interface but what I found is that it was mainly focused on a single user/channel and was intended to review the channel owner's performance. What we needed was to see all the trending videos across Youtube and have data that would be easy to review and compare. Further research showed that Youtube have conducted an end of the year report for the Top Trending videos, found here:<br>

<div>
    <img src="images/00_Youtube_2020_Top_trending_vids.jpg", alt="2020 Top Trending Videos for the U.S.", width="850"><br>
    <a href="https://blog.youtube/culture-and-trends/2020-top-trending-youtube-videos-creators">2020 Top Trending Videos for the U.S.</a><br>
    </div><br>

The blog outlined only the top-most information and mainly focused on the U.S. The data that we we're trying to gather was similar, but we wanted to get an in-depth look into this and also into other countries, namely:<br>
    - United States of America (US)<br>
    - Australia (AU)<br>
    - United Kingdom (GB)<br>
    - Singapore (SG)<br>
    - New Zealand (NZ)<br>
    - Philippines (PH)<br>

We focused on the following countries because this was her identified target audiences. Basically, where her family and friends were located.<br>

We also wanted to focus only on the categories that she creates content about:<br>
    - Travel & Events<br>
    - Video blogging<br>
    - People & Blogs<br>
    - How to & Style<br>
    - Family<br>
This is based on Youtube's content categories, during research I found out that categories vary from country to country, but the above are consistent based on the identified countries.<br>
    
We wanted to find out what the relationships between:<br>
    - Views vs Likes vs Dislikes<br>
    - Likes vs Dislikes vs Comments<br>
    - Types of content(categories) that is trending per country<br>
    - Types of content vs number of comments<br>
    - Duration of content on Trending list<br>

 
Quick Note: We did not consider video content lengths as my friend's content varied across her different videos. And as such, she did now want to video lengths to dictate her creative work.<br>
    
### 3. Data

Acknowledgement: The data collection is possible through a Python Youtube Scraper which was slightly modified from this user Mitchell J (This is his Kaggle link to his project) - <a href="https://www.kaggle.com/datasnaek/youtube-new">https://www.kaggle.com/datasnaek/youtube-new</a><br>
Direct link to the Github repository for the code - <a href="https://github.com/mitchelljy/Trending-YouTube-Scraper">https://github.com/mitchelljy/Trending-YouTube-Scraper</a><br>

This scraper grabs Top trending Youtube links from the Youtube API V3 service and writes the code to a CSV file. The Python file can be found inside the Youtube_scraper folder. Please read the README.md file inside that folder for more information. <br>

In the Youtube_Scraper folder there are 4 important files:<br>
    - README.md (this contains information around the scraper.py Python code)<br>
    - scraper.py (Python code to run, this has been modified for this project)<br>
    - country_codes.txt (Reference file that contains all the countries passed on for the API scrape call)<br>
    - api_key.txt(You Google Youtube API key which will be required as credentials to run the API scrape call)<br>
    
Please read the /Youtube_Scraper/READMME.md file, this will provide instructions on how to run the python script and collect the date. The most important part is to create your own API key. Here is a link to the instructions: <a href="https://developers.google.com/youtube/registering_an_application">https://developers.google.com/youtube/registering_an_application</a><br>
    
Once you run the file, it will write the CSV files inside the "output" folder. When done, you will need to copy these CSV files into the "datasets" folder if you wish to use them with this project.At the moment, the current country_codes.txt file contains: US(American), AU(Australian), PH(Philippine), SG(Singapore), NZ(New Zealand), and GB(United Kingdom). Country codes are based on the 2 letter international standards, you can find out a specific country code here: <a href="https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes">https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes</a><br>

The script will write the files in this format: YR.DATE.MONTH_COUNTRYCODE_videos.csv ex. 21.14.01_AU_videos.csv, this is important to note when reading the csv files. 
This means that the CSV files are separated by country and by dates. 
This worked to my advantage because now I can review the data focusing specifically on which countries we wanted. 
    
I have separated the notebooks into sections per country.<br>

The data scraper will request the following through the Youtube API v3:<br> 
        - Video ID<br>
        - Video Title<br>
        - Published date<br>
        - Channel ID<br>
        - Channel title<br>
        - Category ID<br>
        - Tags<br>
        - Number of views<br>
        - Number of likes<br>
        - Number of dislikes<br>
        - Number of comments<br>
        - Comment status<br>
        - Thumbnail link<br>
        - Rating status<br>
        - Description<br>

Link to my currently collected dataset: <a href="https://drive.google.com/drive/folders/1E_pV6Bl_CyZH-VD_uwiFkMeumpmYXDDx?usp=sharing">https://drive.google.com/drive/folders/1E_pV6Bl_CyZH-VD_uwiFkMeumpmYXDDx?usp=sharing</a><br>

Download the contents of that link into the datasets folder

### 4. Cleaning Process:
Here are my steps in cleaning the data:<br>
    1. Concatenate all the separate CSV files into one Dataframe per country<br>
    2. Check the data info: headers and total entries<br>
    3. Drop non-relevant categories<br>
    4. Remove duplicate - based on the latest views of an entry<br>
    5. Write to new CSV file for data analysis<br>

### 5. & 6. Analysis and Data Visualizations:<br>
To complement the Data Analysis I have consolidated them with the Data Visualizations: <br>
I've included the Observations after each data visualization section.<br>    
    1. What are the top trending categories per country?<br>
    2. How many views does it take to become a trending video?<br>
    3. How long does it usually take for a video to trend?<br>
    4. Exploring if there are any relationships between a video's likes and the number of comments around it<br>
    5. Content Review<br>
Please check the notebook (Analyzing.ipynb) for more visualizations and descriptions<br>

    
### 7. Conclusion
All of this is based on the currently gathered data.<br>
I really think that this notebook and the process here are a good start to reviewing and analyzing the top trending Youtube videos. <br> It provides a bit more control and transparency over what can be purchased via agencies and having to use Youtube's daily trending video and needing to write those down. <br> For this project, the datasets(csv) gathered were small enough that Excel or Google Sheets would have been able to review them. Although, in terms of control and visualization, it would have been more work. <br> But in the long run, especially when the data starts to go into months and year(not years because by then, trends would have probably changed already), this would be a lot more advantageous than having to run everything through Excel or Sheets. 

    
### 8. Future Work
I plan on using this and reviewing it by end of the month with Tracy. And then see if it's something she can use for her channel on a regular basis. <br> From there I will probably tweak a few things, mainly:<br>
- Automation, a lot of the tasks in the notebook and the scraper should be automated more. I think the scraper can be run with a cron job on a server to save time of me having to run it daily. 
- Longer timeframes, as mentioned before, I think a time period of 3, 6, and a 12 month period should be done. Hopefully, we can see where trends are going and help Tracy adjust to the coming trends of the following year
- Better visualizations, I really want to explore more data viz, but more interactive ones. To help create a simple dashboard, but have the freedom to do the code when required. Especially in finding the correlations and filtering categories and videos. 
- Adding in features like reading through Titles, comments. This can help to create an idea of context and what the videos are about. Also potentially sentiments on the comments. Then I can flesh out likes>dislikes>comment sentiments and what exactly are they saying
- Music, something that maybe A.I. can do, or in the short term, just parsing through descriptions and finding any licensing tags. This can help out in identifying what types of music people like. 
- Finally, maybe explore computer vision and A.I. to review the videos. One thing I am really interested in are the production quality and how the videos are created. Are there more talking heads? Are they cinematic? Do they have a lot of changes to scenes?

    

## END OF DOCUMENT