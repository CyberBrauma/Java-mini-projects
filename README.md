import java.util.Scanner;
public class AssignmentSeven {
  public static void main(String[] args){   
Scanner input = new Scanner(System.in);

System.out.println("What is the daily rate for the car rental? ");
double dailyRate = input.nextDouble();

System.out.println("How many days was the car rented? ");
double daysRented = input.nextDouble();

System.out.println("How many miles was the car driven? ");
double milesDriven = input.nextDouble();

double baseCost = dailyRate * daysRented;

double extraMiles = 0;
double extraCost = 0.0;

if (milesDriven > 150){
    extraMiles = milesDriven - 150;
    extraCost = extraMiles * 0.50;

}
double totalCost = baseCost + extraCost;
System.out.println("The base cost of the rental is $" + baseCost + ". THe cost of going " + extraMiles + " miles over " + milesDriven + " is " + extraMiles + ". The total cost is $ " + totalCost);

if(extraMiles > 0){
    System.out.println("Extra miles driven: " + extraMiles);
}  else{
    System.out.println("Good job! You styaed within the mileage limit! ");
}
System.out.println("Total cost: " + totalCost);
System.out.println("Thank you for choosing our car rental service!");

input.close();
  }  
}

