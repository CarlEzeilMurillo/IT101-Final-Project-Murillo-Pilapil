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

## PSUEDO-CODE

# MAIN PROGRAM

**START**

1. Set `again = 'Y'`.

2. WHILE `again = 'Y'`:

   - Display the Main Menu:
     1. Pattern Generator
     2. Pascal's Triangle
     3. Grade Calculator & Evaluator
     4. Palindrome Checker

   - Ask the user to enter their choice.
   - Read `choice`.

   **IF** `choice = 1`:
   - Go to Pattern Generator.

   **ELSE IF** `choice = 2`:
   - Go to Pascal's Triangle.

   **ELSE IF** `choice = 3`:
   - Go to Grade Calculator & Evaluator.

   **ELSE IF** `choice = 4`:
   - Go to Palindrome Checker.

   **ELSE**:
   - Display "Invalid Option, Try Again."

   **END IF**

   - IF `choice` is between 1 and 4:
     - Ask "Do you want to try another operation? (Y/N)"
     - Read `again`.

     - WHILE `again` is not 'Y' AND `again` is not 'N':
       - Display "Invalid Input, Please Enter Y or N."
       - Ask the user again.
       - Read `again`.
     - END WHILE

3. END WHILE

4. Display "Thank You!"

**END**

---

## 1. PATTERN GENERATOR

1. Ask the user to enter the pattern size `n`.
2. Display the Pattern Selection Menu:
   - 1. Right Triangle
   - 2. Square
   - 3. Isosceles Triangle
   - 4. Inverted Right Triangle
   - 5. Christmas Tree
3. Ask the user to select a pattern.
4. Read `patternChoice`.

**IF** `patternChoice = 1`:

- FOR `row = 1` TO `n`:
  - FOR `column = 1` TO `row`:
    - Print `*` without moving to a new line.
  - END FOR
  - Move to the next line.
- END FOR

**ELSE IF** `patternChoice = 2`:

- FOR `row = 1` TO `n`:
  - FOR `column = 1` TO `n`:
    - Print `*` without moving to a new line.
  - END FOR
  - Move to the next line.
- END FOR

**ELSE IF** `patternChoice = 3`:

- FOR `row = 1` TO `n`:
  - FOR `column = 1` TO `n - row`:
    - Print a space.
  - END FOR
  - FOR `column = 1` TO `2 * row - 1`:
    - Print `*` without moving to a new line.
  - END FOR
  - Move to the next line.
- END FOR

**ELSE IF** `patternChoice = 4`:

- FOR `row = 1` TO `n`:
  - FOR `column = 1` TO `n - row + 1`:
    - Print `*` without moving to a new line.
  - END FOR
  - Move to the next line.
- END FOR

**ELSE IF** `patternChoice = 5`:

- FOR `tier = 1` TO `3`:
  - FOR `row = 1` TO `n`:
    - FOR `column = 1` TO `n - row`:
      - Print a space.
    - END FOR
    - FOR `column = 1` TO `2 * row - 1`:
      - Print `*` without moving to a new line.
    - END FOR
    - Move to the next line.
  - END FOR
- END FOR

- FOR `column = 1` TO `n - 2`:
  - Print a space.
- END FOR
- Print `***` for the trunk.

**ELSE**:

- Display "Invalid Option, Try Again."
- Return to the Pattern Selection Menu.

**END IF**

Return to the Main Program.

---

## 2. PASCAL'S TRIANGLE

1. Ask the user to enter the number of rows `n`.
2. FOR `row = 0` TO `n - 1`:

   - Print `n - row - 1` spaces to align the triangle.

   - FOR `column = 0` TO `row`:

     - Calculate the value using:

       `value = FACTORIAL(row) / (FACTORIAL(column) * FACTORIAL(row - column))`

     - Print `value` followed by a space.

   - END FOR

   - Move to the next line.

3. END FOR

4. Display Pascal's Triangle.

