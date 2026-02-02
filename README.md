### Name : NARESH
### Reg.No: 212223240104

## Experiment 1: EDA in IPL Dataset
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

## 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
  
## 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
  
## 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
  
## 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
  
## 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
  
## 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
  
## 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  
  ## Program
  ## 1.Dataset Structure  ( find the uploaded dataset matches.csv)
  How many rows and columns are present in the dataset?
  
  What does the first 5 rows of data look like?
  ```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
df=pd.read_csv('matches.csv')
df.head()


df.shape

 ```

  ## Output
  <img width="233" height="47" alt="image" src="https://github.com/user-attachments/assets/e59ee265-8f15-4138-bd6f-1305dfdeeb38" />


## Matches per Season

How many matches were played in each IPL season?

Can we visualize the trend of matches across seasons?

```
matches_per_season = df['season'].value_counts().sort_index()
matches_per_season
import matplotlib.pyplot as plt

matches_per_season.plot(kind='bar')
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Matches Played per IPL Season")
plt.show()

```
## Output:
<<img width="638" height="566" alt="image" src="https://github.com/user-attachments/assets/90ca415c-1bb1-4844-8a5d-5effcf4a9bbb" />

## Top Winning Teams

Which teams have won the most matches overall?

Can we plot the top 5 winning teams?

```
top_teams = df['winner'].value_counts()
top_teams
top_5_teams = top_teams.head(5)

top_5_teams.plot(kind='bar',colour='green')
plt.xlabel("Team")
plt.ylabel("Matches Won")
plt.title("Top 5 Winning IPL Teams")
plt.show()



```

## Output:
<img width="639" height="729" alt="image" src="https://github.com/user-attachments/assets/badcbaa1-0135-43dd-a900-aa5155766f1d" />


## Toss Decisions

What do captains usually choose after winning the toss (bat or field)?

Can we show this preference in a bar chart?

```
toss_decision = df['toss_decision'].value_counts()
toss_decision

toss_decision.plot(kind='bar')
plt.xlabel("Toss Decision")
plt.ylabel("Count")
plt.title("Toss Decision Preference")
plt.show()
```

## Output:
<img width="643" height="548" alt="image" src="https://github.com/user-attachments/assets/da54acde-b333-4a2c-8264-a7690ddcbd3b" />



## Top Venues

Which stadiums have hosted the most matches?

Can we display the top 5 venues in a clear visual?

```
top_venues = df['venue'].value_counts()
top_venues.head(5)

top_venues.head(5).plot(kind='bar',colour='purple')
plt.xlabel("Venue")
plt.ylabel("Number of Matches")
plt.title("Top 5 IPL Venues")
plt.show()


```

## Output:

<img width="639" height="646" alt="image" src="https://github.com/user-attachments/assets/6178e7c5-1c9c-408a-a74f-ccf76cf320d8" />



 ## Result
  This experiment is executed successfully.




