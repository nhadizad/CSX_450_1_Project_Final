# Abalone #

## Domain ##
The problem is drawn from the analysis of data when studying the physical characteristic of abalones as it relates to their age.

## Problem Statement ##
The age of abalone is determined by cutting the shell through the cone, staining it, and counting the number of rings through a microscope, a time consuming process. In order to simplify the proces, we will create a supervised classification model to predict the age range of abalones, using their physical characteristics.

## Dataset ##
The abalone dataset contains measurements for 4177 with 8 features, and the number of rings.


As each element will be stored in an R, the size of the dataframe will be approximately 284036 bytes (4177 rows * 4 columns * 8 bytes + 4177 rows * 1 column * 4 bytes) plus any overhead associated with the dataframe. With an overhead of 5% for this relatively large dataset, the total in-memory size of this dataframe is approximately 290000 bytes.

Number of Attributes: 8 numeric, predictive attributes and the number of rings (directly related to age).


|Name           |Data Type     |Meas.  |Description|
|---------------|--------------|-------|-----------|
|Sex|nominal||M, F, and I (infant)|
|Length|continuous|mm|Longest shell measurement|
|Diameter|continuous|mm|perpendicular to length|
|Height|continuous|mm|with meat in shell|
|Whole weight|continuous|grams|whole abalone|
|Shucked weight|continuous|grams|weight of meat|
|Viscera weight|continuous|grams|gut weight (after bleeding)|
|Shell weight|continuous|grams|after being dried|
|Rings|integer||+1.5 gives the age in years|

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
