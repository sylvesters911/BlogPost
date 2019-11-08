# BlogPost
Using CRISP-DM process to create a blog for AirBnB data (Seattle and Boston) 

##### Table of Content
1. [Installation](#Installation)
2. [Business Understanding](#Business-Understanding)
3. [Data Understanding](#Data-Understanding)
4. [Prepare Data](#Prepare-Data)
5. [Data Modeling](#Prepare-Data)
6. [Evaluate the Results](#Evaluate-the-Results)
7. [Additional Links to View Folium Map](#Additional-Links-to-View-Folium-Map)
8. [Licensing, Authors, Acknowledgements](#Licensing-Authors-Acknowledgements)

## Installation
The code should run using the stadard Python packages (Python versions 3.*). Additional libraries that you need for this project is:
1. nltk (nltk.set_proxy('<<'proxy'>>:<<'port'>>'), nltk.downloader.download('vader_lexicon')
2. folium
3. seaborn
4. wordcloud

When using nltk sentiment analysis a proxy might have to be considered a connection can be set up by using nltk.set_proxy('<<'proxy'>>:<<'port'>>').
The vader lexicon must be downloaded using nltk.downloader.download('vader_lexicon')

## Business Understanding
Data was provided made available to understand the resent trends in property rentals, by looking at the locations relative to each other and relative to certain local attractions price number of visits can be determined and see how they vary for the properties and could potentially adjust the price accordingly. Other potential avenues to explore is how guests perceive the properties as well as their feedback. The cities considered was Boston and Seattle to better understand:

1. The average price that is charged in relation to the location of the listings relative to top 10 attractions
2. The description on the listings for advertisement 
3. What is the general feedback or sentiment from the guests by city and how their stay is experienced   

By answering these questions, the guests could have a better experience, the property owners can be more efficient and AirBnB can improve their footprint as well as overall image by optimizing their criteria in terms of price, description required from owners and also minimum amenities.

## Data Understanding
The data for as provided by AirBnB for the two cities Seattle and Boston can be obtained [here](https://www.kaggle.com/airbnb/seattle/data) and [here](https://www.kaggle.com/airbnb/boston). This data was looked at as well as inspected to see what the various attributes are. 

All the columns that was going to be used was checked by looking at the number of entries as well as the number of missing values for categorical variables. In plotting the locations none of the coordinates was missing allowing for a complete view. The descriptions of the properties also did not have any missing or null entries and could be used as such.
The sentiment analysis on the feedback by the guest saw a few missing values. As thee values was ignored and would not have a significant influence in the overall results as only 75 out of the total 153 124 records was missing.

## Prepare Data

The datasets was downloaded and inspected. It was found that the listings and review datasets will be used as the calendar data have all of the historic prices.
A merge was performed on the review and listings data, investigation show that Boston data had three additional columns and these was identified. The identified columns was deleted as they bare no interest in the analysis.

The two datasets was appended one each other and the data cleaning process began. It was found no missing values in terms of coordinates, no missing values for the descriptions of the properties. For guest feedback a small percentage was missing, these entries was dropped as the sentiment will not change so dramatically with these included.
Additional data points was added to indicate the top 10 local attractions, this data was obtained for Seattle [here]( https://www.seattletimes.com/life/travel/seattlersquos-top-10-attractions/) and Boston [here]( https://www.boston-discovery-guide.com/top-boston-attractions.html). The coordinates was obtained from maps by searching for them individually. 

## Data Modeling
Each of the questions proposed above no new machine learning model was used, descriptive statistics was provided on the number of visits as well as the price of each per location. The sentiment analysis was performed using and already trained model and the reference on this model is included below. 

## Evaluate the Results

The results can be viewed [here]() 

## Additional Links to View Folium Map

Folium maps do not render on GitHub natively, a viewer has to be used and the link to the viewer can be found [here](https://nbviewer.jupyter.org/), It likely do with the site's settings on running JavaScript. 
To view the maps on the .ipynb scripts click [here](https://nbviewer.jupyter.org/github/sylvesters911/BlogPost/blob/master/NanoDegree%20Project1%20Term2.ipynb)

## Licensing, Authors, Acknowledgements

To use the nltk sentiment analyzer the following acknowledgment must be made:

'''Hutto, C.J. & Gilbert, E.E. (2014). VADER: A Parsimonious Rule-based Model for
Sentiment Analysis of Social Media Text. Eighth International Conference on
Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014.'''

Images [here](https://github.com/sylvesters911/BlogPost/blob/master/Seattle.png) for Seattle and [here](https://github.com/sylvesters911/BlogPost/blob/master/Boston.png)
 for Boston was sourced [here](https://www.google.com/search?q=seattle+pictures&rlz=1C1GCEV_enZA846ZA846&tbm=isch&source=iu&ictx=1&fir=apRREfoghGZEwM%253A%252C2y9-WSCIHbmZRM%252C_&vet=1&usg=AI4_-kR946M9quWCEp8P7dQEHCAJvk5u9g&sa=X&ved=2ahUKEwiG3NzV6tflAhUIEcAKHTnoC80Q9QEwAHoECAcQLg#imgrc=apRREfoghGZEwM:) and [here](https://www.google.com/search?q=boston+pictures&rlz=1C1GCEV_enZA846ZA846&tbm=isch&source=iu&ictx=1&fir=8C-VIqTviVhJuM%253A%252Cl3xiktX5CWEodM%252C_&vet=1&usg=AI4_-kSRLVeT0B8JISIYS2Ejoz-SPf_avA&sa=X&ved=2ahUKEwiS7tzl6tflAhVSolwKHQEwC60Q9QEwAHoECAcQLA#imgrc=FJhNLwDX0fuJmM) respectively.
