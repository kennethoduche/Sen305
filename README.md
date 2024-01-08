
```java
import java.util.Scanner;

          public class SGPA_Calculator 
        {
    public static void main(String[] args)
     {
        // Course names
        String[] courseNames = {"SEN 201", "SEN 202", "SEN 203", "SEN 204", "Gst 211", "SEN 206", "SEN 209", "Gst 271", "SEN 210"};
        
        // Credit Units
        int[] creditUnits = {3, 2, 3, 2, 2, 3, 2, 2, 3};
        
        // Grade Points
        double[] gradePoints = {5.0, 4.0, 3.0, 2.0, 1.0, 0.0};
        
        // Scanner to read user input
        Scanner scanner = new Scanner(System.in);
        
        // Variables to store total credit points and total credit units
        double totalCreditPoints = 0.0;
        int totalCreditUnits = 0;
        
        // Loop through each course
        for (int i = 0; i < courseNames.length; i++) {
            // Prompt user for course grade
            System.out.print("Enter grade obtained for " + courseNames[i] + ": ");
            String grade = scanner.nextLine();
            
            // Calculate grade points based on the grade entered
            double gradePoint = 0.0;
            if (grade.equalsIgnoreCase("A")) {
                gradePoint = gradePoints[0];
            }
              else if (grade.equalsIgnoreCase("B")) 
            {
                gradePoint = gradePoints[1];
            } 
               else if (grade.equalsIgnoreCase("C")) 
            {
                gradePoint = gradePoints[2];
            } 
               else if (grade.equalsIgnoreCase("D")) 
            {
                gradePoint = gradePoints[3];
            } 
             else if (grade.equalsIgnoreCase("E")) 
             {
                gradePoint = gradePoints[4];
            }   
             else if (grade.equalsIgnoreCase("F")) 
             {
                gradePoint = gradePoints[5];
            } 
               else 
             {
                System.out.println("Invalid grade submitted. Please try again.");
                i--; // Decrement i to repeat the current iteration
                continue; // Skip the rest of the current iteration
            }
            
            // Calculate credit points for the course
            double creditPoints
