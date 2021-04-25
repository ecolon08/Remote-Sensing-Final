# ECE471 Topics in Machine Learning: Remote Sensing

The Cooper Union
Spring 2021

Glacier extent change over time

**Proposal outline/questions**
- What problem is your group trying to solve? Why does it matter? 
- Good responses will be specific rather than general 
- Specify both spatial and temporal constraints if applicable
- How does your group plan to tackle the problem?
 
The effects of climate change are very pervasive today. These effects range from increased global temperatures, rising sea levels, sea ice melt, and glacier shrinkage, to name a few. Our project will study shrinking glaciers in a specific region to assess the impact of climate change using remote sensing techniques. 

When glaciers melt, sea levels rise and water resources for local communities and fauna are threatened. Our project will analyze glacier surface extent change over the last decade and correlate the results with surface temperature data.Our deliverable will include both a quantitative and qualitative assessment. For the quantitative assessment, we will compute glacier area change over time in relation to our baseline. For the qualitative assessment, we will generate image stacks that outline the change over time and stitch them in a timelapse video.

In the glaciology literature, two common metrics used to assess glacier shrinkage or melting are surface area change and surface velocity field patterns. We will use the Global Land Ice Measurements from Space (GLIMS) dataset and the Randolph Glacier Inventory (RGI) to select a polygonal area of interest and use it as a baseline to assess glacier change over time. We will also incorporate optical sensor data from Sentinel 1 or 2 to aid both the quantitative analysis and the visual/qualitative analysis. Landsat optical data is another possible dataset depending on the time span chosen (Sentinel only dates back to 2015). 
 
To assess glacier area change, we plan to implement classification algorithms to segment the glacier pixels (ice or snow) and segregate these from off-glacier pixels. Common techniques to study ice and snow cover are based on red - SWIR band ratios as described in [1]. This band ratio could be a starting point for our segmentation algorithm. SAR data from Sentinel 1 has also been used in [3] to monitor glacier change velocity fields.


**What datasets will you use?**
	
Our objective is to assess glacier change for a particular geographical region or even a single glacier from 2015 to 2021. We will start with the Sentinel datasets dating back to 2015. If we determine we need more data prior to 2015, we will augment or pivot to use Landsat optical data. For the surface temperature correlation analysis, we plan on using ERA5 data from the GEE catalog. Lastly, as stated above, we will use GLIMS and/or RGI to establish a glacier extent baseline.

**What algorithms will you implement / adapt?**
**What’s going to be challenging? What are the unknowns?**

One of the biggest challenges we will face is data availability. Depending on the geographical region or glacier we study, we may not get enough data due to cloud coverage. For instance, some parts of the Patagonia region in Chile are notoriously cloudy [1]. Sentinel 2 has a 5-day revisit time, which is another motivation for using this dataset. In contrast, the Landsat satellites have a 16-day revisit time. We are considering two potential geographical regions to assess as outlined below. Our objective is to select one glacier or extent within one of these regions as we start to study the datasets. 
Potential regions: 
Northern Patagonia region in Chile
Alaska

**What does the final deliverable of your project look like?
What output will your code produce?
What analysis will you perform?**
Quantitative assessment: glacier area change over time 
Qualitative assessment: glacier area composites over time (timelapse)
Correlation between glacier area change and surface temperature

References

[1] S. H. Winsvold, A. Kääb and C. Nuth, "Regional Glacier Mapping Using Optical Satellite Data Time Series," in IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing, vol. 9, no. 8, pp. 3698-3711, Aug. 2016, doi: 10.1109/JSTARS.2016.2527063.

URL: https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7422705

[2] Di Tullio, Marco & Nocchi, F. & Camplani, A. & Emanuelli, N. & Nascetti, Andrea & Crespi, Mattia, “Copernicus Big Data And Google Earth Engine For Glacier Surface Velocity Field Monitoring: Feasibility Demonstration On San Rafael And San Quintin Glaciers”. ISPRS - International Archives of the Photogrammetry, Remote Sensing and Spatial Information Sciences (2018). XLII-3. 289-294. 

URL: https://www.int-arch-photogramm-remote-sens-spatial-inf-sci.net/XLII-3/289/2018/isprs-archives-XLII-3-289-2018.pdf


[3] Millan, Romain. Mapping Surface Flow Velocity of Glaciers at Regional Scale Using a Multiple Sensors Approach. Remote Sensing (2019).  11. 10.3390/rs11212498. 

URL: https://www.researchgate.net/publication/336810374_Mapping_Surface_Flow_Velocity_of_Glaciers_at_Regional_Scale_Using_a_Multiple_Sensors_Approach

[4] GLIMS: Global Land Ice Measurements from Space - GEE
URL: https://developers.google.com/earth-engine/datasets/catalog/GLIMS_current
