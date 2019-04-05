# **Assignment: Decision making**
#### **Task:**
 ● **Clients complain that the searches for a destinations sometimes fail. Head of product decided to address the issue, and ask development team to work on fix.** 
 
● **The team committed to work out the solution during August. It was agreed that the team’s bonus payout would depend on effectiveness of the solution.**  

● **The Head of Product ask you to analyze the data and help him to decide whether the team deserve the bonus?**

**Here is the link to see the results in** [Google spreadsheet](https://docs.google.com/spreadsheets/d/194XMaTDwEYE6okEWqFwytMPnsHCGDEFv1gxR9r7wTAg/edit?usp=sharing)

**UNDERSTANDING DATA**
We calculate some diferent functions
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

##### **Result**
**%Errors_August**: 1.53%     
**%Correct_August**: 99,6%

**%Errors_September**: 1.03%     
**%Correct_September**: 99.12%

![Gráfica](https://github.com/Lidiamasso/DAM19/blob/master/%25Queries_Error%20by%20Month.Excel.PNG?raw=true)

As we can see above, in August were more Query_errors than in September. It seems that the developers could have fixed some issues.

**Let's see now how is the evolution during the Month**


 We will show how many ***Query_errors*** per day have occurred during August month comparing with September Month and related to how many users has been conected.


![Gráfica](https://github.com/Lidiamasso/DAM19/blob/master/%25%20Queries_Error%20by%20Day.Excel.PNG?raw=true)

As we can see above in September month somedays queries_error where higher than in August

**Now, we will see how is the evolution by Hour**

```
	MES	Valores				
	8		9			
HORAS	SUM de Queries_error	SUM de USERS	SUM de Queries_error	SUM de USERS	August Rate	September Rate
0	364	36112	298	33434	1,01%	0,89%
1	469	29052	299	28845	1,61%	1,04%
2	379	27559	321	25048	1,38%	1,28%
3	343	19303	174	17351	1,78%	1,00%
4	198	9913	111	10683	2,00%	1,04%
5	103	6328	64	7697	1,63%	0,83%
6	94	4705	27	5868	2,00%	0,46%
7	94	6247	36	6199	1,50%	0,58%
8	143	11391	61	10615	1,26%	0,57%
9	292	28667	193	29280	1,02%	0,66%
10	868	48371	949	53390	1,79%	1,78%
11	968	40940	744	45366	2,36%	1,64%
12	899	29987	247	32030	3,00%	0,77%
13	870	31741	286	35049	2,74%	0,82%
14	867	34348	276	38094	2,52%	0,72%
15	829	39000	340	43006	2,13%	0,79%
16	586	43624	488	50873	1,34%	0,96%
17	600	47355	512	47127	1,27%	1,09%
18	537	46044	522	48834	1,17%	1,07%
19	628	53608	689	56769	1,17%	1,21%
20	868	68686	777	69989	1,26%	1,11%
21	670	67373	706	67442	0,99%	1,05%
22	631	60798	478	58249	1,04%	0,82%
23	528	49967	352	45095	1,06%	0,78%
```

![Gráfica](https://github.com/Lidiamasso/DAM19/blob/master/%25%20Queries_Error%20by%20Hours.Excel.PNG?raw=true)


















 

