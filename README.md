# Social Street Smart

The rise of the Internet has also birthed challenges such as abusive language, fake news, click-baits, and security threats. Fake news, in particular, can skew perceptions and influence major events like elections. Click-baits, with sensationalized headlines, waste users' time by not delivering promised content. Malicious websites pose security risks, targeting unsuspecting users. This project aims to develop a Chrome Extension to safeguard users, ensuring a more informed, productive, and safer online experience.


# Tech Stack and Skills Used

-   JavaScript, Chrome Extension Development(Node.js, Gulp packages, WebD)
-   Python, Flask REST API, PostgreSQL Database, Flask-SQLAlchemy
-   Good Hands on experience with Machine Learning and Natural Language Processing: NN, RNN, SVM, feature engineering, text processing, text similarity, Word and sentence Embeddings, etc.
-   familiar with AWS instance and how to host API on it and universal port forwarding.



The file explorer is accessible using the button in left corner of the navigation bar. You can create a new file by clicking the **New file** button in the file explorer. You can also create folders by clicking the **New folder** button.

# APIs developed so far


## Fake News API

**Divided into two parts:**


**Frontend/ Chrome extension part:** Regular struct like all other chrome extensions. content scripts facebook.js, twitter.js, newsWeb.js, scraps news post and send it to server-side for its verification.

**Backend/ Server-side:**


**Fake News/ML: **consist of all py script to do text-processing, generate embedding, generate hand feature and model weight for ML model. Jupyter notebook on trained model is also attached within this repo.

**Fake News/News_Scrapper:** scripts to scrap news and authentic news from two websites on a regular interval with help of News-please API.

**Fake News/ DB:** contain Postgres DB table definition to store news.

**Fake News/ Cache:** definition of Cache table to store the result from various source so that we don't need to call ML model always for the same post.

**Fake News/ application.py:** main Flask APP which handles post request, Scheduled scrapping of news, etc.

**Fake News/ API_manager.py **: app manager to handle DB migration and hosting.

## News Origin API

**Profanity Word Blur**
This functionality searches for the profanity words on the webpage and if found they are blurred.

**Objectionable website alert**
When the user visits a News website it displays a chrome notification containing information like bias/ownership of the webiste.

**Marking Clickbaits on Social media sites**
This functionality checks if the links shared on Twitter, Facebook and Youtube are clickbait and if they are the Chrome Extension marks them as clickbait.

**Probable News Origin**
Using this functionality one can find the probable origin of a viral news piece or a rumour. Select a piece of text right click and select Get probable Origin option and soon a chrome notification showing the probable News Origin would be displayed. This can't always tell the source of the news with 100% accuracy but it definitely shows what type of websites are publishing news similar to it. For example for a satire news piece you are likely to get sites like Reddit and Onion as output but not no nonsense sites like Guardian and C-Span.

The News Origin API would perform better if the user has their own set of API keys. To do so, follow these steps:

- Go to https://developers.google.com/custom-search/v1/introduction

- Click on Get a Key

- Click on Select or Create a new project

- Create a project called NewsOriginAPI (You can name it anything you want) and click Next

- An API Key would be generated. Copy and it save it somewhere. You can input this key in the settings page of Social Street Smart's Chrome Extension.

Or you can open https://developers.google.com/custom-search/v1/introduction and follow this video guide https://youtu.be/hZP4H0Ox3Ik

## Disinformation in Images API

The tool allows users to search the web for any image's usage. It provides data on where the image appears online. Utilizing an open-source corpus, it assesses the website's factual reliability. This determines the trustworthiness of the image's use. Users can verify if a source is credible based on its image use.

The Disinformation in Images API requires you to generate a set of custom API keys for yourself.
- Please follow these steps to obtain a JSON file containing your API keys: https://youtu.be/1Oz5TfwvhfQ.
- You can then input this JSON file on the settings page of Social Street Smart's Chrome Extension.
