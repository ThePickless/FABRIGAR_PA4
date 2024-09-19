# EXPERIMENT 4 - DATA WRANGLING AND DATA VISUALIZATION

Repository #4 shows Python script designed to solve various problems in Advanced Programming. For this repository, it is specified to organizing data. Below is a summary of each script. 

### Problem 1

##### This specific problem set requires you to access pandas from the library and loading a ".csv" file into your notebook and clean and organize the given data using the follwing functions: 

**Function:**

``` python
import pandas as pd
#Input of the board2.xlsx file
df = pd. read_excel ("board2.xlsx" )
df ['Average'] = df.mean (numeric_only=True, axis=1)
df
```

**Output:**


![image](https://github.com/user-attachments/assets/f2f2044c-9cc6-4c36-97a8-c1f4d3964b9e)
![image](https://github.com/user-attachments/assets/582def43-4b74-4c20-be44-a7834fe5bc7b)

**Function:**

``` python
#Function to print the instruction asked.
print("--Instru--")
Instru = df.loc[(df.Track=="Instrumentation") & (df.Hometown=="Luzon") & (df.Electronics>70), ['Name', 'GEAS' , 'Electronics']]
Instru
```

**Output:**

![image](https://github.com/user-attachments/assets/2927b106-a886-47ba-a2cb-ad0703cc5967)

**Function:**

``` python
#Function to print the instruction asked.
print("—-Mindy--")
Mindy = df.loc[(df.Hometown=="Mindanao") & (df.Gender=="Female") & (df.Average>=55) , ['Name', 'Track', 'Electronics', 'Average']]
Mindy
```

**Output:**

![image](https://github.com/user-attachments/assets/2f3a0d10-e573-445b-93d4-f21f617ffca9)


### Problem 2

##### This specific problem set requires you to show different features and specific questions in the problem:

**Function:**

``` python
import matplotlib.pyplot as plt

#Function to print the graph that states the correlation of chosen track to grades.
plt.figure (figsize=(5,6))
plt.bar (df ['Track'], df ['Average'])
plt.xlabel ("Chosen Track in College") 
plt.ylabel ("Average")
plt.title ("Table 1.1: A bar graph showing the relationship of chosen track in college .")
```

**Output:**


![image](https://github.com/user-attachments/assets/349120d0-4876-492b-8af7-8ba9bcdd01cd)

**Function:**

``` python
#Function to print the graph that states the correlation of gender to grades.
plt.figure (figsize=(5,6))
plt.bar (df ['Gender'], df ['Average'])
plt.xlabel ("'Gender")
plt.ylabel ("Average")
plt.title ("Table 1.2: A bar graph showing the relationship of gender and average grade.")
```

**Output:**


![image](https://github.com/user-attachments/assets/e122b03d-c862-4283-a97a-8c3bd6cc7910)

**Function:**

``` python
#Function to print the graph that states the correlation of hometown to grades.
plt.figure(figsize=(5,6))
plt.bar (df['Hometown'],df ['Average'])
plt.xlabel ("Hometown" ) 
plt.ylabel ("Average")
plt.title ("Table 1.3: A bar graph showing the relationship of hometown and average grade.")
```

**Output:**


![image](https://github.com/user-attachments/assets/a7f6f602-a833-4463-a9f6-c1f6b24abd7c)

### That is it for this repository I hope you learned something :)))

