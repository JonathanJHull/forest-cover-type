# Illustrative examples of Machine Learning Techniques Applied to Kaggle Forest Cover Data

A complete machine learning project pipeline is presented for the Kaggle Forest Cover Type competition.  The individual techniques are illustrative examples and can be used as the basis for further discussion.

## Files

plots/ -- png files from the Jupyter notebook for the report

proposal/ -- project proposal

submission/ -- files submitted for final evaluation

JonathanHull_capstone.ipynb -- Jupyter notebook with source code

best_gbrt_cfl.pkl -- optimized Gradient Boosting classifier

best_mlp52_19_7_clf.pkl	 -- optimized multi-layer perceptron

best_mlp_clf.pkl -- basic multi-layer perceptron

best_rf_clf.pkl	-- optimized random forest classifier

best_sgd_clf.pkl -- optimized stochastic gradient descent classifier

kaggle_test.csv	-- test data from the kaggle competition

kaggle_train.csv -- training data from the kaggle competition

submission_best_rf.csv	-- kaggle submission with results from best RF classifier

submission_majority_vote.csv -- kaggle submission with majority vote results

submission_stacked.csv -- kaggle submission with one level of stacking with logistic regression

## Installation

Copy the Jupyter notebook JonathanHull_capstone.ipynb as well as the data files in \*.csv to your python environment and open the notebook.  You can begin exceuting the cells from the top.  Everything should work seemlessly as long as you have the typical pandas, numpy, etc. installed.

This project requires Python 3.0+ and the following Python libraries:

NumPy
Pandas
matplotlib
scikit-learn

You will also need to have software installed to run and execute an iPython Notebook

We recommend you install Anaconda, a pre-packaged Python distribution that contains all of the necessary libraries and software for this project.

## Code

Python code for the project is in JonathanHull_capstone.ipynb.

## Run

## Data
### Features

The Kaggle version of the Forest Cover data set will be used.  The training set (15120 observations) contains both features and class labels (Cover_Type).  The test set contains only the features.  [https://www.kaggle.com/c/forest-cover-type-prediction/data]

The 54 features associated with each observation follow.  Besides basic geographical features, the remainder is from either the domain of forestry or geology.

1.	Elevation - Elevation in meters

2.	Aspect - Aspect in degrees azimuth

3.	Slope - Slope in degrees

4.	Horizontal_Distance_To_Hydrology - Horz Dist to nearest surface water features

5.	Vertical_Distance_To_Hydrology - Vert Dist to nearest surface water features

6.	Horizontal_Distance_To_Roadways - Horz Dist to nearest roadway

7.	Hillshade_9am (0 to 255 index) - Hillshade index at 9am, summer solstice

8.	Hillshade_Noon (0 to 255 index) - Hillshade index at noon, summer solstice

9.	Hillshade_3pm (0 to 255 index) - Hillshade index at 3pm, summer solstice

10.	Horizontal_Distance_To_Fire_Points - Horz Dist to nearest wildfire ignition points

Four different wilderness areas (binary columns):

11.	Rawah Wilderness Area

12.	Neota Wilderness Area

13.	Comanche Peak Wilderness Area

14.	Cache la Poudre Wilderness Area

40 different soil types (binary columns) and what they represent:

15.	1 Cathedral family - Rock outcrop complex, extremely stony.

16.	2 Vanet - Ratake families complex, very stony.

17.	3 Haploborolis - Rock outcrop complex, rubbly.

18.	4 Ratake family - Rock outcrop complex, rubbly.

19.	5 Vanet family - Rock outcrop complex complex, rubbly.

20.	6 Vanet - Wetmore families - Rock outcrop complex, stony.

21.	7 Gothic family.

22.	8 Supervisor - Limber families complex.

23.	9 Troutville family, very stony.

24.	10 Bullwark - Catamount families - Rock outcrop complex, rubbly.

25.	11 Bullwark - Catamount families - Rock land complex, rubbly.

26.	12 Legault family - Rock land complex, stony.

27.	13 Catamount family - Rock land - Bullwark family complex, rubbly.

28.	14 Pachic Argiborolis - Aquolis complex.

29.	15 unspecified in the USFS Soil and ELU Survey.

30.	16 Cryaquolis - Cryoborolis complex.

31.	17 Gateview family - Cryaquolis complex.

32.	18 Rogert family, very stony.

33.	19 Typic Cryaquolis - Borohemists complex.

34.	20 Typic Cryaquepts - Typic Cryaquolls complex.

35.	21 Typic Cryaquolls - Leighcan family, till substratum complex.

36.	22 Leighcan family, till substratum, extremely bouldery.

37.	23 Leighcan family, till substratum - Typic Cryaquolls complex.

38.	24 Leighcan family, extremely stony.

39.	25 Leighcan family, warm, extremely stony.

40.	26 Granile - Catamount families complex, very stony.

41.	27 Leighcan family, warm - Rock outcrop complex, extremely stony.

42.	28 Leighcan family - Rock outcrop complex, extremely stony.

43.	29 Como - Legault families complex, extremely stony.

44.	30 Como family - Rock land - Legault family complex, extremely stony.

45.	31 Leighcan - Catamount families complex, extremely stony.

46.	32 Catamount family - Rock outcrop - Leighcan family complex, extremely stony.

47.	33 Leighcan - Catamount families - Rock outcrop complex, extremely stony.

48.	34 Cryorthents - Rock land complex, extremely stony.

49.	35 Cryumbrepts - Rock outcrop - Cryaquepts complex.

50.	36 Bross family - Rock land - Cryumbrepts complex, extremely stony.

51.	37 Rock outcrop - Cryumbrepts - Cryorthents complex, extremely stony.

52.	38 Leighcan - Moran families - Cryaquolls complex, extremely stony.

53.	39 Moran family - Cryorthents - Leighcan family complex, extremely stony.

54.	40 Moran family - Cryorthents - Rock land complex, extremely stony.

### Class Label

The class label is the Cover_Type.  It can be one of the following seven different values:

class label	represents	class label	represents	class label	represents

1	Spruce/Fir	4	Cottonwood/Willow	7	Krummholz

2	Lodgepole Pine	5	Aspen		

3	Ponderosa Pine	6	Douglas Fir		