Return to the Main Program.

---

## 3. GRADE CALCULATOR & EVALUATOR

1. Ask the user to enter their Prelim Grade.
2. Read `prelim`.
3. Ask the user to enter their Midterm Grade.
4. Read `midterm`.
5. Ask the user to enter their Pre-Final Grade.
6. Read `preFinal`.
7. Ask the user to enter their Final Grade.
8. Read `final`.

9. Calculate the average:

   `average = (prelim + midterm + preFinal + final) / 4`

10. Display the calculated average.

11. Check the average:

   **IF** `average >= 75`:
   - Display "PASS".

   **ELSE**:
   - Display "FAIL".

   **END IF**

Return to the Main Program.

---

## 4. PALINDROME CHECKER

1. Ask the user to enter a single word.
2. Read `word`.
3. Find the length of the word and store it in `length`.
4. Set `first = 0`.
5. Set `last = length - 1`.
6. Set `isPalindrome = TRUE`.

7. WHILE `first < last` AND `isPalindrome = TRUE`:

   - Compare `word[first]` with `word[last]`.

   - **IF** `word[first]` is equal to `word[last]`:
     - Increase `first` by 1.
     - Decrease `last` by 1.

   - **ELSE**:
     - Set `isPalindrome = FALSE`.

   - **END IF**

8. END WHILE

9. Check the result:

   **IF** `isPalindrome = TRUE`:
   - Display "The word is a palindrome."

   **ELSE**:
   - Display "The word is not a palindrome."

   **END IF**

Return to the Main Program.

---

## FACTORIAL PROCEDURE

Used by Pascal's Triangle to calculate its values.

**FUNCTION FACTORIAL(number)**

1. Set `result = 1`.
2. FOR `i = 1` TO `number`:
   - Set `result = result * i`.
3. END FOR
4. Return `result`.

**END FUNCTION**

## CODE

#include <stdio.h>
#include <string.h>

