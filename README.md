Group Members: Willaim Zhu, Sam Rubin


# Introduction

Why was the project undertaken?

We are both large fans of the card game Magic the Gathering, with the amount of cards that come out due to the popularity of the game. We were curious if a neural network could find a pattern in the art of the cards and if it correlated to their color.

What was the research question, the tested hypothesis, or
the purpose of the research?

Our goal is to find if there is some pattern / theme that exists for knowing what color a card is due to the artwork.

# Selection of Data 

What is the source of the dataset? Characteristics of data?
Any munging, imputation, or feature engineering?

We took our data from scryfall's api. They were able to return us card image urls as well as the card's color. Cards were taken from the past 10 sets and then their order shuffled. It was important to get the card art image and not the full card due to the border color giving away the card's color. The card urls were ran through a node.js package to download images locally. The images and data were then renamed. Card image sizes were also resized to be a uniform 300x300. Lastly the set was split 70-30 into training and test sets.

# Methods 

What materials/APIs/tools were used or who was included in
answering the research question?

Scryfall API, TensorFlow Keras, NPM Image-Downloader

# Results 

What answer was found to the research question; what did
the study find? Was the tested hypothesis true? Any
visualizations?
 
 ![image](https://user-images.githubusercontent.com/56366459/184983284-89d070be-c707-4e0f-9b8f-a31adce47854.png)
 
# Discussion 

What might the answer imply and why does it matter? How
does it fit in with what other researchers have found? What
are the perspectives for future research? Survey about the
tools investigated for this assignment.

We found that our model gave inaccurate results. We had a 96% on our training and 20% for test data. We believe the multi class cards gave the model more inaccuracies. The layers were also potentially too small but larger ones were not running well. For future research we would like to stick to the 5 basic colors. 

Another large factor to the small success rate is due to the design of the game. Part of the card design of magic is in that Art doesn't have to relate to the color of the art entirely. Or more so such that Magic has gone through a ton of iterations in the physical design of the cards. One of the upsides of the current style of the cards is in the surrounding information. Red cards are red on the card around the art, same with all the colors. We still think there could be a pattern found within the art. But one of the large difficulties is the way in which Magic is made. Each new expansion is set somewhere else, and as such comes with a new theme. We shift from Japanese-themed technopunk to Dungeons and Dragons inspired classic fantasy. So the sets we include contain so much distinct worlds that While there is most certainly something that you could find. It is certainly hard given the structure of the game.

# Sources:
https://scryfall.com/


