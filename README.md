# Ganongan_PA-4

Dateframe
1.
``` python
import pandas as pd

#Inputs the eceboard.xlsx file into a table.
df = pd. read_excel ("eceboard.xlsx" )
df ['Average'] = df.mean (numeric_only=True, axis=1)
df
```
![image](https://github.com/user-attachments/assets/fb4fc2d1-57b4-489d-95c6-8fe94267f9d5)

``` python
#to print only specific values that the instruction is asking for
print("--Instru--")
Instru = df.loc[(df.Track=="Instrumentation") & (df.Hometown=="Luzon") & (df.Electronics>70), ['Name', 'GEAS' , 'Electronics']]
Instru
```
![image](https://github.com/user-attachments/assets/1a6abd7c-4136-4053-a6a9-79296501f037)

``` python
#to print only specific values that the instruction is asking for.
print("—-Mindy--")
Mindy = df.loc[(df.Hometown=="Mindanao") & (df.Gender=="Female") & (df.Average>=55) , ['Name', 'Track', 'Electronics', 'Average']]
Mindy
```
![image](https://github.com/user-attachments/assets/48f7982c-1cdb-4a6c-8b52-7c22af9bf068)

2.
``` python
import matplotlib.pyplot as plt

#the graph showing the chosen track's relationship to grades should be printed.
plt.figure (figsize=(5,6))
plt.bar (df ['Track'], df ['Average'])
plt.xlabel ("Chosen Track in College") 
plt.ylabel ("Average")
plt.title ("Table 1.1: A bar graph showing the relationship of chosen track in college.")
```
![image](https://github.com/user-attachments/assets/330dd6d5-8420-4170-95c4-bb640fa2ac42)

``` python
#Print the graph showing the relationship between gender and grades using this function.
plt.figure (figsize=(5,6))
plt.bar (df ['Gender'], df ['Average'])
plt.xlabel ("'Gender")
plt.ylabel ("Average")
plt.title ("Table 1.2: A bar graph showing the relationship of gender and average grade.")
```
![image](https://github.com/user-attachments/assets/b595c74b-26ed-4143-b012-044f748fcfe1)

``` python
#Prints the graph displaying the hometown-grade correlation function.
plt.figure(figsize=(5,6))
plt.bar (df['Hometown'],df ['Average'])
plt.xlabel ("Hometown" ) 
plt.ylabel ("Average")
plt.title ("Table 1.3: A bar graph showing the relationship of hometown and average grade.")
```
![image](https://github.com/user-attachments/assets/fc4628fe-1374-4089-94a0-19a1bcafbbe3)
