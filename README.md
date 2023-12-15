## Welcome to my WeatherDataProject
This is from my project from Scripting for Large Databases. It consisted of curating precipitation data from NOAA for two cities: Harrisburg, Pa and Castle Rock, CO. This data focuses specifically on snow fall and comparing how much snowfall these two cities receive with particular attention being paid to whether the year had an El Niño or La Niña in effect.
### Formatting
This is a dataset consisting of three different parts that make up a whole. However, unlike the other repository data I've curated, this data could be used individually. You can use this data by itself for other purposes, but know that the purpose of this data may be limited due to the fact that I was focused on snowfall/winter precipitation.
### How to Use or Manipulate this Data
I created a simple csv file using Excel. In the project I was working on, I used Google colab to manipulate the data, but you should be able to use whatever program can read csv file. Here is an example of some of the manipulations I did to the data. Please note that the data is pulled individually and then manipulated:
```import pandas as pd
snwfll0 = pd.read_csv('datafile.csv', index_col=0)
snwfll0 #prints out the data. this could be used for any one of the datasets that are in this repository

table1 = snwfll1.pivot_table(values=['January', 'February', 'March', 'April', 'May', 'June', ... 'December'], index=['Annual'], aggfunc='mean')
table1 #just an example of pivoting the table to see the data better

castlenoann = snwfll0.loc[:, snwfll0.columns!='Annual']
castlenoann #an example of pulling the accumulation for a specific time

castlenoann[['December','January','February','March']].std() #looking at standard deviation
```

### Reuse Potential
This data should be used for statistics regarding the amount of rainfall for the two cities. The data from El Niño and/or La Niña could be used for other projects regarding weather from 1985 to 2020. Especially, because this data is separate from the precipitation data from the two cities.
I would not use this data to determine any climate change evidence for these two cities in regards to rainfall/snowfall. There needs to be more factors than simply just precipitation.
