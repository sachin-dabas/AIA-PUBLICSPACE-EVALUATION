# AIA-Public_Space_IAAC, MaCAD-2021 (WIP)
The following repository is the collection of all the data used for evualuation of a Good Public Space. We used NLP, Image segmentation and space syntax analysis.
Our Project deals with the focus on evaluation of the User Perception using ML to understand the notion of a Good Public Space. The questions that we are trying to resolve include What features of a existing Public Space are Users most excited about? To what are the aspects do Users want these features? And overall, how can we integrate the Users feedback into the design process?


The Methodology:
01// NLP: The process of Natural Language Processing involves understanding the underlying information in texts. The NLP method that we used included 2 main analysis ; sentiment and topic modeling. The process of NLP includes following;

01: COLLECTION OF DATASET
02: TOKENIZE DATA
03: REMOVE STOPWORDS
04: STEMMING
05: LEMMATIZATION
06: COUNT VECTORIZATION
07: EDA
08: WORD CLOUD 
09: SENTIMENT ANALYSIS
10: TOPIC MODELING

We ran the Polarity/ Subjectivity Analysis onto the Dataset for each Public Square to get the overall popularity scores. Here, you see the example of Placa de Catalonia that shows the Positive Sentiment for most of the reviews.  But this method needed to still be refined in order to extract meaningful data that could be related to the features of the image segmentation. Hence we trained a LDA model to get coherence values for number of topics in the data and identified the most popular words in each topic. The PCA analysis showed us which are the most distinctive topics from the dataset and we could extract 5 main categories from the data based on PCA.  This was the first part of the analysis , in order to link this data to the features of the image segmentation , we identified the frequency of each popular words in each topic and assigned a value between 0 to 1 based on token values that we got from the PCA analysis.  Here you can see the 14 categories of image segmentation that are relatable to the 5 categories of NLP. 

02// SEMANTIC SEGMENTATION FOR SATELLITE IMAGERY:
Public spaces are different. Some are open and quiet while others are busy and compact, others wide and empty, while others are full of amenities and features. Having in mind the idea of creating a replicable method, we have chosen to work with semantic segmentation for satellite imagery which refers to the process of linking each pixel in an image to a class label - our urban features. By identifying these features - benches, trees, vegetation, pavements, fountains, etc. -  we were capable of understanding the percentage of each one in a certain space, measuring the ones with more impact and understanding the proportions between them. By doing so, our perception from the spaces could be, in a better way, connected to the user experiences and their perception of the space.

03// SPACE SYNTAX:
Space Syntax has been explored to add a layer of  contextual urban information to better understand the nature of urban squares. Values of urban squares  are generated for three space syntax analysis criteria using the plugin DecCodingSpaces Toolbox.  Space Syntax values provide information about eye level visibility graph derived from the public square spatial layout in three aspects. The average visibility area of a public square, the compactness which defines the ratio of the square of the perimeter to the area, and finally the average value of circularity in a public square. As a result, these space syntax values were then compiled with both sentiment analysis as well as image segmentation analysis for all the public squares to better understand the correlation between these different analyses and draw through graphs conclusions and understanding for what characterizes a good square from a less preferable one.

04// TOOL:
A: Select the site imagery of the public square to analyze. 
B: Run the semantic segmentation on it to identify the urban features.
C: Get the scores for the segmentation.
D: Run space syntax analysis for the square from the .gh file
E: Get the google reviews from the google maps (OPTIONAL)
F: Plot the results for comparision
