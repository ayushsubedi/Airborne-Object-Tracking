### AIRBORNE OBJECT TRACKING DATASET (AOT) DESCRIPTION

The Airborne Object Tracking (AOT) dataset is a collection of flight sequences collected onboard aerial vehicles with high-resolution cameras. To generate those sequences, two aircraft are equipped with sensors and fly *planned* encounters (e.g., Helicopter1 in Figure 1(a)). The trajectories are designed to create a wide distribution of distances, closing velocities, and approach angles. In addition to the so-called *planned* aircraft, AOT also contains other *unplanned* airborne objects, which may be present in the sequences (e.g., Airborne1 in Figure 1(a)). Those objects are also labeled but their distance information is not available. Airborne objects usually appear quite small at the distances which are relevant for early detection: 0.01% of the image size on average, down to a few pixels in area (compared to common object detection datasets, which exhibit objects covering more considerable portion of the image). This makes AOT a new and challenging dataset for the detection and tracking of potential aerial approaching objects. 

![](https://images.aicrowd.com/uploads/ckeditor/pictures/356/image.png)

*Figure 1: Overview of the Airborne Object Tracking (AOT) dataset, more details in the "Data Diversity" section*

In total, AOT includes close to 164 hours of flight data:

-   4,943 flight sequences of around 120 seconds each, collected at 10 Hz in diverse conditions. Each sequence typically includes at most one planned encounter, although some may include more.
-   5.9M+ images
-   3.3M+ 2D annotation

![](https://images.aicrowd.com/uploads/ckeditor/pictures/400/493d98aa-b7e5-45f8-aed1-640e4768f647_video.gif)

*Video 1: Flight sequence of the drone, with other airborne objects annotated*

* * * * *

### DATASET DIVERSITY

A unique feature of AOT compared to comparable existing datasets is the wide spectrum of challenging conditions it covers for the detection and tracking of airborne objects.

![](https://images.aicrowd.com/uploads/ckeditor/pictures/348/image.png)

*Figure 2: Samples images showcasing the diversity in AOT dataset*

-   Airborne object size: often a direct proxy to a distance to the object, the area of objects in the dataset varies from 4 to 1000 pixels, as illustrated in Fig. 1 (b). Note that the ground truth for tiny and small objects cannot be marked perfectly tight, instead it is approximated with circles of radius 3 and 8 pixels respectively, which yield two bright horizontal lines in the Fig. 1 (b).
-   Planned encounters:
    -   Distance to the object: concentrated between 600 to 2,000 meters (25-75 percentiles)
    -   Closing velocity (the velocity with which the object approaches the camera): up to 70 meters per second
    -   Angle of approach:
        -   Azimuth: from -60 to 60 degrees
        -   Elevation: from -45 to 45 degrees
    -   Collision risk: out of the planned encounters, it is estimated that 55% of them would qualify as potential collision trajectories and close encounters
-   Camera roll angle: related to camera trajectory, the bank angle goes up to 60 degrees in high bank turns
-   Altitude: the altitude of the camera varies from 24 to 1,600 meters above mean sea level (MSL) with most captures between 260 and 376 meters MSL. The captures are as low as 150 meters above ground, which is challenging to capture.
-   Distance to visual horizon: 80% of targets are above the horizon, 1% on the horizon, and 19% below. This feature particularly affects the amount of clutter in the background of the object.
-   Airborne object type: see Figure 1 (d) and Table 1 below
-   Sky conditions and visibility: sequences with clear, partly cloudy, cloudy, and overcast skies are provided, 69% of the sequences have good visibility, 26% have medium visibility, and 5% exhibit poor visibility conditions.
-   Light conditions:
    -   Back-lit aircraft, sun flare, or overexposure are present in 5% of the sequences
    -   Time of the day: data was captured only during well lit daylight operations but a different times of the day, creating different sun angle conditions
    -   Terrain: flat horizon, hilly terrain, mountainous terrain, shorelines


 |