int main() {

    int choice, patternChoice;
    int n, row, column, tier;
    int rows;
    int first, last, isPalindrome;
    int again = 'Y';

    float prelim, midterm, preFinal, finalGrade, average;
    long long value;
    char word[100];

    do {

        // MAIN MENU
        printf("\n===== IT101 FINAL PROJECT =====\n");
        printf("1. Pattern Generator\n");
        printf("2. Pascal's Triangle\n");
        printf("3. Grade Calculator & Evaluator\n");
        printf("4. Palindrome Checker\n");
        printf("===============================\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        // OPTION 1: PATTERN GENERATOR
        if (choice == 1) {

            printf("\n===== PATTERN GENERATOR =====\n");
            printf("Enter pattern size: ");
            scanf("%d", &n);

            // PATTERN SELECTION MENU
            do {
                printf("\n===== PATTERN MENU =====\n");
                printf("1. Right Triangle\n");
                printf("2. Square\n");
                printf("3. Isosceles Triangle\n");
                printf("4. Inverted Right Triangle\n");
                printf("5. Christmas Tree\n");

                printf("Select a pattern: ");
                scanf("%d", &patternChoice);

                if (patternChoice < 1 || patternChoice > 5) {
                    printf("Invalid Option, Try Again.\n");
                }

            } while (patternChoice < 1 || patternChoice > 5);

            // RIGHT TRIANGLE
            if (patternChoice == 1) {

                for (row = 1; row <= n; row++) {
                    for (column = 1; column <= row; column++) {
                        printf("*");
                    }
                    printf("\n");
                }
            }

            // SQUARE
            else if (patternChoice == 2) {

                for (row = 1; row <= n; row++) {
                    for (column = 1; column <= n; column++) {
                        printf("*");
                    }
                    printf("\n");
                }
            }

            // ISOSCELES TRIANGLE
            else if (patternChoice == 3) {

                for (row = 1; row <= n; row++) {

                    for (column = 1; column <= n - row; column++) {
                        printf(" ");
                    }

                    for (column = 1; column <= (2 * row - 1); column++) {
                        printf("*");
                    }

                    printf("\n");
                }
            }

            // INVERTED RIGHT TRIANGLE
            else if (patternChoice == 4) {

                for (row = 1; row <= n; row++) {
                    for (column = 1; column <= n - row + 1; column++) {
                        printf("*");
                    }
                    printf("\n");
                }
            }

            // CHRISTMAS TREE
            else if (patternChoice == 5) {

                // Print three triangle tiers
                for (tier = 1; tier <= 3; tier++) {

                    for (row = 1; row <= n; row++) {

                        for (column = 1; column <= n - row; column++) {
                            printf(" ");
                        }

                        for (column = 1; column <= (2 * row - 1); column++) {
                            printf("*");
                        }

                        printf("\n");
                    }
                }

                // Print the trunk
                for (column = 1; column <= n - 2; column++) {
                    printf(" ");
                }

                printf("***\n");
            }
        }

        // OPTION 2: PASCAL'S TRIANGLE
        else if (choice == 2) {

            printf("\n===== PASCAL'S TRIANGLE =====\n");
            printf("Enter number of rows: ");
            scanf("%d", &rows);

            for (row = 0; row < rows; row++) {

                // Print spaces for alignment
                for (column = 0; column < rows - row - 1; column++) {
                    printf("  ");
                }

                value = 1;

                // Calculate and print values in each row
                for (column = 0; column <= row; column++) {

                    printf("%4lld", value);

                    value = value * (row - column) / (column + 1);
                }

                printf("\n");
            }
        }

        // OPTION 3: GRADE CALCULATOR & EVALUATOR
        else if (choice == 3) {

            printf("\n===== GRADE CALCULATOR =====\n");

            printf("Enter Prelim Grade: ");
            scanf("%f", &prelim);

            printf("Enter Midterm Grade: ");
            scanf("%f", &midterm);

            printf("Enter Pre-Final Grade: ");
            scanf("%f", &preFinal);

            printf("Enter Final Grade: ");
            scanf("%f", &finalGrade);

            // Calculate the average
            average = (prelim + midterm + preFinal + finalGrade) / 4;

            printf("\nYour Average: %.2f\n", average);

            // Evaluate the grade
            if (average >= 75) {
                printf("RESULT: PASS\n");
            }
            else {
                printf("RESULT: FAIL\n");
            }
        }

        // OPTION 4: PALINDROME CHECKER
        else if (choice == 4) {

            printf("\n===== PALINDROME CHECKER =====\n");

            printf("Enter a word: ");
            scanf("%99s", word);

            // Get the length of the word
            int length = strlen(word);

            // Set the first and last positions
            first = 0;
            last = length - 1;

            isPalindrome = 1;

            // Compare characters until they meet in the middle
            while (first < last && isPalindrome == 1) {

                if (word[first] == word[last]) {

                    first++;
                    last--;

                }
                else {

                    isPalindrome = 0;

                }
            }

            // Display the result
            if (isPalindrome == 1) {
                printf("The word is a palindrome.\n");
            }
            else {
                printf("The word is not a palindrome.\n");
            }
        }

        // INVALID MAIN MENU OPTION
        else {

            printf("\nInvalid Option, Try Again.\n");

        }

        // TRY AGAIN MENU
        if (choice >= 1 && choice <= 4) {

            do {

                printf("\nDo you want to try another operation? (Y/N): ");
                scanf(" %c", &again);

                if (again != 'Y' && again != 'y' &&
                    again != 'N' && again != 'n') {

                    printf("Invalid Input, Please Enter Y or N.\n");

                }

            } while (again != 'Y' && again != 'y' &&
                     again != 'N' && again != 'n');

        }

    } while (again == 'Y' || again == 'y');

    printf("\nThank You!\n");

    return 0;
}
