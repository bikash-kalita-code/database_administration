# Pattern Matching
Use the `LIKE` or `NOT LIKE` comparison operators for pattern matching.

**NOTE:**
 - `%` matches any number of characters
 - `_` matches only one character
 - The matching here is case insensitive

### Examples:

 - To find names beginning with characater **b**:\
 `SELECT * FROM pet WHERE name LIKE 'b%';`
 - To find names ending with **fy**:\
 `SELECT * FROM pet WHERE name LIKE '%fy';`
 - To find names cotaining **w**:\
 `SELECT * FROM pet WHERE name LIKE '%w%';`
 - To find name containing exactly 5 characters:\
 `SELECT * FROM pet WHERE name LIKE '_____';`
    
## Using Regular Expressions:
Use the `REGEXP_LIKE()` function (or the `REGEXP` or `RLIKE` operators, which are synonyms for `REGEXP_LIKE()`).

### Examples:

 - To find names beginning with **b**, use **^** to match the beginning of the name:
 `SELECT * FROM pet WHERE REGEXP_LIKE(name, '^b');`