import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numberOfSubjects;
        double totalMarks = 0;

        // Prompt user to enter the number of subjects
        System.out.print("Enter the number of subjects: ");
        numberOfSubjects = scanner.nextInt();

        double[] marks = new double[numberOfSubjects];

        // Prompt user to enter the marks for each subject
        for (int i = 0; i < numberOfSubjects; i++) {
            System.out.print("Enter the marks for subject " + (i + 1) + ": ");
            marks[i] = scanner.nextDouble();
            totalMarks += marks[i];
        }

        // Calculate the total marks and average percentage
        double averagePercentage = totalMarks / numberOfSubjects;

        // Determine the grade based on the average percentage
        char grade;
        if (averagePercentage >= 90) {
            grade = 'A';
        } else if (averagePercentage >= 80) {
            grade = 'B';
        } else if (averagePercentage >= 70) {
            grade = 'C';
        } else if (averagePercentage >= 60) {
            grade = 'D';
        } else {
            grade = 'F';
        }

        // Display the results
        System.out.println("Total Marks: " + totalMarks);
        System.out.println("Average Percentage: " + averagePercentage + "%");
        System.out.println("Grade: " + grade);

        scanner.close();
    }
}
