# Travel Time Matrix  
A guide to create travel time matrices using the Digitransit Routing API and the HERE Route API.  
### Used technologies:  
* QGIS3.8  
* Python 3.7  

![Lahti travel time matrix](img/lahti-travel-time-matrix.jpg)  
  
## Preparations  
We start by opening QGIS and choosing the area we like to focus on. You may use the OpenStreetMap from XYZ Tiles as a help. Borders of the window will be the borders of our matrix. Create a grid using the Create grid tool from the Processing Toolbox.  
Set Grid type to Rectangle (polygon) and Grid extent to Use Canvas Extent. Grid CRS has to be EPSG:4326 - WGS 84 to work. Lastly, set the spacing (in degrees) to for example 0,008. The smaller the number the more time consuming it will be to create the matrix.  
![Create Grid](img/create-grid.png)  
Select the grid you just created. From Vector -> Geometry Tools -> Add Geometry Attributes add the geometry attributes to the layer. Here it's wise to save the grid layer as GeoJSON to a folder where you can find it later.  
Show centroids of the grid by choosing Vector -> Geometry Tools -> Centroids. Add geometry attributes to the newly added points as well. Save the centroids layer as GeoJSON for further use. Lastly, export centroids layer as csv. You need the index column and the coordinate columns.  
## Get the data  
Once you have 
## Color the matrix  