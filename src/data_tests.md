
## Data tests

Data tests are `ASSERT` statements that you can run on your database tables and views and perform checks on data quality, recency, etc. Assert statements checks the result of a condition - a boolean expression.
Assert-based testing are enabled for every backend, they are translated by PowerSQL to queries return a
boolean.

Some examples:
```sql
-- Column should be NOT NULL
ASSERT NOT EXISTS(
  SELECT X
  FROM t
  WHERE column IS NULL
) AS 'column should be non null';
ASSERT NOT EXISTS (
    SELECT quantity
    FROM rev_per_product
    WHERE quantity <= 0
) AS 'quantity should be positive';
ASSERT NOT EXISTS (
    SELECT product_id
    FROM rev_per_product
    WHERE product_id IS NULL
) AS 'product_id should be not null';
ASSERT (
    SELECT COUNT (*)
    FROM rev_per_product
    WHERE quantity < 10
) >= 0.7 * (    
    SELECT COUNT(*)
    FROM rev_per_product
) AS 'At least 70% should have a quantity lower than 10'
```
