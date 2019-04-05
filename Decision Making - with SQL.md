# **Assignment: Decision making**
#### **Task:**
 ● **Clients complain that the searches for a destinations sometimes fail. Head of product decided to address the issue, and ask development team to work on fix.** 
 
● **The team committed to work out the solution during August. It was agreed that the team’s bonus payout would depend on effectiveness of the solution.**  

● **The Head of Product ask you to analyze the data and help him to decide whether the team deserve the bonus?**

**Here is the link to see the results in** [Google spreadsheet] 

[Google spreadsheet]:(https://docs.google.com/spreadsheets/d/194XMaTDwEYE6okEWqFwytMPnsHCGDEFv1gxR9r7wTAg/edit?usp=sharing)

**UNDERSTANDING DATA**
We calculate some diferent functions
August:
```
SELECT
    sum(users) as Total_Users,
    sum(Queries_correct) as Total_correct,
    sum(Queries_error) as Total_Error,
    max(Queries_error) as Max_error,
    min(Queries_error) as Min_error,
    avg(Queries_error) as Avg_error,
    max(Queries_correct) as Max_correct,
    min(Queries_correct) as Min_correct,
    avg(Queries_correct) as Avg_correct
From Agosto_
GROUP BY MES
```
##### **Result**
**August**
**Total_Users**= 841119

**Total_correct**= 834060

**Total_Error** = 12828

**Max_error** = 142

**Min_error** = 0

**Avg_error** = 4.5409

**Max_correct** = 896

**Min_correct** = 7 

**Avg_correct** = 295.2425


**September**

```
SELECT
    sum(users) as Total_Users,
    sum(Queries_correct) as Total_correct,
    sum(Queries_error) as Total_Error,
    max(Queries_error) as Max_error,
    min(Queries_error) as Min_error,
    avg(Queries_error) as Avg_error,
    max(Queries_correct) as Max_correct,
    min(Queries_correct) as Min_correct,
    avg(Queries_correct) as Avg_correct
From Septiembre
GROUP BY MES
```
**Total_Users**= 866333

**Total_correct**= 858740

**Total_Error** = 8950

**Max_error** = 38

**Min_error** = 0

**Avg_error** = 3.7684

**Max_correct** = 1160

**Min_correct** = 10 

**Avg_correct** = 361.5747

We can see that *Queries_error* in August month there are some extremely high values. 

**EXPLORING DATA**
We would like to know the difference between how many users and *query_errors* ocurred in August and how many users and *query_errors* ocurred in September
```
SELECT		
    ROUND((sum(a.queries_error)/sum(a.users)*100),2) AS '% Rate_Error_August',
    ROUND((sum(a.Queries_correct)/sum(a.users)*100),2) AS '% Rate_Correct_August',
    ROUND((sum(s.queries_error)/sum(s.users)*100),2) AS '% Rate_Error_September',
    ROUND((sum(s.Queries_correct)/sum(s.users)*100),2) AS '% Rate_Correct_September'

    
FROM Agosto_ AS a INNER JOIN Septiembre as s 
GROUP BY a.MONTH
````
##### **Result**
**%Errors_August**: 1.53%     
**%Correct_August**: 99,6%
**%Errors_September**: 1.03%     
**%Correct_September**: 99.12%

![Gráfica](https://github.com/Lidiamasso/DAM19/blob/master/%25Queries_Error%20by%20Month.PNG?raw=true)

As we can see above, in August were more Query_errors than in September. It seems that the developers could have fixed some issues.

**Let's see now how is the evolution during the Month**


 We will show how many ***Query_errors*** per day have occurred during August month comparing with September Month and related to how many users has been conected.

```
SELECT
    sum(a.users) AS Users_A,
    sum(a.queries_error) AS Error_August,
    (sum(a.queries_error)/sum(a.users)*100) AS '% August',
    sum(s.users) AS Users_S,
    sum(s.queries_error) AS Error_September,
    (sum(s.queries_error)/sum(s.users)*100) AS '% September',
    a.DAY
FROM 
    Agosto_ AS a LEFT JOIN Setiembre AS s ON a.day = s.day
GROUP BY 
    a.day
```
![Gráfica](https://github.com/Lidiamasso/DAM19/blob/master/%25Queries_Error%20by%20Day.JPG?raw=true)

As we can see above in September month somedays queries_error where higher than in August

**Now, we will see how is the evolution by Hour**
```
SELECT
    sum(a.users) AS Users_A,
    sum(a.queries_error) AS Error_August,
    (sum(a.queries_error)/sum(a.users)*100) AS '% August',
    sum(s.users) AS Users_S,
    sum(s.queries_error) AS Error_September,
    (sum(s.queries_error)/sum(s.users)*100) AS '% September',
    a.HOURS
FROM 
   Agosto_ AS a LEFT JOIN Setiembre AS s ON a.hours = s.HOURS
GROUP BY 
    a.HOURS
```
![Gráfica](https://github.com/Lidiamasso/DAM19/blob/master/%25%20Queries_Error%20by%20Hours.PNG?raw=true)

















 

