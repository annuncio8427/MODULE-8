## 🎯 Aim

To maintain a dictionary of students with their marks in five subjects, calculate their **total marks**, store them in a new dictionary, and identify the **student with the highest total (topper)**.

---

## 🧠 Algorithm

1. **Start** the program.
2. Create a dictionary `student_marks`:
   - Keys → Student names.
   - Values → List of marks in five subjects.
3. Initialize an empty dictionary `total_marks`.
4. Loop through `student_marks`:
   - Calculate the total marks using `sum()`.
   - Store the result in `total_marks`.
5. Use `max()` on `total_marks` to find the student with the highest total.
6. Print:
   - The `total_marks` dictionary.
   - The **topper's name and score**.

---

## 💻 PROGRAM:

student_marks = {
    "Arun": [85, 92, 78, 90, 88],
    "Bina": [79, 85, 80, 82, 75],
    "Chitra": [95, 90, 92, 89, 94],
    "David": [88, 76, 85, 90, 82]
}

total_marks = {}

for student, marks in student_marks.items():
    total_marks[student] = sum(marks)

topper_name = max(total_marks, key=total_marks.get)
topper_score = total_marks[topper_name]

print("Total Marks Dictionary:", total_marks)
print("-" * 30)
print(f"The Class Topper is {topper_name} with {topper_score} marks.")

## OUTPUT

Total Marks Dictionary: {'Arun': 433, 'Bina': 401, 'Chitra': 460, 'David': 421}
------------------------------
The Class Topper is Chitra with 460 marks.

## RESULT

The program was successfully executed. The dictionary of student marks was processed to calculate total scores, and the student with the highest total marks was correctly identified and displayed as the topper.
