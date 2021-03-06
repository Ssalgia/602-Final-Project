# Fatal Shootings Data Analysis from Washington Post Survey
The Washington Post's database contains records of every fatal shooting in the United States by a police officer in the line of duty since Jan. 1, 2015.

This data includes  the race of the deaths,  the different scenarios in which the shoots took place, if or not the person was armed  or faced a mental-health crisis.

The Post’s database is updated regularly as fatal shootings are reported.

In a survey conducted by Manhattan Institute colleague Eric Kaufmann, for example, eight in 10 African-Americans and about half of white Biden voters said that they thought that young black men were more likely to be shot to death by police than to die in a car accident—one of the largest mortality risks to the young and healthy. [1]Another survey, by Skeptic magazine, showed that more than a third of liberal and very liberal respondents thought that the number of unarmed blacks killed by police each year was “about 1,000” or more. About a fifth of those calling themselves “very conservative” thought the same thing. [2] Yet another survey, from a trio of academics, found that about four in 10 African-Americans reported being “very afraid” of being killed by the police, which was roughly twice the share of black respondents who reported being “very afraid” of being murdered by criminals, as well as about four times the share of whites who reported being “very afraid” of being killed by the police. [3] 
Reference - https://www.manhattan-institute.org/verbruggen-fatal-police-shootings 

So Lets find out if the shootings were racial bias or no.


## About the data

Parts of the data description have been taken from (https://github.com/washingtonpost/data-police-shootings) Readme File.

The file `fatal-police-shootings-data.csv` contains data about each fatal shooting in CSV format. The data contains approximately 7.2k rows and 17 features, out of which not all of them are used in the analysis. The file can be  https://data.world/data-society/fatal-police-shootings OR
https://github.com/washingtonpost/data-police-shootings

Each row has the following variables:

`id`: a unique identifier for each victim

 The `threat column` and the `fleeing column` are not necessarily related.
 
 `Flee column` has 3 categories -> Car, Foot and Not Fleeing. The Data Analysis answers the questions as to which of the following modes has the highest frquency amaong the victims.

`body_camera`: News reports have indicated an officer was wearing a body camera and it may have recorded some portion of the incident.

`latitude` and `longitude`: the location of the shooting expressed as coordinates, geocoded from addresses. The coordinates are rounded to 3 decimal places, meaning they have a precision of about 80-100 meters within the contiguous U.S. 


`is_geocoding_exact`: reflects the accuracy of the coordinates. `true` means that the coordinates are for the location of the shooting (within approximately 100 meters), while `false` means that coordinates are for the centroid of a larger region, such as the city or county where the shooting happened.

The other columns include 'name', 'age' , 'Gender', 'Race', 'City', 'State', 'armed', 'signs of mental illness' and a few others. 

The `Race` feature represents 
1. A -> Asian
2. B -> Black
3. H -> Hispanic
4. W -> White
5. N -> Native
6. O -> Others

For State abbreviations - https://www.scouting.org/resources/los/states/

## About the Classification Problem.

Random Forest, Logistic Regression, and Naive Bayes Classifier, can be used to predict the race of fatal police shooting victims.
