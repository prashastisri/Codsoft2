package program1;
	import java.util.Scanner;
public class Codsoft2
 {
	    public static void main(String[] args) {
	        Scanner scanner = new Scanner(System.in);
	        
	        // Constants for grade calculation
	        final double A_GRADE_THRESHOLD = 90.0;
	        final double B_GRADE_THRESHOLD = 80.0;
	        final double C_GRADE_THRESHOLD = 70.0;
	        final double D_GRADE_THRESHOLD = 60.0;
	        
	        // Number of subjects
	        System.out.print("Enter the number of subjects: ");
	        int numSubjects = scanner.nextInt();
	        
	        // Variables for total marks and grades
	        int totalMarks = 0;
	        char grade;
	        
	        // Input marks for each subject
	        for (int i = 1; i <= numSubjects; i++) {
	            System.out.print("Enter marks obtained in subject " + i + ": ");
	            int marks = scanner.nextInt();
	            totalMarks += marks;
	        }
	        
	        // Calculate average percentage
	        double averagePercentage = (double) totalMarks / numSubjects;
	        
	        // Assign grades based on average percentage
	        if (averagePercentage >= A_GRADE_THRESHOLD) {
	            grade = 'A';
	        } else if (averagePercentage >= B_GRADE_THRESHOLD) {
	            grade = 'B';
	        } else if (averagePercentage >= C_GRADE_THRESHOLD) {
	            grade = 'C';
	        } else if (averagePercentage >= D_GRADE_THRESHOLD) {
	            grade = 'D';
	        } else {
	            grade = 'F';
	        }
	        
	        // Display results
	        System.out.println("\nTotal Marks: " + totalMarks);
	        System.out.println("Average Percentage: " + averagePercentage + "%");
	        System.out.println("Grade: " + grade);
	        
	        scanner.close();
	    }
	}
