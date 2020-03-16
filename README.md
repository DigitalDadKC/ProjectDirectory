# ProjectDirectory

Comprehensive project directory featuring a DataTables index, project analysis, project comparison, and project modelling.

STILL IN DEVELOPMENT!

Highlights include:
- Querying INFORMATION_SCHEMA for 129 column names with a prepared statement in order to concatenate another Inception-style query to sum various combinations of a 41-element array.

SELECT CONCAT('SELECT ', GROUP_CONCAT(COLUMN_NAME SEPARATOR '+'), ' FROM GUIDE.BuildUp;') FROM INFORMATION_SCHEMA.COLUMNS WHERE COLUMN_NAME LIKE ? AND TABLE_SCHEMA='GUIDE' AND TABLE_NAME='BuildUp' AND COLUMN_NAME != 'id' AND COLUMN_NAME != 'fk_Project';

- Traversing the DOM in order to sum 3 nested levels (2 subtotal levels and 1 grand total).
