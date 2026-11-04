# cis165-lab6

Program Plans
Program 1: BMI Calculator
Inputs:
Weight in pounds.
Height in inches.
Variables:
weight: stores the user's weight as a double.
height: stores the user's height as a double.
bmi: stores the calculated BMI as a double.
Validation:
Check that weight is greater than zero.
Check that height is greater than zero.
Display an error and stop if either value is zero or negative.
Calculation:
Use the formula:
bmi = weight * 703.0 / (height * height);
Output:
Display BMI to two decimal places.
Display Underweight, Optimal weight, or Overweight.
Tests planned:
Underweight BMI.
Optimal BMI.
Overweight BMI.
Zero weight or height.
Negative weight or height.

Program 2: Color Mixer
Inputs:
First primary color.
Second primary color.
Variables:
COLOR_SIZE: named constant set to 20.
first_color: character array containing the first color.
second_color: character array containing the second color.
Validation:
Check that both colors are red, blue, or yellow.
Display an error if either color is invalid.
Comparisons:
Use strcmp() to compare character arrays.
Check whether the colors are identical.
Check all three color combinations in both possible orders.
Output:
Purple for red and blue.
Orange for red and yellow.
Green for blue and yellow.
The original color if both valid colors are identical.
An error message for invalid colors.
Tests planned:
All three color combinations.
Reversed color combinations.
Identical primary colors.
Invalid first and second colors.

Test Records

