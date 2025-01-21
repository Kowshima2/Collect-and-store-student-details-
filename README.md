# Collect-and-store-student-details-
import java.util.ArrayList;
import java.util.Scanner
class Student {
    private String name;
    private int age;
    private String grade;
    public Student(String name, int age, String grade) {
        this.name = name;
        this.age = age;
        this.grade = grade;
    }
    public void displayStudentDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Grade: " + grade);
    }
}

public class StudentDetails {
    public static void main(String[] args) 
        ArrayList<Student> students = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter the number of students:");
        int numberOfStudents = scanner.nextInt();
        scanner.nextLine(); 

        for (int i = 0; i < numberOfStudents; i++) {
            System.out.println("Enter details for student " + (i + 1) + ":");

            System.out.print("Enter name: ");
            String name = scanner.nextLine();

            System.out.print("Enter age: ");
            int age = scanner.nextInt();
            scanner.nextLine(); 

            System.out.print("Enter grade: ");
            String grade = scanner.nextLine();

           
            students.add(new Student(name, age, grade));
        }

        // Display all student details
        System.out.println("\nStudent Details:");
        for (Student student : students) {
            student.displayStudentDetails();
            System.out.println();
        }

        scanner.close();
    }
}


Output 
Student Details:
Name: Alice
Age: 20
Grade: A

Name: Bob
Age: 22
Grade: B
