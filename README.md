
-- Task 1: Arrange the 'Orders' dataset in decreasing order of amount

SELECT 
    * FROM 
    orders_table
ORDER BY 
    amount DESC;


-- Task 2: Create and populate 'Employee_details1' and 'Employee_details2'


-- Create the first table
CREATE TABLE Employee_details1
(
    Emp_id INT,
    Emp_name VARCHAR(20),
    Emp_salary INT
);

-- Insert data into Employee_details1
INSERT INTO Employee_details1 (Emp_id, Emp_name, Emp_salary)
VALUES
    (1, 'Thomas', 23450),
    (2, 'Willson', 75643),
    (3, 'Ustad', 34624),
    (4, 'Merlin', 78422),
    (9, 'Berlin', 76239); 

-- Create the second table
CREATE TABLE Employee_details2
(
    Emp_id INT,
    Emp_name VARCHAR(20),
    Emp_salary INT
);

-- Insert data into Employee_details2
INSERT INTO Employee_details2 (Emp_id, Emp_name, Emp_salary)
VALUES
    (5, 'Mathew', 23450),
    (6, 'Neslen', 75643),
    (7, 'Hazel', 34624),
    (8, 'Max', 78422),
    (9, 'Berlin', 76239);


-- Task 3: Apply the UNION operator

SELECT 
    * FROM 
    Employee_details1 
UNION
SELECT 
    * FROM 
    Employee_details2;

-- Task 4: Apply the INTERSECT operator

SELECT 
    * FROM 
    Employee_details1 
INTERSECT
SELECT 
    * FROM 
    Employee_details2;

-- Task 5: Apply the EXCEPT operator


-- A. Rows unique to Employee_details1
SELECT 
    * FROM 
    Employee_details1 
EXCEPT
SELECT 
    * FROM 
    Employee_details2;

-- B. Rows unique to Employee_details2
SELECT 
    * FROM 
    Employee_details2 
EXCEPT
SELECT 
    * FROM 
    Employee_details1;
