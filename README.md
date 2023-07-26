# Assignment-1
def calculate_grade(marks):
    if marks >= 90:
        return "A+"
    elif marks >= 80:
        return "A"
    elif marks >= 70:
        return "B"
    elif marks >= 60:
        return "C"
    elif marks >= 50:
        return "D"
    else:
        return "Fail"

def get_valid_marks():
    while True:
        try:
            marks = float(input("Enter the marks obtained by the student: "))
            if 0 <= marks <= 100:
                return marks
            else:
                print("Invalid input! Marks should be between 0 and 100.")
        except ValueError:
            print("Invalid input! Please enter a numeric value for marks.")

def main():
    print("Welcome to the Student Grading Program!")
    while True:
        marks = get_valid_marks()
        grade = calculate_grade(marks)
        print(f"Grade: {grade}\n")

        choice = input("Do you want to calculate grade for another student? (y/n): ")
        if choice.lower() != 'y':
            break

    print("Thank you for using the Student Grading Program!")

if __name__ == "__main__":
    main()
