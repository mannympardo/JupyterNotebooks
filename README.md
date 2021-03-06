# JupyterNotebooks

This Jupyter Notebook written in Python utilizes the Haversine calculation (since we know the earth is round) to calculate the distance between a request from the DataSample.csv and coordinate pairs from the POILIst.csv files. We then take this calculation to perform analysis such as proximity density, average distance, and the standard deviation. 

Haversine returns a distance in this case in Kilometers which can be adjusted to Miles if necessary, by interchanging the constants. (km = 6371, miles = 3959)

https://en.wikipedia.org/wiki/Haversine_formula

Included are the sample input data files which can also be gotten here https://github.com/EQWorks/ws-data-spark along with a sample of the output which is reflected in the Jupyter output.

A. Cleanup
  We start by removing any duplications of the two coordinate pairs from the DataSample.csv file. 

B. Label
  Assign each request (from data/DataSample.csv) to the closest (i.e. minimum distance) POI (from data/POIList.csv).

Note: a POI is a geographical Point of Interest.
C. Analysis
 For each POI, calculate the average and standard deviation of the distance between the POI to each of its assigned requests.
 At each POI, draw a circle (with the center at the POI) that includes all of its assigned requests. Calculate the radius and density (requests/area) for each POI.

Note
While a dynamic and scalable DataSample.csv is supported; at the time of this release the POIList.csv file is limited to 4 entries.
