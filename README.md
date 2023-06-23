# Excel_Formulas
This repository has some formulas for Excel!

### Conditional Operations

The formula "=AVERAGEIF(A1:A14, x, B1:B14)" calculates the average values in range B1:B14 based on a specific condition in range A1:A14.
The condition is that the corresponding cell in range A1:A14 must equal x. The formula will consider only those values in range B1:B14 where the corresponding cell in range A1:A14 meets this condition.

```
=AVERAGEIF(A1:A14, x, B1:B14)
```
Here's an example of how you can calculate the standard deviation of values in range B1:B14 based on a condition in range A1:A14:
```
=STDEV(IF(A1:A14=x, B1:B14))
```


### Box Plots
To create a box plot of values in range B1:B14 based on a specific condition in range A1:A14, you can follow these steps in Excel:

Filter the data based on the desired condition in column A.

Click on the filter button in the header of column A and select the value(s) you want to include in the box plot (e.g., select "1" to filter for cells equal to 1).
This will display only the rows where the condition is met.
Calculate the necessary statistical measures for the box plot.

In an empty column, let's say column C, enter the following formulas:

- In C1, enter "=QUARTILE.INC($B$1:$B$14,1)" to calculate the first quartile (Q1).

- In C2, enter "=MEDIAN($B$1:$B$14)" to calculate the median (Q2).
- In C3, enter "=QUARTILE.INC($B$1:$B$14,3)" to calculate the third quartile (Q3).
- In C4, enter "=C3-C1" to calculate the interquartile range (IQR).
- In C5, enter "=C1-1.5*C4" to calculate the lower whisker limit.
- In C6, enter "=C3+1.5*C4" to calculate the upper whisker limit.

**Create a box plot chart**
- Select the data in columns B and C (including the headers).
- Insert a box plot chart by going to the "Insert" tab, selecting the "Statistical" chart category, and choosing the "Box and Whisker" chart type.
- Excel will generate the box plot chart based on the filtered data and the calculated statistical measures.
