## Welcome to the First Malaysian DashCam Datasets

<img src="example.png" alt="hi" class="inline"/>

## What is myDashCam Datasets
The Malaysian DashCam Datasets (myDashCam) is an initiative work that aims to analyse and understand videos recorded via DashCams. It is the first annotated malaysian DashCam dataset that is primarly collected and annotated for resreach purposes.


## The Dataset

### The Video Files

The videos can be downloaded from [here](https://drive.google.com/file/d/1yhn4ouQbQrhJqX0g1Z808AXoF0oz35PG/view?usp=sharing). There are total of 21 videos in the folder. Each of which has been annotated using video annotation tool.

### The Annotation File

[The annotation file](https://github.com/binmosa/myDashCam/blob/master/Annotation_master.csv) is in csv format. It has 6 colomns that hold the annotation data. These columns are as follows:

```
metadata_id  |     file_list    |  flags  |  temporal_coordinates  |  spatial_coordinates  |         metadata
1_RXp9R3ua   | "[""ID01.mp4""]" |    0    |      [3.677,5.646]     | [2,333,198,22.5,45]   | "{""1"":""4"",""2"":""2""}"
```

each column data is described below:

#### 1) metadata_id

The **metadata_id** field can be used as a primary key for each row that contains annotation information. 


#### 2) file_list

The **file_list** field holds the name of the video file to which the annotation information is linked. 


#### 3) flags
The **flags** field is an extra field which has no a specific purpose. It can be used for general purpose.


#### 4) temporal_coordinates	
The **temporal_coordinates** field holds the temporal annotation information. It has the following structure: [From, To] or [seconds]. For example, the temporal coordinate of [1.349 2.741] denotes a temporal segment from time 1.346 sec. to 2.741 sec. While the temporal coordinate of [4.633] denotes a still video frame at 4.633 sec. Please note that during processing, you may need to convert this timestamp into a readable format based on your case.


#### 5) spatial_coordinates
The **spatial_coordinates** field holds the spatial coordinate information. It has the following structure:[shape id (e.g rectangle), shape location (a * a), shape size (a * a)]. For example, the spatial_coordinates of [2, 10, 20, 50, 80] denotes a rectangle (shape_id=2) of size 50x80 placed at (10, 20).


#### 6) metadata
The **metadata** field holds the annotation class id with the following structure: {"class_type":"class_id"}. For example, metadata of {""1"":""3""} indicates class type with id "1" set to the class value with id "3". In this dataset, we have 3 types of classes: 1 = Activity Class, 2= Object class, 3=Time class. The activity class type has 7 class values, each of which describes below:
---------------------------------------------------------------------------
ID	**Class name**	Desciptions
---------------------------------------------------------------------------
1	**Sudden_lane_change**	A driver/rider in front changes the lane abruptly.
2	**Illegal U-turn**	A driver/rider making a U-turn while it is not allowed.
3	**Illegal crossing**	An object illegally crosses the road
4	**Dangerous over-take**	A vehicle approaching fast from the back and over-taking a vehicle dangerously
5	**Object on road**	The vehicle suddenly confronts an object on the road (including animals)
6	**Wrong lane**	The vehicle is on a lane that it is not supposed to be on (including the reverse drive)
7	**Other**	Other event such as accident, unexpected behaviour, etc.
---------------------------------------------------------------------------



