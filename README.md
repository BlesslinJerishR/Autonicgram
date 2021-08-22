
<p align="center">
  <img src="https://pbs.twimg.com/profile_images/1232518700/Endhiran-Movie-Wallpapers-6_1_.jpg" width="154" style="border-radius: 8px; border: 3px solid #FF0000;">
  <h1 align="center">Autonicgram</h1>
  <p align="center"> <b>Automates</b> your Instagram posts by taking images from sites like 9gag or other Instagram accounts and posting it onto your page. 
  </p>
  <p align="center">
    </a>
    <a href="https://github.com/SeleniumHQ/selenium">
      <img src="https://img.shields.io/badge/built%20with-Selenium-yellow.svg" />
    </a>
    <a href="https://www.python.org/">
    	<img src="https://img.shields.io/badge/built%20with-Python3-red.svg" />
    </a>
  </p>
</p>

[comment]: <> (<p align="center">)

[comment]: <> (  <img src="#" width="">)

[comment]: <> (</p>)

## Features

* Adjustable interval between posts   
* Original captions/title as post captions  
* Multiple 9gag categories   
* Log into Instagram with Facebook credentials 
* Duplicate post prevention  
* Get Instagram users past photos and add to queue  
* Max post limit  
* Listens for new images 
* Automatically resizes images to fit Instagram  
* Simulates real clicking
  
## Installation  
  
Clone :
```sh
git clone https://github.com/HenryAlbu/auto-Instagram-posting-bot.git
```

Directory : 
```sh
cd auto-Instagram-posting-bot 
```

Requirements :
```sh
pip install -r requirements.txt
```  

Selenium <b>chromedriver</b>.
[Download](https://sites.google.com/a/chromium.org/chromedriver/downloads) & drag and drop it into the directory.

## Running
Execute : 
``python app.py``

## File structure

| Files/Folders | Description |
| --- | --- |
| app.py | The main file for the project contains the UI and connections calls the other files. (Run this file) |
| insta.py | Contains the functions and steps that sign you into Instagram. Also contains the Selenium driver options |
| ninegag.py | Contains the functions to download and queue up 9gag posts   |
| settings.py | Contains the global variables   |
| insta_scraper.py | Contains the functions to download and queue up scrapped Instagram posts from selected user   |
| filesCheck.txt | (created on initial run) Contains the id's of images that have been downloaded to prevent duplicate uploads (keeps the last 50 id's) |
| filesDict.json | (created on initial run) When images are downloaded they are given an id's and put into this JSON file that acts as the queue |
| images (folder) | (created on initial run) Where the images are downloaded to.  |

  
  
## UI - PySimpleGUI

https://github.com/PySimpleGUI/PySimpleGUI

[comment]: <> (<p align="center">)

[comment]: <> (  <img src="#" width="70%">)

[comment]: <> (</p>   )

## Limitations  
  
Currently, the bot only uploads images. This is due to the fact that it is using Selenium to interact with the Instagram web interface. The Instagram interface only allows for uploads of images. (currently looking into a way around this)
  
## Caution 
  
This project uses Selenium. What this means is that it does not use the Instagram API for posting, making Instagram think that it's a real user posting, **BUT**
You should still be cautious by setting a reasonable wait time before posts. By default, this is set at 50 seconds. If you set it to something like 10 seconds, there is a chance that Instagram will notice bot activity. 

# TODOs

* Adding Imgur.com to the list of options to take images

* Ability to add your own files to queue. Kind of like those sites that charge you to schedule Instagram posts.

* Figuring out how to get videos to upload

#### [ Developer : Mastermindx33 ]