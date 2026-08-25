The following SQL code creates a college database named college_demo containing four related tables. 
The department table stores department IDs and names, with dept_id as the primary key. 
The student table stores student details and connects each student to a department using a foreign key. 
The course table stores course information and also connects to departments. 
The enrollment table records which students are enrolled in which courses, along with their semester and grade. 
It uses a composite primary key consisting of roll_no, course_id, and semester. 
Foreign keys maintain relationships and ensure data consistency between all tables.
Normalization is a process of arranging a database into tables such that unnecessary repetition of data does not take place and consistency is maintained. 
In the following database design, the department table holds information about department, the student table holds information about the student, the course table holds information about the course, and the enrollment table helps in linking the student to the course.
For 1NF, each attribute should have a single atomic value and there should be no repeating groups, which is achieved in your database because courses are not present as repeating values within the student table.
For 2NF, the table must be in 1NF and each non-key attribute should be fully functionally dependent on the primary key, which in case of the enrollment table is that grade depends on roll_no, course_id, and semester altogether.
For 3NF, the table must be in 2NF and the non-key attributes should not be dependent on any other non-key attribute, an example being that the dept_name in student table should not be repeating and only one instance is held in department table and dept_id is used as a foreign key.
