# Student-Assignment-Counter
This is a Bash + AWK script that analyzes student assignment records and counts how many times each assignment was submitted by each student. It's designed to process log-style or space-separated records where each line contains at least a student ID and an assignment name.

##  Features

- Groups records by student ID
- Counts the number of times each assignment was submitted by each student
- Automatically resets counters between students
- Outputs results in a readable grouped format
- Efficient, stream-based (processes sorted input line by line)

---

##  Input Format

The script expects a text file with **space-separated** fields. For example:
There are 4 columns, date, time, student_number, assignment_name respectively.
2024-05-10 12:30 23001 A1
2024-05-09 13:40 23002 A1
2024-05-20 14:00 23001 A2
2024-05-11 15:10 23003 A1
2024-05-30 15:30 23001 A3
2024-05-30 15:33 23001 A3
2024-05-30 15:40 23001 A3
2024-05-30 21:30 23001 A3
2024-05-21 14:00 23001 A2

##  Why Sort First?

- Keeps the code simple
- Avoids unnecessary memory usage
- Scales better for large files

