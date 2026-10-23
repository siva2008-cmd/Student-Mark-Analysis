# Student-Mark-Analysis
# Mark Analysis Program for 3 Subjects

subjects = ["Math", "Science", "English"]

marks = {}
total = 0

for subject in subjects:
    score = float(input(f"Enter marks for {subject} (out of 100): "))
    while score < 0 or score > 100:
        print("Invalid marks! Please enter a value between 0 and 100.")
        score = float(input(f"Enter marks for {subject} (out of 100): "))
    marks[subject] = score
    total += score

average = total / len(subjects)

# Grade calculation based on average
if average >= 90:
    grade = "A"
elif average >= 80:
    grade = "B"
elif average >= 70:
    grade = "C"
elif average >= 60:
    grade = "D"
else:
    grade = "F"

print("\n--- Mark Analysis ---")
for subject in subjects:
    print(f"{subject}: {marks[subject]}")

print(f"Total Marks: {total}")
print(f"Average Marks: {average:.2f}")
print(f"Grade: {grade}")
