# RoleClustering
DSCI441
Recent advancements in trajectory data logging and vision-based tracking systems have made it possible to analyze individual and team behavior. Current analysis is based on original starting position only and evaluates the mean position over time (the static assumption), but such methods do not take into account the constant interchanging of player positions and contextual information of a players relative to the other roles. Given player tracking data D, we can model the role formations for the entire team. Each role within a formation is unique; no two players in a team can have the same role at the same time, but players can swap roles throughout the match. This approach allows for the detection and visualization of formations and provides contextual information for the analysis of how well individual players adhere to their role. The statistical modeling method employed is unsupervised and similar to kmeans clustering.

Methods based on:
A. Bialjowski, P. Lucey, P. Carr, Y. Yue, S. Sridharan and I. Matthews. “Large-scale analysis of soccer matches using spatiotemporal tracking data”. In 2014 IEEE International Conference on Data Mining (ICDM), 2014 
![image](https://user-images.githubusercontent.com/72851656/224083336-be919977-af99-4b45-8f66-936c2a06dc4f.png)

## Usage:
File `Redo_Soccer_Spatial_Analytics.ipynb` contains all the code necessary to run the entropy minimization and role discovery procedure. Code can be run cell-by-cell. With the necessary dependencies given in the first cell, the main loop will produce role distributions for each pass over the data set. 

## A note about the data:

It is important that player tracking data is stored as a .csv file on the same level as the main notebook. Otherwise, the data location will need to be specified relative to the main notebook when initializing the CustomDataLoader(file_path = '') class.
 
Additionally, the .csv of player tracking data should be specified with columns headers according to the following format:

Period	| Frame	Time[s]	| Player1-x	| Player1-y	| ... Player14-x	| Player14-y

