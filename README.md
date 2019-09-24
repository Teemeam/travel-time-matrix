# Travel Time Matrix  
A guide to create travel time matrices using the Digitransit Routing API and the HERE Route API.  
  
![Lahti travel time matrix](img/lahti-travel-time-matrix.jpg)  
  
This is Lahti region and Lahti's four shopping centres. An example of how to read the matrix: When using public transport, Karisma is the closest shopping centre anywhere in the red area.  
## Table of Contents  
1. [Used technologies](#used-technologies)  
2. [Preparations](#preparations)  
3. [Digitransit Routing API](#digitransit-routing-api)  
3. [HERE Route API](#here-route-api)  
4. [Color the matix](#color-the-matrix)  
## Used technologies:  
* QGIS3.8  
* Python 3.7  
## Preparations  
Our first mission is to create a list of origin coordinates and target coordinates. In the example above, the origin coordinates are the coordinates of the shopping centers and the target coordinates are the centroids of the rectangles.  
  
We start by opening QGIS and choosing the area we like to focus on. You may use the OpenStreetMap from XYZ Tiles as a help. Borders of the window will be the borders of our matrix. Create a grid using the Create grid tool from the Processing Toolbox. 

Set Grid type to Rectangle (polygon) and Grid extent to Use Canvas Extent. Grid CRS has to be EPSG:4326 - WGS 84 to work. Lastly, set the spacing (in degrees) to for example 0,008. The smaller the number the more time consuming it will be to create the matrix.  

![Create Grid](img/create-grid.gif) 

Select the grid you just created. From Vector -> Geometry Tools -> Add Geometry Attributes add the geometry attributes to the layer. Here it's wise to save the grid layer as GeoJSON to a folder where you can find it later.  

Show centroids of the grid by choosing Vector -> Geometry Tools -> Centroids. Add geometry attributes to the newly added points as well. Save the centroids layer as GeoJSON for further use.  
  
Lastly, export centroids layer as csv. You need the index column and the coordinate columns. The file should look like this:  
  
| Id  | longitude | latitude |
| --- | --- | --- |
| 1  | 25,52843866  | 61,02111019  |
| 2  | 25,52843866  | 61,01511019  |
| 3  | 25,52843866  | 61,00911019  |
| 4  | 25,52843866  | 61,00311019  |
| 5  | 25,52843866  | 60,99711019  |  

## Digitransit Routing API
Once you have 
## HERE Route API  
Text  
## Color the matrix 