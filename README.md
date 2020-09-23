# German Temperature Data Preprocessing and Applying Haversine Calcuation to Impute Missing Values

## Task
In this project I have been working with temperature data from 
European Climate Assessment & Dataset [ECAD](https://www.ecad.eu/).
The data contains daily temperature measurements in all european cities. 
I chose to extract and preprocess data for german state capitals (Landeshaupstädte) for the last 20 
years. 
The main challenge in this project is to deal with not available measurements
and define a good imputation strategy.

## Usage
Due to the huge size of the data (4,5 GB) I did not upload it in this repository.
Here is the procedure to read the data and run the notebook:


- Go to [ecad site](https://www.ecad.eu/)
- Go to “Daily data”
- Download predefined subsets (ASCII) 
- Pick "Daily mean temperature tg" (position 3)
- Save the the files in a folder names 'data' on the same level as the notebook file 'temperature_data_preprocessing'.
Note that each station has a txt file.
- Download the notebook 'temperature_data_preprocessing' and run it

## Work Breakdown

- Download and read the data
- Extract stations ids for Germany
- Clean and transform stations dataframes
- Extract station ids for state capitals (Landeshauptstädte)
- Choose best station for each capital according to measurements avialability
- Extract and clean temperature data for each capital
- Define a function that calculates the distance between two stations according to the [Haversine Formula](https://en.wikipedia.org/wiki/Haversine_formula)
- Impute nok measurements for each capital applying haversine distance calculation (each nok measurement is imputed 
with the ok measurement from the next station)
- Define additional imputation method: shifted measurement values (one week, 
one year, two years, etc.)

