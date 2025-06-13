 🎓 University Examination System

This project is a relational database design for managing a **university examination system**, which includes entities such as **students**, **faculty members**, **departments**, **courses**, **exams**, and **exam attempts**. It provides a robust structure to handle complex relationships like course enrollment, teaching assignments, department coordination, and multi-attempt exams.



 📁 Entities and Relationships

 👨‍🏫 Faculty
- Attributes: Faculty_ID (PK), Name, Designation
- A faculty member can:
  - Head a department
  - Coordinate courses
  - Teach multiple courses
  - Create exams

  🏬 Department
- Attributes: Dept_ID (PK), Dept_Name, Head_Faculty_ID (FK)
- Each department has:
  - A unique name
  - A head (faculty member)
  - Multiple offered courses

  📚 Course
- Attributes: Course_Code (PK), Title, Dept_ID (FK), Coordinator_ID (FK)
- Each course belongs to one department and is coordinated by a faculty member.
- A course can be taught by multiple faculty members.

 👩‍🎓 Student
- Attributes: Roll_No (PK), Student_Name, Dept_ID (FK)
- Each student:
  - Belongs to one department
  - Can enroll in multiple courses offered by their department

 📘 Student_Course (Enrollment)
- Junction table representing students' enrollment in courses.
- Tracks:
  - Attendance percentage
  - Courses per student

 📝 Exam
- Attributes: Exam_ID (PK), Title, Subject_Name, Duration, Exam_Date, Exam_Type, Course_Code (FK), Created_By (FK)
- Each exam is:
  - Created by a faculty member
  - Linked to a course (subject name assumed same as course title)
  - Can be of type internal or external

 🎯 Exam_Attempt
- Tracks students' attempts for each exam.
- Attributes include: Attempt_ID (PK), Exam_ID (FK), Roll_No (FK), Attempt_Number, Marks
- A student can have multiple attempts for the same exam.

---

 🏗️ Table Structure

SQL scripts are included for:
- Table creation with primary and foreign keys
- Relationships reflecting real-world constraints
- Support for multiple roles (e.g., faculty as department head and course coordinator)



📦 Sample Use Cases

- Track exam creation and participation
- Analyze attendance and academic performance
- Assign department heads and course coordinators
- Allow students to reattempt exams with individual marks recorded

 🛠️ Technologies Used

- SQL (MySQL / PostgreSQL compatible)
- Relational database design principles
- Normalization for data integrity



 📂 Files

- `create_tables.sql` – Contains all `CREATE TABLE` statements.
- `README.md` – Project overview and documentation (this file).


 🚀 Future Enhancements (Optional Ideas)

- Add Faculty-Course teaching assignments explicitly
- Include grades or pass/fail status in Exam_Attempt
- Add triggers to calculate GPA or validate attendance


![image](https://github.com/user-attachments/assets/28e4ce6a-604a-49cd-871a-265335348395)

![image](https://github.com/user-attachments/assets/52f67591-a37e-434d-8c22-a0c22c5322c1)


