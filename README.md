# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("/content/Data_set1.csv")
df.tail()

```
# output
![alt text](image.png)
```
df.tail(3)
```
# output
![alt text](image-2.png)
```
df.info()
```
# output
![alt text](image-3.png)
```
df.describe()
```
# output
![alt text](image-4.png)
```
df.isnull()
```

# output
![alt text](image-6.png)
```
df.dropna(axis=1)
```
# output
![alt text](image-7.png)
```
dfs=df[df['watchers']>11111]
dfs
```
# output
![alt text](image-8.png)
```
df.iloc[[1,3,5],[1,3]]
```
# output
![alt text](image-10.png)
```
df['num_episodes'].fillna(value=df['num_episodes'].mean())
```
# output
![alt text](image-11.png)
```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df.describe()
```
# output
![alt text](image-13.png)

```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df.info()
```

# output
![alt text](image-19.png)

```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df.fillna(method='ffill')
```
# output
![alt text](image-20.png)

```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df.fillna(method='bfill')
```
# output
![alt text](image-21.png)

```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
tot=df.dropna(subset=['M1','M2','M3','M4'],how='any')
print(tot)
```
#  output
![alt text](image-22.png)
```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df.isnull()
```
# output
![alt text](image-23.png)
```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df.notnull()
```
# output
![alt text](image-24.png)
```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df['DOB']
```
# output
![alt text](image-26.png)
```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df['DOB']=pd.to_datetime(df['DOB'])
df
```
# output
![alt text](image-27.png)
```
sb.boxplot(data=df)
```
# output
![alt text](image-29.png)
```
sb.scatterplot(data=df)
```
# output
![alt text](image-30.png)
```
sb.scatterplot(data=qm)
```
# output
![alt text](image-31.png)


# Result
The data clearing has been done successfully.
