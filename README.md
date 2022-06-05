# foursquare-location-matching

Initialization Date: 2022.05.17
Authors: Tim Gorman, Ling Zhou, Yu Cao

-------------------------------------
Repo Description
-------------------------------------

This repository was created as part of the Erdos Institutes' May 2022 Data Science Bootcamp Final Project. It contains code 
to answer the question stated under "Project Goal".

--------------------------------------
Project Goal
--------------------------------------
https://www.kaggle.com/competitions/foursquare-location-matching

When you look for nearby restaurants or plan an errand in an unknown area, you expect relevant, accurate information. 
To maintain quality data worldwide is a challenge, and one with implications beyond navigation. 
Businesses make decisions on new sites for market expansion, analyze the competitive landscape, and show relevant ads informed by location data. 
For these, and many other uses, reliable data is critical.

Large-scale datasets on commercial points-of-interest (POI) can be rich with real-world information. 
To maintain the highest level of accuracy, the data must be matched and de-duplicated with timely updates from multiple sources. 
De-duplication involves many challenges, as the raw data can contain noise, unstructured information, and incomplete or inaccurate attributes. 
A combination of machine-learning algorithms and rigorous human validation methods are optimal to de-dupe datasets.

With 12+ years of experience perfecting such methods, Foursquare is the #1 independent provider of global POI data. The leading independent location technology and data cloud platform, 
Foursquare is dedicated to building meaningful bridges between digital spaces and physical places. Trusted by leading enterprises like Apple, Microsoft, Samsung, and Uber, 
Foursquare’s tech stack harnesses the power of places and movement to improve customer experiences and drive better business outcomes.

In this competition, you’ll match POIs together. Using a dataset of over one-and-a-half million Places entries heavily altered to include noise, 
duplications, extraneous, or incorrect information, you'll produce an algorithm that predicts which Place entries represent the same point-of-interest. 
Each Place entry includes attributes like the name, street address, and coordinates. Successful submissions will identify matches with the greatest accuracy.

By efficiently and successfully matching POIs, you'll make it easier to identify where new stores or businesses would benefit people the most.

Data Description
---------------------------------------
The data presented here comprises over one-and-a-half million place entries for hundreds of thousands of commercial Points-of-Interest (POIs) around the globe. Your task is to determine which place entries describe the same point-of-interest. Though the data entries may represent or resemble entries for real places, they may also contain artificial information or additional noise.

## Training Data
* `train.csv` - The training set, comprising eleven attribute fields for over one million place entries, together with:  
    * `id` - A unique identifier for each entry.  
    * `point_of_interest` - An identifier for the POI the entry represents. There may be one or many entries describing the same POI. Two entries "match" when they describe a common POI.
               
* `pairs.csv` - A pregenerated set of pairs of place entries from train.csv designed to improve detection of matches. You may wish to generate additional pairs to improve your model's ability to discriminate POIs.  
    * `match` - Whether (True or False) the pair of entries describes a common POI.
 
## Example Test Data
To help you author submission code, we include a few example instances selected from the test set. When you submit your notebook for scoring, this example data will be replaced by the actual test data. The actual test set has approximately 600,000 place entries with POIs that are distinct from the POIs in the training set.
  
* `test.csv` - A set of place entries with their recorded attribute fields, similar to the training set.  
* `sample_submission.csv` - A sample submission file in the correct format.  
    * `id` - The unique identifier for a place entry, one for each entry in the test set.  
    * `matches` - A space delimited list of IDs for entries in the test set matching the given ID. Place entries always self-match.


Structure:
---------------------------------------
Raw Data: The raw data should be saved under a sub folder called "data_raw", and that folder
should be ignored by the .gitignore file  because the files are 
too large, per github's policy. The raw data can be found at the following link.

https://www.kaggle.com/competitions/foursquare-location-matching/data

The data has been repartitioned into smaller files which are saved under "data_curated". This data should be included
in the repo and is where data analysis should be based on.

Contributor Code:
--------------------------------------
To start, the code is broken out by contributor. For example code written by Tim is under "tim_code".

Project Code
--------------------------------------

The code for the final project should be stored under "group_code". The exploratory data analysis and data engineering code can be found in "4square-eda2.0.ipynb" and the  modeling code can be found in "Final_Modeling.ipynb". The data used for modeling can be found under "./data_curated/pairs_us_diffs.csv".

