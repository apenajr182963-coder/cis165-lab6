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
BMI Results
BMI 1: Inputs: Weight - 100, Height 70, Expected result should be (14.35, underweight), the actual results were the same as the expected results.
BMI 2: Inputs: Weight - 150, Height 70, Expected result should be (21.52, Optimal Weight), the actual results were the same as the expected.
BMI 3: Inputs: Weight - 200, Height 70, Expected result should be (28.68, Overweight), the actual results were the same as the expected.
BMI 4: Inputs: Weight - 150, Height 0, Expected result should be an error, the actual results were error: weight and height should be positive. 
BMI 5: Inputs: Weight - -150, Height 70, Expected result should be an error, the actual results were error: weight and height should be positive. 

Color Test Results
Color 1: Inputs: (Red, Blue), Expected result should be purple, the actual results were the same as the expected.
Color 2: Inputs: (Red, Yellow), Expected result should be orange, the actual results were the same as the expected.
Color 3: Inputs: (Blue, Yellow), Expected result should be green, the actual results were the same as the expected.
Color 4: Inputs: (Blue, Red), Expected result should be purple, the actual results were the same as the expected.
Color 5: Inputs: (Red, Red), Expected result should be Red, the actual results were the same as the expected.
Color 6: Inputs: (Orange, Blue), Expected result should be an error, the actual result were error: enter red, blue, or yellow.
Color 7: Inputs: (Red, Orange), Expected result should be an error, the actual result were error: enter red, blue, or yellow.


Explanation Questions
1. The BMI formula uses the person's weight in pounds and height in inches. It multiplies the weight by 703.0 and divides it by the height multiplied by itself. Height times height is needed because the formula requires height squared.

2. The first condition checks whether BMI is less than 18.5. The second condition checks whether BMI is less than or equal to 25.0. This means exactly 18.5 and exactly 25.0 both belong to the Optimal weight category. The order matters because the conditions are checked from top to bottom. The first condition removes all values below 18.5, so the second condition covers the entire range from 18.5 through 25.0 without gaps.

3. I check the weight and height first because neither value should be zero or negative. A zero height would cause division by zero, and negative measurements are invalid for this program. Checking first prevents an invalid calculation.

4. I classify the original BMI because rounding it first could change which category it belongs to. I use fixed and setprecision(2) only to control how the BMI appears on the screen.

5. The strcmp() function returns zero when two strings contain the same text. The == operator does not compare the contents of character arrays in the required way. That is why I use strcmp() for the color comparisons.

6. I use the OR (||) operator to check both possible orders of each color combination. I also check whether both colors are identical before checking the mixtures. If they match, the program displays the original color.

7. I check the first color and second color against all three valid primary colors. If either input does not match red, blue, or yellow, the program displays an error message instead of mixing the colors.

8. Named constants give important values a meaningful name and prevent repeated numbers from being scattered throughout the code. Result variables store calculations before they are displayed. Both practices make the programs easier to understand, test, and maintain.

