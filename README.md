# PowerBI DAX Mini Practice 002

This PowerBI mini exercise aims to familiarize users with basic and useful functions in DAX (Data Analysis Expressions). The exercises include:

### 1. Sum of Values
Calculate the total sales by summing the '销售表'[销售数量] column.

```DAX
total_sales = SUM('销售表'[销售数量])
```

### 2. Calculate Sum of Values with Filtering Conditions

#### Single Condition:
Calculate the total sales for product "A" using different tables.

```DAX
total_sales_A_1 = CALCULATE([total_sales], '销售表'[商品名称]="A")
total_sales_A_2 = CALCULATE([total_sales], '商品表'[品名]="A")
```

#### Multiple Conditions:
Calculate the total sales for product "A" with specific conditions.

```DAX
multi_condition_1 = CALCULATE([total_sales], '商品表'[品名]="A", '商品表'[进价]=0.1)
multi_condition_2 = CALCULATE([total_sales], '商品表'[品名] IN {"A", "B"})
```

### 3. Importance of Using Dimension Table for Filtering

Highlight the significance of utilizing a dimension table to filter the fact table when visualizing data using a matrix.

### 4. Measure Storage Best Practices

Provide guidance on storing measures efficiently.

### Additional Information

This exercise is inspired by [Bilibili user 437239552](https://space.bilibili.com/437239552).

Feel free to explore and apply these DAX functions to enhance your PowerBI skills!
