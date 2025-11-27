# 🎓 Hackerrank:Python Program to Find Students with the Second Lowest Grade

This program reads student names and their corresponding grades, identifies the **second lowest grade**, and prints the names of all students who have that grade in **alphabetical order**.


## 🎯 Aim

To write a Python program to:
- Read a list of students and their grades.
- Identify the second lowest grade.
- Print the names of students who have that grade, sorted alphabetically.


## 🧠 Algorithm

1. **Read** an integer `n` representing the number of students.
2. **Read** each student’s name and grade, and store them as a sublist inside a list.
3. **Extract** all the grades and sort them.
4. **Identify** the second lowest grade from the sorted grade list.
5. **Collect** names of all students whose grade matches the second lowest grade.
6. **Sort** the names alphabetically.
7. **Print** each name on a new line.


## 💻  Program

if __name__ == '__main__':
    students = []
    for _ in range(int(input())):
        name = input()
        score = float(input())
        students.append([name, score])

    unique_scores = sorted(set([student[1] for student in students]))
    
    second_lowest_grade = unique_scores[1]

    second_lowest_students = [student[0] for student in students if student[1] == second_lowest_grade]

    second_lowest_students.sort()

    for name in second_lowest_students:
        print(name)

## Output

5
Harry
37.21
Berry
37.21
Tina
37.2
Akriti
41
Harsh
39

Berry
Harry
## Result

The Python program to find students with the second lowest grade was successfully executed. The logic correctly handled identifying the unique grades, selecting the second lowest, and printing the corresponding student names in alphabetical order.
