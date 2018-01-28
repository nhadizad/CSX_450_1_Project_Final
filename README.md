# Age of Abalone #

## Domain ##
The problem is drawn from the analysis of data when studying the physical characteristic of abalones as it relates to their age.

## Problem Statement ##
The age of abalone is determined by cutting the shell through the cone, staining it, and counting the number of rings through a microscope; a time consuming process. In order to simplify the process, we will create a supervised classification model to predict the age of abalones, using their physical characteristics.

## Dataset ##
The abalone dataset contains measurements for 4177 instances, with 8 features as well as the target, the number of rings.


As data elements will be stored in R, the size of the dataframe will be approximately 284036 bytes (4177 rows * 4 columns * 8 bytes + 4177 rows * 1 column * 4 bytes) plus any overhead associated with the dataframe. With an overhead of 5% for this relatively larger dataset, the total in-memory size of this dataframe is approximately 290000 bytes.

Number of Attributes: 8 predictive attributes and the target class of number of rings (directly related to age).


	Name		Data Type	Meas.	Description
	----		---------	-----	-----------
	Sex		nominal			M, F, and I (infant)
	Length		continuous	mm	Longest shell measurement
	Diameter	continuous	mm	perpendicular to length
	Height		continuous	mm	with meat in shell
	Whole weight	continuous	grams	whole abalone
	Shucked weight	continuous	grams	weight of meat
	Viscera weight	continuous	grams	gut weight (after bleeding)
	Shell weight	continuous	grams	after being dried
	Rings		integer			+1.5 gives the age in years


Missing Attribute Values: None

Class Distribution:

	Class	Examples
	-----	--------
	1	1
	2	1
	3	15
	4	57
	5	115
	6	259
	7	391
	8	568
	9	689
	10	634
	11	487
	12	267
	13	203
	14	126
	15	103
	16	67
	17	58
	18	42
	19	32
	20	26
	21	14
	22	6
	23	9
	24	2
	25	1
	26	1
	27	2
	29	1

Summary Statistics:

    Sex          Length         Diameter          Height        WholeWeigth    
    F:1307  Min.   :0.075   Min.   :0.0550   Min.   :0.0000   Min.   :0.0020  
    I:1342  1st Qu.:0.450   1st Qu.:0.3500   1st Qu.:0.1150   1st Qu.:0.4415  
    M:1528  Median :0.545   Median :0.4250   Median :0.1400   Median :0.7995  
            Mean   :0.524   Mean   :0.4079   Mean   :0.1395   Mean   :0.8287  
            3rd Qu.:0.615   3rd Qu.:0.4800   3rd Qu.:0.1650   3rd Qu.:1.1530  
            Max.   :0.815   Max.   :0.6500   Max.   :1.1300   Max.   :2.8255  
    ShuckedWeigth    VisceraWeight     ShellWeight         Rings       
    Min.   :0.0010   Min.   :0.0005   Min.   :0.0015   Min.   : 1.000  
    1st Qu.:0.1860   1st Qu.:0.0935   1st Qu.:0.1300   1st Qu.: 8.000  
    Median :0.3360   Median :0.1710   Median :0.2340   Median : 9.000  
    Mean   :0.3594   Mean   :0.1806   Mean   :0.2388   Mean   : 9.934  
    3rd Qu.:0.5020   3rd Qu.:0.2530   3rd Qu.:0.3290   3rd Qu.:11.000  
    Max.   :1.4880   Max.   :0.7600   Max.   :1.0050   Max.   :29.000



## Solution ##

We will create three classification models, that would predict the age of abalones based on their physical characteristics. We will use the most appropriate models for this analysis, as we learn more about the dataset and the techniques that are available for classification problems. As an example we can use, Linear Discriminant Analysis (LDA), K Nearest Neighbor (KNN), and Classification and Regression Trees (CART). Additionally, since this is a supervised model, we can break up our measurements into two sets. We use the first portion of the dataset for training and developing the models, and use the second portion to validate our models. We have to be careful on how we can break up the data so that the distribution of the classes are proportional. Ultimately we can see which model produces the most accurate results.

## Benchmark Model ##

A good benchmark would be to predict the class (i.e. the number of rings and ultimately the age) of an abalone, given its physical characteristic features. With further analysis, we may realize that some of these features are very closely correlated, such as lehgth and diameter, and we don't need all of these features in our models. Additionally we need to make sure that our data is clean. As an example the Min of the Height indicates that there are zero values for this feature, and we have to take the apporpriate action accordingly. One option would be to drop these zero valued measurements if the model is heavily correlated to Height.

## Performance Metric ##

We will be using the metric of 'Accuracy' to evaluate our models. This is a ratio of the number of correctly predicted instances divided by the total number of instances in the dataset multiplied by 100 to give a percentage (e.g. 98% accurate).
