# ECE_2112_P.A-4
## Programming Assignment #4

### Objectives:
#### 1. To identify the codes and functions needed in cleaning and visualizing data
#### 2. To be able to apply and use the different codes and functions in creating a Python program that will be used in data wrangling and data visualization

### Instructions:
##### Download the ECE Board Exam 2 dataset found on this link: bit.ly/ECEBoardExamDataset and write a
##### Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.

### ECE BOARD EXAM PROBLEM: Using data wrangling and data visualization technique with storytelling, analyze the data and present different (i) data frames; and (ii) visuals using the dataset given

#### Problem #1:
### ![image](https://github.com/user-attachments/assets/c9587a55-5df6-42e5-875c-3b112718c097)


## Problems/Insights to the Code: 
### 1. we first Import the pandas library to get the given Problems
## ![image](https://github.com/user-attachments/assets/05b03efe-f975-4247-b643-8b2ebf42ebbd)
### 2. We need to import/ read the file and the data frame given to us and naming it df, hence to read it we use the .read_excell() function
### ![image](https://github.com/user-attachments/assets/10f665bc-f32b-410e-837b-2240dcc1b373)
### Output for the code:
### ![image](https://github.com/user-attachments/assets/3bd6c0a1-901d-4fb3-ae29-5026b6760730)

### 3. A. The variable instru should Output the Name, GEAS, Elecronics should be greater than 70 where the track should be instrumentation and the hometown is Luzon
### Solution to the Problem A
#### ![image](https://github.com/user-attachments/assets/b3b29c1e-091a-4790-b190-94a5a387530e)
#### we use use .loc function to identify and to get the function we need:
#### - (df['Hometown'] ==  'luzon') where it would output the hometown who are only in Luzon
#### - (df['Electronics']>70 ) where it would only output the score In electronics who is greater than 70
#### - (df['Track'] == 'Instrumentation') where it would only output the track is only on Instrumentation
#### - ,['Name', 'GEAS', 'Electronics'] this would only output the columns that is said
#### - we use & so that the given should Satify all the conditions met

### Output of the code:
# ![image](https://github.com/user-attachments/assets/7c668614-9814-4a89-832b-8a548805c011)

### 4. B. The Variable Mindy should hold the following conditions it should only ouput ['Name', 'Track', 'Electronics', 'Average>55 '] where the hometown is located on mindanao and the gender is Female
### 4.1 new problem arises in which we dont have Average of the subjects, hence we make one using this block of code: 
### ![image](https://github.com/user-attachments/assets/18f4b1d2-cc75-41d4-a5b8-7292320cbe56)
#### - we use df['Average'] as new variable 
#### - df['GEAS', 'Electronics', 'Math', 'Communication'].mean(axis=1) Utilizing the.mean function we mean the whole row and in order to do that we put the axis on 1 hence in each list we average the row and put it into df['Average']
#### - df['Hometown'] == 'Mindanao' where it would specified the hometown output to only mindanao
#### - df['Gender']== 'Female' where it would only output only Female on the Gender category
#### - df['Average'] > 55 where it would only output only greater than 55 of score
#### - ,['Name', 'Track', 'Electronics', 'Average'] the only colomns to be output

### Output Of the Code:
## ![image](https://github.com/user-attachments/assets/dfb59493-c67e-40ba-90b9-b6b79f902972)


### Problem 2
# ![image](https://github.com/user-attachments/assets/ce607973-c684-4b1b-a955-560247e39297)

### 1. First we Import matpolib Library
# ![image](https://github.com/user-attachments/assets/52d39a46-b93f-4770-8dca-c68b8eb775ee)


### 2. Average Score per Track we use Visualization or a bar Graph to show which Track is the most promising on the Board exam
### Code to Solve the Problem:
### ![image](https://github.com/user-attachments/assets/46d07efe-f1e1-4627-bf70-89a0721f1ada)

#### - plt.figure(figsize=(5, 5)) we  use ply.figure to set how big in x and y axis of the graph
#### - track = plt.bar(df['Track'], df['Average']) utilizing this function to set what should we input unto the bar graph
#### - plt.xlabel('Track') we use this function to name the Graph on the x axis
#### - plt.ylabel('Average') we use this function to name the Graph on the y axis
#### - plt.title('Average by Track') we use this function to name the Entire Graph
#### - plt.show() utilizing this function we can see the data
### Output Of the Code: 
# ![image](https://github.com/user-attachments/assets/89d011a6-1c2d-4d89-9233-37d11ec03f3b)
#### By the Description of the Table we can see that Microelectronics track it the one who is the Most promising on the board exam following by communication, then Instrumentation

### 3. Average score per Gender we use Visualization or a bar Graph to show which Track is the most promising on the Board exam
### Code To Solve The Problem: 
#### ![image](https://github.com/user-attachments/assets/0a584a06-0f0a-4dce-96b8-85f112aeff14)

#### plt.figure(figsize = (5,5))  we  use ply.figure to set how big in x and y axis of the graph
#### track = plt.bar(df['Gender'], df['Average']) utilizing this function to set what should we input unto the bar graph
#### plt.xlabel('Gender')  we use this function to name the Graph on the x axis
#### plt.ylabel('Average')  we use this function to name the Graph on the y axis
#### plt.title('Average by Gender')  we use this function to name the Entire Graph
### plt.show()  utilizing this function we can see the data

### Ouput Of the Code:
# ![image](https://github.com/user-attachments/assets/c5496f42-cc46-4b96-b927-c8b334791e74)
#### As the Table shows it is clear that The most Promising or the one who has the Higher Average are the Females rather than the Males

### 4.  Average score per Hometown we use Visualization or a bar Graph to show which Track is the most promising on the Board exam
### Code To Solve the Problem: 
# ![image](https://github.com/user-attachments/assets/af33abcb-5090-4d06-9064-25623eb9b3b7)

#### plt.figure(figsize = (5,5))  we  use ply.figure to set how big in x and y axis of the graph
#### track = plt.bar(df['Hometown'], df['Average']) utilizing this function to set what should we input unto the bar graph
#### plt.xlabel('Hometown')  we use this function to name the Graph on the x axis
#### plt.ylabel('Average')  we use this function to name the Graph on the y axis
#### plt.title('Average Score by Hometown')  we use this function to name the Entire Graph
### plt.show()  utilizing this function we can see the data

### Output of the Code: 
# ![image](https://github.com/user-attachments/assets/d00af531-a893-47fc-8038-1172b0365077)
##### By the graph has shown the highest Average by hometown is Luzon next is Visayas followed by Mindanao

## Author:
#### Angostora, Tristan Zeth V.

## Program Advisers:
####  P.A provided by: Engr. Ma. Madecheen S. Pangaliman, M.Sc.
##### • Faculty member at UST-ECE Department
##### • PhD EEE with specialization in AI and
##### Robotics student at UP-Diliman



r 





