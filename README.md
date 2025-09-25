Using two 3D MRI brain images, the goal was to make a comparison and understand the neuroscientific impacts of experiments on quails . Later, the program was constrained to return the similarities detected on both images.

As part of our project, we process images in batches because they contain a large amount of data. The 3D brain images are processed one at a time, meaning they are divided into 2D sub-images that are processed one after the other. Following this process, the 2D images are stacked again along the axis in which they were cut. We can choose to cut them along the x, y, or z axes.
First, we calculate the difference between the pixels with the maximum and minimum intensity in the image. If the difference exceeds the predetermined threshold, the image is deemed non-homogeneous. A square image is now divided into 4 squares. The process is repeated for each square. In the opposite case, the segmentation step is complete. This step is called the "split".
When the split is made, the borders between the squares that touch each other are subjected to the homogeneity test. The goal is to group the squares that belong to the same region. This step of the project is called "merge".

Next step : find the best solutions to store the data from the brains to compare them at the end.

Solution chosen : 
modeling graphs looking exactly like the brains of animals with nodes placed at the center of gravity of each regions and the arcs made between nodes that belong to regions that are neighbors.
Through modeling that closely resembles the appearance of a brain, we are able to compare two brains and extract similarities between them.

Results : 
2 methods chosen and one implemented to exploit the data and have a result: 

1.	We used a computer measurement unit called graph edit distance (GED) that helps quantify the dissimilarity between our two graphs. This is based on the minimum number of operations we can perform to transform one graph into another. These operations can be the insertion, deletion, or substitution of nodes and edges. The first allows the addition of a node or edge, the second allows the removal of them. The last step is to modify them so that they correspond to another node or edge in the graph.


2.  Making histograms that represent the difference of regions' volumes on each brain : the one subjected to experiments and the other one. 

At the end, we had the possibility to see the impacts of experiments on the brains and give this part to the doctorant to complete his project on researches in neurosciences thank's to AI.
