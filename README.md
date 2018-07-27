# Data Analysis on Google Timeline data

This is my first project on a raw and unlabeled GPS dataset. I took a deep dive and analyze every single features on this dataset, determined whether these features are accurate/useful to be used later for modeling and tried to discover the way Google record these data. I also learn to use Folium, a beautiful mapping library to map GPS points onto Leaflet map for visualization. Finally I used clustering technique (k-means) to clean up, identify and extract clusters that can review user's habit and common routine

## Outline of this project
1. [Exploring and initial data cleaning (long version)](https://github.com/anhquan0412/google-location/blob/master/cleaning_long.ipynb)
2. [Exploring and initial data cleaning (short version)](https://github.com/anhquan0412/google-location/blob/master/cleaning_short.ipynb): This is the short version if you don't want all the details. You will have a nice and clean dataframe for next steps
3. [Main Exploratory Data Analysis](https://github.com/anhquan0412/google-location/blob/master/eda.ipynb) Perform extensive analysis on all features. Determine which features are important/unimportant. Clean up abnormal GPS data points
4. [Clustering](http://nbviewer.jupyter.org/github/anhquan0412/google-location/blob/master/common_clusters.ipynb) Mapping GPS points using Folium. Perform k-means to identify dense clusters and recognize common areas such as home, work, school ... areas. Determine common habits on weekday vs weekend, day vs night

## Technical Aspect
- To get your own Google Timeline location history (in JSON file), download it from https://takeout.google.com/settings/takeout

- What you need to run these notebooks:
    - numpy + pandas + matplotlib + sklearn + seaborn. I recommend install [Anaconda](https://conda.io/docs/user-guide/install/index.html), a free distribution of Python/R for machine learning related applications that includes all these packages
    - folium: can be install with anaconda using command `conda install -c conda-forge folium `
    
## My thought on Google timeline dataset
- Besides latitudes,longitudes and timestamp, this dataset has other features such as heading, velocity, activity type and confidence. I did provide python functions to extract all of these features. However, I decide not to use these features as majority of them are not accurate (see more in my EDA notebook). This could be the result of my old model Android phone not be able to capture these features correctly. If you have a newer Android phone, feel free to test and include them in your model.
- This dataset requires a lot more cleaning than usual just to see interesting clusters.
- Google collects A LOT OF DATA from me.
- Since I work on my own dataset so I might be biased (know which clusters are more important before hand).

Let me know if you have any suggestion/correction for me. Any contribution will be appreciated! Sadly I cannot include any of my own data but feel free to use your own and let me know if you find anything interesting at my [twitter](https://twitter.com/therealquantran)
