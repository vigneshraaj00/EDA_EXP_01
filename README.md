# Experiment 1: EDA in IPL Dataset

**Aim:**

To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.


**Algorithm / Procedure:**

**1.Import Libraries**

  Import pandas for data handling.
  
  Import matplotlib and seaborn for visualization.
  
**2.Load Dataset**

  Use pd.read_csv() to load the IPL matches dataset.

  Check dataset shape using .shape.
  
  View first 5 rows using .head().

**3.Matches per Season (Univariate Analysis)**

  Group data by season and count matches.
  
  Plot a bar chart to visualize growth/decline in matches.

**4.Top Winning Teams (Univariate Analysis)**

  Use value_counts() on the winner column.
  
  Plot top 5 winning teams in a bar chart.

**5.Toss Decisions (Univariate Analysis)**

  Count toss decision preferences (bat vs field).
  
  Plot results using a bar chart.

**6.Top Venues (Univariate Analysis)**

  Count matches per venue.
  
  Display top 5 venues with a horizontal bar chart.

**7.Draw Insights**

  Observe patterns in toss decisions.
  
  Identify teams with consistent winning trends.
  
  **Program and Output**
  ```
# Step 1: Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Step 2: Load the dataset
matches = pd.read_csv("matches.csv")

# Step 3: Basic info about dataset
print("Dataset Shape:", matches.shape)    # total rows & columns
print(matches.head())                     # first 5 rows

```

<img width="595" height="583" alt="image" src="https://github.com/user-attachments/assets/6eadf018-aef9-47bf-8dca-fa758472e641" />

```
# Step 4: Number of matches per season
season_counts = matches['season'].value_counts().sort_index()
print("\nMatches per season:\n", season_counts)

# Plot matches per season
plt.figure(figsize=(8,4))
sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
plt.title("Number of Matches per Season")
plt.xlabel("Season")
plt.ylabel("Matches")
plt.show()
```
<img width="1072" height="707" alt="image" src="https://github.com/user-attachments/assets/b321a560-aa62-4d8f-94e2-85290e4f5501" />

```
# Step 5: Most successful teams
team_wins = matches['winner'].value_counts()
print("\nTop Winning Teams:\n", team_wins.head(5))

plt.figure(figsize=(8,4))
sns.barplot(x=team_wins.head(5).index, y=team_wins.head(5).values, palette="magma")
plt.title("Top 5 Winning Teams")
plt.xlabel("Team")
plt.ylabel("Wins")
plt.show()

```
<img width="1199" height="586" alt="image" src="https://github.com/user-attachments/assets/0bd5b799-14fa-4442-a22c-32999f7dc66d" />


```
# Step 6: Toss decisions (bat vs field)
toss_decision = matches['toss_decision'].value_counts()
print("\nToss Decisions:\n", toss_decision)

plt.figure(figsize=(6,4))
sns.barplot(x=toss_decision.index, y=toss_decision.values, palette="Set2")
plt.title("Toss Decisions (Bat or Field)")
plt.show()
```
<img width="1285" height="585" alt="image" src="https://github.com/user-attachments/assets/3398b531-218b-4983-8e44-bf7a67311cff" />


```
# Step 7: Venues hosting most matches
venue_counts = matches['venue'].value_counts().head(5)
print("\nTop Venues:\n", venue_counts)

plt.figure(figsize=(8,4))
sns.barplot(y=venue_counts.index, x=venue_counts.values, palette="coolwarm")
plt.title("Top 5 Venues by Matches Hosted")
plt.xlabel("Matches Hosted")
plt.ylabel("Venue")
plt.show()
```

<img width="1334" height="635" alt="image" src="https://github.com/user-attachments/assets/59b2a202-a297-46df-b9dc-677b2740364e" />




 **Result**
 
  This experiment is executed successfully
# Experiment 1: EDA in IPL Dataset

**Aim:**

To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.


**Algorithm / Procedure:**

**1.Import Libraries**

  Import pandas for data handling.
  
  Import matplotlib and seaborn for visualization.
  
**2.Load Dataset**

  Use pd.read_csv() to load the IPL matches dataset.

  Check dataset shape using .shape.
  
  View first 5 rows using .head().

**3.Matches per Season (Univariate Analysis)**

  Group data by season and count matches.
  
  Plot a bar chart to visualize growth/decline in matches.

**4.Top Winning Teams (Univariate Analysis)**

  Use value_counts() on the winner column.
  
  Plot top 5 winning teams in a bar chart.

**5.Toss Decisions (Univariate Analysis)**

  Count toss decision preferences (bat vs field).
  
  Plot results using a bar chart.

**6.Top Venues (Univariate Analysis)**

  Count matches per venue.
  
  Display top 5 venues with a horizontal bar chart.

**7.Draw Insights**

  Observe patterns in toss decisions.
  
  Identify teams with consistent winning trends.
  
  **Program and Output**
  ```
# Step 1: Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Step 2: Load the dataset
matches = pd.read_csv("matches.csv")

# Step 3: Basic info about dataset
print("Dataset Shape:", matches.shape)    # total rows & columns
print(matches.head())                     # first 5 rows

```

<img width="595" height="583" alt="image" src="https://github.com/user-attachments/assets/6eadf018-aef9-47bf-8dca-fa758472e641" />

```
# Step 4: Number of matches per season
season_counts = matches['season'].value_counts().sort_index()
print("\nMatches per season:\n", season_counts)

# Plot matches per season
plt.figure(figsize=(8,4))
sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
plt.title("Number of Matches per Season")
plt.xlabel("Season")
plt.ylabel("Matches")
plt.show()
```
<img width="1072" height="707" alt="image" src="https://github.com/user-attachments/assets/b321a560-aa62-4d8f-94e2-85290e4f5501" />

```
# Step 5: Most successful teams
team_wins = matches['winner'].value_counts()
print("\nTop Winning Teams:\n", team_wins.head(5))

plt.figure(figsize=(8,4))
sns.barplot(x=team_wins.head(5).index, y=team_wins.head(5).values, palette="magma")
plt.title("Top 5 Winning Teams")
plt.xlabel("Team")
plt.ylabel("Wins")
plt.show()

```
<img width="1199" height="586" alt="image" src="https://github.com/user-attachments/assets/0bd5b799-14fa-4442-a22c-32999f7dc66d" />


```
# Step 6: Toss decisions (bat vs field)
toss_decision = matches['toss_decision'].value_counts()
print("\nToss Decisions:\n", toss_decision)

plt.figure(figsize=(6,4))
sns.barplot(x=toss_decision.index, y=toss_decision.values, palette="Set2")
plt.title("Toss Decisions (Bat or Field)")
plt.show()
```
<img width="1285" height="585" alt="image" src="https://github.com/user-attachments/assets/3398b531-218b-4983-8e44-bf7a67311cff" />


```
# Step 7: Venues hosting most matches
venue_counts = matches['venue'].value_counts().head(5)
print("\nTop Venues:\n", venue_counts)

plt.figure(figsize=(8,4))
sns.barplot(y=venue_counts.index, x=venue_counts.values, palette="coolwarm")
plt.title("Top 5 Venues by Matches Hosted")
plt.xlabel("Matches Hosted")
plt.ylabel("Venue")
plt.show()
```

<img width="1334" height="635" alt="image" src="https://github.com/user-attachments/assets/59b2a202-a297-46df-b9dc-677b2740364e" />




 **Result**
 
  This experiment is executed successfully
