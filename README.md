# BlogPost
Using CRISP-DM process to create a blog for AirBnB data (Seattle and Boston) 

##### Table of Content
1. [Installation](#Installation)
2. [Project Motivation](#Project-Motivation)
3. [Additional Links to View Folium Map](#Additional-Links-to-View-Folium-Map)
4. [Results](#Results)
5. [Licensing, Authors, Acknowledgements](#Licensing-Authors-Acknowledgements)

## Installation
The code should run using the stadard Python packages (Python versions 3.*). Additional libraries that you need for this project is:
1. nltk (nltk.set_proxy('<<'proxy'>>:<<'port'>>'), nltk.downloader.download('vader_lexicon')
2. folium
3. seaborn
4. wordcloud

When using nltk sentiment analysis a proxy might have to be considered a connection can be set up by using nltk.set_proxy('<<'proxy'>>:<<'port'>>').
The vader lexicon must be downloaded using nltk.downloader.download('vader_lexicon')

## Project Motivation
For this project, I was interested in using AirBnB data from Boston and Seattle to better understand:

1. The average price that is charged in relation to the location of the listings
2. The description on the listings
3. What is the general feedback from the guests by city and how their stay is experienced  

## Additional Links to View Folium Map

Folium maps do not render on GitHub natively, a viewer has to be used and the link to the viewer can be found [here](https://nbviewer.jupyter.org/), It likely do with the site's settings on running JavaScript. 
To view the maps on the .ipynb scripts click [here](https://nbviewer.jupyter.org/github/sylvesters911/BlogPost/blob/master/NanoDegree%20Project1%20Term2.ipynb)

## Results

The results can be viewed [here](https://github.com/sylvesters911/BlogPost/blob/master/BlogPostResults.html) 

## Licensing, Authors, Acknowledgements

The data for Seattle data can be obtained [here](https://www.kaggle.com/airbnb/seattle/data). The data for Boston can be obtained [here](https://www.kaggle.com/airbnb/boston). To use the nltk sentiment analyser the following aknowlagment must be made:

'''Hutto, C.J. & Gilbert, E.E. (2014). VADER: A Parsimonious Rule-based Model for
Sentiment Analysis of Social Media Text. Eighth International Conference on
Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014.'''
