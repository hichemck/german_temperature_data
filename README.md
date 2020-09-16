# German Temperature Data Preprocessing and Applying Haversine Calcuation to Impute Missing Values

## Task
In this project I have been working with temperature data from 
European Climate Assessment & Dataset [ecad](https://www.ecad.eu/).
The data contains daily temperature measurements in all europe cities. 
I chose to extract and preprocess data for german capitals (Landeshaupstädte) for the last 20 
years. The main challenge in this project is to deal with not available measurements
and define the best imputation strategy.

## Data
Due to the huge size of the data (4,5 GB) I did not upload it in this repository.
Here is the procedure to read the data :


- Go to [ecad site](https://www.ecad.eu/)
- Go to “Daily data”
- Download predefined subsets (ASCII) 
- Pick "Daily mean temperature tg" (position 3)
Note that each station has a txt file.

## Work Breakdown

- Download and read the data
- Extract stations ids for Germany
- Clean and transform stations dataframes
- Extract station ids for state capitals (Landeshauptstädte)
- Choose best station for each capital according to measurements avialability
- Extract and clean temperature data for each capital
- Impute nok measurements for each capital (each nok measurement is imputed 
with the ok measurement from the next station. Distance is calculated accodring to
the haversine formula)
- Define additional imputation method: shifted measurement values (one week, 
one year, two years, etc.)

