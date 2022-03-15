# ThicknessMap
This module is an extention for 3D Slicer.  
It was implemented to generate Thickness Maps of segments obtained from MRI-CT data.

# Usage at 3dSlicer
1) Install ThicknessMap extention by using the Extension Wizard or Manuel
2) Load a MRI or CT data to 3D Slicer (you can use Sample Data extension)
3) Open ThicknessMap extention and select a 3D input volume
4) Set a threshold value to get a segment from the 3D volume and click Apply Segmentation button. You can repeat this process until you find the most suitable threshold value
7) Click the Apply Thickness button to generate Thickness Map model of the segment

# Algorithm [1]
1) Export Label-Map and Model from the segmentation
2) A medial surface from the label-map is created by using the BinaryThinningImageFilter
3) A distance map from the medial surface is created by using the DanielssonDistanceMapImageFilter (Binary=Yes and ImageSpacing=Yes)
4) A thickness model with the distance map is generated by using the Probe Volume with Model.

[1] Fluvio Lobo, Most Efficient Way of Creating a Thickness Map, Link: https://discourse.slicer.org/t/most-efficient-way-of-creating-a-thickness-map/18203/3

# Example 
![image](https://user-images.githubusercontent.com/22032994/158266336-d6c9699a-8e6a-4e71-84f7-226c1b63aa5e.png)
