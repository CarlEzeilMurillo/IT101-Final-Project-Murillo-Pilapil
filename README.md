# IT101-Final-Project-Murillo-Pilapil
Final Project for first sem
# Algorithm

**START**

**MAIN MENU**
1. Display Menu:
   - 1. Pattern Generator
   - 2. Pascal's Triangle
   - 3. Grade Calculator & Evaluator
   - 4. Palindrome Checker
2. Ask the user to select an operation.
3. Check the selected operation.

**IF 1 is selected:**
1. Ask the user to enter the size or height of the pattern.
2. Display the Pattern Selection Menu:
   - 1. Right Triangle
   - 2. Square
   - 3. Isosceles Triangle
   - 4. Inverted Right Triangle
   - 5. Christmas Tree
3. Ask the user to select a pattern.
4. Check the selected pattern.
5. If the selection is valid, use loops to print the selected pattern using asterisks (*).
6. Otherwise, print "Invalid Option, Try Again."
END IF

**ELSE IF 2 is selected:**
1. Ask the user to enter the number of rows.
2. Set the first value of each row to 1.
3. Use loops to calculate the values of each row.
4. Display the calculated values in a triangular format.
5. Continue until the requested number of rows has been displayed.
END IF

**ELSE IF 3 is selected:**
1. Ask the user to enter their Prelim Grade.
2. Ask the user to enter their Midterm Grade.
3. Ask the user to enter their Pre-Final Grade.
4. Ask the user to enter their Final Grade.
5. Calculate the average of the four grades.
6. Display the calculated average.
7. Check if the average is 75 or higher:
   - IF yes, display "PASS".
   - ELSE, display "FAIL".
END IF

**ELSE IF 4 is selected:**
1. Ask the user to enter a single word.
2. Read the entered word.
3. Compare the first character with the last character.
4. Continue comparing characters while moving toward the middle of the word.
5. Stop if two characters do not match or the middle of the word is reached.
6. IF all characters match, display "The word is a palindrome."
7. ELSE, display "The word is not a palindrome."
END IF

**ELSE:**
1. Display "Invalid Option, Try Again."
END IF

**TRY AGAIN LOOP**
1. Ask the user: "Do you want to try another operation? (Y/N)"
2. IF the user enters Y, return to the Main Menu.
3. ELSE IF the user enters N, display an exit message and terminate the program.
4. ELSE, display "Invalid Input, Please Enter Y or N."

**END**
