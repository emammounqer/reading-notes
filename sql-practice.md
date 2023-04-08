# SQL Practice

## Understanding

the most thing that changed my understanding of sql is Order of execution of a Query, because it always confuse me how group by and order by work, and how to use them and the order of execution is:

- `FROM` and `JOIN` : The **FROM** and **JOIN** clauses are executed first to determine the total working set of data.
- `WHERE` : The **WHERE** clause is then applied to discard rows that do not satisfy the constraint.
- `GROUP BY` : The remaining rows are then grouped by common values in the column specified in the **GROUP BY** clause.
- `HAVING` : The **HAVING** clause is applied to the grouped rows if the query has a GROUP BY clause.
- `SELECT`: Any expressions in the **SELECT** part of the query are then computed.
- `DISTINCT` : Rows with duplicate values in the column marked as **DISTINCT** are discarded.
- `ORDER BY` : The rows are then sorted by the specified data in the **ORDER BY** clause.
- `LIMIT` and `OFFSET` : the **LIMIT** and **OFFSET** clauses are applied to discard rows that fall outside the range specified.

## screenshots

![screen shots 1](./assets/sql/sql-ss%20(1).png)
![screen shots 2](./assets/sql/sql-ss%20(2).png)
![screen shots 3](./assets/sql/sql-ss%20(3).png)
![screen shots 4](./assets/sql/sql-ss%20(4).png)
![screen shots 5](./assets/sql/sql-ss%20(5).png)
![screen shots 6](./assets/sql/sql-ss%20(6).png)
![screen shots 7](./assets/sql/sql-ss%20(7).png)
![screen shots 8](./assets/sql/sql-ss%20(8).png)
![screen shots 9](./assets/sql/sql-ss%20(9).png)
![screen shots 10](./assets/sql/sql-ss%20(10).png)
![screen shots 11](./assets/sql/sql-ss%20(11).png)
![screen shots 12](./assets/sql/sql-ss%20(12).png)
![screen shots 13](./assets/sql/sql-ss%20(13).png)
![screen shots 14](./assets/sql/sql-ss%20(14).png)
![screen shots 15](./assets/sql/sql-ss%20(15).png)
![screen shots 16](./assets/sql/sql-ss%20(16).png)
![screen shots 17](./assets/sql/sql-ss%20(17).png)
