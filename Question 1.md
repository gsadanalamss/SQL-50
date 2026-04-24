## Question 1

### Table: Products

| Column Name | Type |
|-------------|------|
| product_id  | int  |
| low_fats    | enum |
| recyclable  | enum |

- `product_id` is the primary key (column with unique values) for this table.  
- `low_fats` is an ENUM ('Y', 'N') where:
  - 'Y' means the product is low fat  
  - 'N' means it is not  
- `recyclable` is an ENUM ('Y', 'N') where:
  - 'Y' means the product is recyclable  
  - 'N' means it is not  

### Problem

Write a query to find the **IDs of products** that are **both low fat and recyclable**.

Return the result table in **any order**.

---

### Example 1

#### Input

**Products table:**

| product_id | low_fats | recyclable |
|------------|----------|------------|
| 0          | Y        | N          |
| 1          | Y        | Y          |
| 2          | N        | Y          |
| 3          | Y        | Y          |
| 4          | N        | N          |

#### Output

| product_id |
|------------|
| 1          |
| 3          |

#### Explanation

Only products **1** and **3** are both **low fat** and **recyclable**.

## Solution 
```
select product_id from Products 
where low_fats = "Y" and 
recyclable = "Y";
```
