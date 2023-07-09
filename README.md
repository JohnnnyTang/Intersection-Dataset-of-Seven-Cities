# Intersection-Dataset-of-Seven-Cities
## Abstract
The identification of road intersections and their characteristics is a crucial task with various practical applications. Previous studies on intersection identification, which rely on datasets such as raster maps, satellite images, and global navigation satellite system data, have encountered challenges in terms of accuracy, characteristic identification and wide-range applicability. In this paper, we propose a novel method for precise identification of road intersections and their road-related characteristics based on the spatial constraint relationships of vector data. Our method leverages the vector-raster fusion technique to improve the accuracy of intersection identification. We further introduce hierarchical layout templates based on the spatial constraint relationships of corresponding road lines, allowing for the identification of road-related characteristics. Experimental results demonstrate that the proposed method can efficiently handle complex road networks of various cities and accurately identify road intersection locations and road-related characteristics. Comparative experiments with the widely used OSMnx tool demonstrate the superiority of our method in terms of precision, recall, and F1 score. The proposed method provides a promising solution for generating comprehensive road intersection datasets on a larger spatial scale.
![resPtAll-clipped](https://github.com/JohnnnyTang/Intersection-Dataset-of-Seven-Cities/assets/53413691/7f1951d8-974a-4ea0-a330-59bede9baa83)
![resLineAll-clipped](https://github.com/JohnnnyTang/Intersection-Dataset-of-Seven-Cities/assets/53413691/778dc4f8-8067-40bd-9cc9-52c45937b27c)
## Instruction

![image](https://github.com/JohnnnyTang/Intersection-Dataset-of-Seven-Cities/assets/53413691/e79892db-e42c-4a02-97fe-9f32d9bbee51)

This dataset contains road intersection data of seven cities (Berlin, Beijing, London, Nanjing, New York City, Rome, Shanghai) identified by our proposed method.
The data of each city are stored in the folder named by its abbreviation.
In each folder, there will be five *.shp files.

![image](https://github.com/JohnnnyTang/Intersection-Dataset-of-Seven-Cities/assets/53413691/b2b4570f-573f-456c-82e0-edad1a8b654c)

(1) Roadnetwork (roads.shp)
This layer stores the OSM road network with tag attributes.

(2) Intersection points (cross-res.shp)
This layer stores the location of the intersection point and the general characteristics of the road layout, including the number of intersecting roads and layout type. This provides the necessary location information for mapping and spatial analyses.

(3) Related road lines (fullLine-res.shp/fail-fullLine.shp)
The original road lines related to intersections extracted from the road networks were stored in this layer, preserving the inherent attributes of the original dataset. In addition, matching information, indicating whether the lines represent the same road, was stored as an attribute.

(4) Synthesized road lines (simpleLine-res.shp)
The geometries of this layer store synthesized road lines representing road orientations, whereas the attributes store acquired characteristics, including roadway configurations and match indices, which allow the synthesized road lines to be connected to the original roads from which they were derived. This connection is achieved through “pt_id” linked with cross-res.shp and “match_id” linked with fullLine-res.shp.
