# bmi-calc
Calculates BMI

/*
Name: Angelo Alviar
Date: 10/11/2017
Comments: N/A
 */
package programmingassignment1;

import java.util.Scanner; //import Scanner tool
import java.text.NumberFormat; //import NumberFormat tool

/**
 *
 * @author angelo alviar
 */
public class ProgrammingAssignment1 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
        // TODO code application logic here
    
   // Create an object of Scanner class
   Scanner sc = new Scanner(System.in); //sc is a variable

   //Prompt user to type their names
   System.out.println("Please type your name. ");
    
   //Store name typed by user
   String inputName = sc.next();

    
   //Prompt user to type weight in pounds
   System.out.println("Type your weight (in pounds). ");
    
   //Store weight typed by user
   double inputWeight = sc.nextDouble();
    
   //Prompt user to type height in inches
   System.out.println("Type your height (in inches). ");
   
   //Store height typed by user
   double inputHeight = sc.nextDouble();
   
   //Calculate BMI
   double BMI = inputWeight / (inputHeight * inputHeight) * 703;
   
   //Declare category
   String category = "";
        
    //Determine BMI category through if else if statement
        if(BMI >= 40) //No semicolon needed
        {
            category = "Morbidly Obese";
        }
        else if(BMI >= 35)
        {
            category = "Severely Obese";
        }
        else if(BMI >= 30)
        {
            category = "Obese";
        }
        else if(BMI >= 25)
        {
            category ="Overweight";
        }
        else if(BMI >= 18.5)
        {
            category = "Normal";
        }
        else
        {
            category = "Underweight";
        }
       
   //Create an object of NumberFormat class
   NumberFormat number = NumberFormat.getNumberInstance();
   
   //Set maximum fraction digits
   number.setMaximumFractionDigits(2);
           
   //Store BMI into a string in order to format it
   String BMIString = number.format(BMI);
   
        //Print out name, weight, height, BMI, and BMI category
        System.out.println("Name: " + inputName);
        System.out.println("Weight: " + inputWeight + " pounds ");
        System.out.println("Height: " + inputHeight + " inches ");
        System.out.println("BMI: " + BMIString);
        System.out.println("BMI Category: " + category);
    
    
    }

}
