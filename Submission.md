# Accident and break-down prediction for Reading Buses

## Inspiration
We were impressed with the approach of Reading Buses to make their data open and available. 
We wanted to use their data to show that open data creates win-win situations between the public sector, 
the private sector, and civil society. It was our ambition to create a real, value-adding product for 
Reading Buses using ECMWF data. 

## What it does
Our model predicts probability of accidents for buses on bus lines in response to weather conditions

## How we built it
We used data on bus collisions from 2001 to 2016 and ECMWF data from MARS extracted via the python API. 
We started off with exploratory data analysis in R and plotly (included as html).
Models were built in R using generalised linear models with lasso and ridge regression, 
cross-validation for hold-out test and validation datasets, and plots.

## Challenges we ran into
Cleaning the bus data was challenging, and it would have been nice to get the MARS data directly into R.
However, the python API did a great job in the end! Perhaps we should come back to the dataset and write an
R package implementation of the Web API library?

## Accomplishments that we're proud of
Built a model with an out-of-sample AUC of 0.76! AUC is a measure of predictive accuracy, 
with 0.5 being random and 1 being a perfect prediction. 0.76 indicates a pretty decent result for a real-world, 
large-scale dataset like this. Quite a bit better than we had initially anticipated! 

## Team name & members
Predicting Accidents for Reading Buses

* Fiona Grimson - Fiona.grimson@gmail.com
* Rajesh Sydlon - rajesh.sydlon@gmail.com
* Laura Castrillo - Castrillo@gmail.com
* Mo - mtarky@outlook.com
* Gordon Rates - wegiangb@hotmail.co.uk
* Laurens Geffert - laurensgeffert@gmail.com

## Lessons learnt
We learned how to extract MARS data via the python API, and how to deal with NetCDF format data in R.
If we could start all over again we would force John to stay with us the weekend ;)
More of his domain expertise on the could have benefited a lot!

## Future developments
We are pretty confident that Reading Buses will be interested in using our model. 
We are handing over code and model, and hope that there will be opportunities to build on this work in the future! 
Other data can be included to improve the model, such as bus operations, special events in Reading, and time of the day.

**Additional Data sets...**
- More weather data, perhaps of high spatial resolution
- Including events like Reading Festival in the model
- More bus operations data and passenger surveys

**Expand predictive analytics within Reading Buses...**
- Scheduling engineers 
- Optimising customer experience ( information about delays )

**Write an R package for accessing ECMWF data? (rOpenSci)**
