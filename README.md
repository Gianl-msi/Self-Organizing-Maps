# Self-Organizing-Maps
A self-organizing map (SOM) is a type of artificial neural network that is trained using unsupervised learning to produce a low-dimensional, discretized representation of the input space of the training samples, called a map, and is therefore a method to do dimensionality reduction. The demo I made here shows how powerfull SOMs are. I used the Credit Approval Data Set from the UCI Machine learning Repository (https://archive.ics.uci.edu/ml/datasets/Credit+Approval). 

The dataset includes 16 columns: the first one is the customer ID and the last one the class (approved, non approve). The total number of observation is 690. The pie chart below shows that the two classes are fairly balanced.

![alt text]()

To create SOMs I utilized the MiniSom class from the Minisom package (https://github.com/JustGlowing/minisom)
I created a SOM with 100 nodes and one with 81 nodes. The latter has less empty nodes and thus better fit the dataset I have. Finally to better display the datapoints on the plot I introduced some jitter to the (x,y) coordinate values.  

![img1](https://github.com/Gianl-msi/Self-Organizing-Maps/blob/main/Images/som100.png)
![img2](https://github.com/Gianl-msi/Self-Organizing-Maps/blob/main/Images/som81.png)
![img3](https://github.com/Gianl-msi/Self-Organizing-Maps/blob/main/Images/som81_plus_jitter.png)

The addition of some jittering to the value of the x,y coordinates allows a better understanding of how the samples are distributed.
There are three clear clusters:
 - Top left cluster: mostly green squares
 - The cluster localized on the diagonal: mostly red cyrcles
 - Bottom right cluster:  mostly green squares
 
There two nodes whose mean interneuron distance (MID) is almost one (4,8 and 7,7): these contain several outliers. 
