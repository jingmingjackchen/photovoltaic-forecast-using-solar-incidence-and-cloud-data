# Photovoltaic Forecast Using Solar Incidence and Cloud Data

A simple program to estimate the hourly forecasted efficiency of solar panels using clouds data sourced from free API.

## Requirements:

- Written and tested on Python 3.12.3
- Tested in a conda environment with dependecies listed in [requirements.txt](requirements.txt).

## Input/output:

- Inputs:
  - Latitude and longitude of the location to generate forecast.
  - Tilt (from horizontal) and azimuth angle (from north) of the solar panel.
  - (Optional) Hour offset and time step size of the forecast.
- Output:
  - Forecasted efficiency percentage as a decimal.

## How to run this program:

1. Create a conda environment:
   `conda create --name <my-env>`
2. Install the dependecies listed in [requirements.txt](requirements.txt):
   `conda install requirements.txt`
3. Obtain API key from [Meteoblue](https://www.meteoblue.com/weather-api).
4. Create a `.env` file in the root directory and enter the API key into the file:
   `METEOBLUE_API_KEY=<API key>`
5. Update the `LONG` and `LAT` variables in [weatherAPI.ipynb](weatherAPI.ipynb) to the desired coordinates.
6. Update the `LONG`, `LAT`, `self.tilt_angle`, and `self.azimuth_angle` in [model.ipynb](model.ipynb) to the same coordinates.
7. Run every cell in [weatherAPI.ipynb](weatherAPI.ipynb), then run every cell in [model.ipynb](model.ipynb). Adjust the arguments passed into `calculate_power_efficiency_forecast` if necessary.

## Credits:

- A. Zeh, C. Hainzinger and R. Witzmann, "Generation and evaluation of photovoltaic forecasts based on freely available weather data," _2016 IEEE/PES Transmission and Distribution Conference and Exposition (T&D)_, Dallas, TX, USA, 2016, pp. 1-5, [doi: 10.1109/TDC.2016.7520042](https://ieeexplore.ieee.org/document/7520042).
- Herrería-Alonso S, Suárez-González A, Rodríguez-Pérez M, Rodríguez-Rubio RF, López-García C. A Solar Altitude Angle Model for Efficient Solar Energy Predictions. _Sensors_. 2020; 20(5):1391. https://doi.org/10.3390/s20051391
