## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
## Aim:
To write a C program print the lowercase English word corresponding to the number
## Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
## Program:
```
#include <stdio.h>

int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);

    switch (n) {
        case 1: printf("one\n"); break;
        case 2: printf("two\n"); break;
        case 3: printf("three\n"); break;
        case 4: printf("four\n"); break;
        case 5: printf("five\n"); break;
        case 6: printf("six\n"); break;
        case 7: printf("seven\n"); break;
        case 8: printf("eight\n"); break;
        case 9: printf("nine\n"); break;
        case 10: printf("ten\n"); break;
        case 11: printf("eleven\n"); break;
        case 12: printf("twelve\n"); break;
        case 13: printf("thirteen\n"); break;
        default: printf("greater than 13\n"); break;
    }

    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/3de30557-b3c6-40f4-bbad-919419c0ebc2)

Result:
Thus, the program is verified successfully
 
## EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
## Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
## Program:
```
#include <stdio.h>

int main() {
    char a[50];
    int i, digit, count;
    scanf("%s", a);

    for (digit = 0; digit <= 3; digit++) {
        count = 0;
        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] - '0' == digit) {
                count++;
            }
        }
        printf("%d ", count);
    }

    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/305df37d-1961-4f97-ae5b-8c57f92bf647)

## Result:
Thus, the program is verified successfully

## EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
## Aim:
To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
## Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int compare(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}

void permute(char *str, int l, int r) {
    if (l == r) {
        printf("%s\n", str);
    } else {
        for (int i = l; i <= r; i++) {
            char temp = str[l];
            str[l] = str[i];
            str[i] = temp;

            permute(str, l + 1, r);

            temp = str[l];
            str[l] = str[i];
            str[i] = temp;
        }
    }
}

int main() {
    int n;
    printf("Enter the number of strings: ");
    scanf("%d", &n);

    char **s = (char **)malloc(n * sizeof(char *));
    printf("Enter the strings:\n");
    for (int i = 0; i < n; i++) {
        s[i] = (char *)malloc(100 * sizeof(char));
        scanf("%s", s[i]);
    }

    qsort(s, n, sizeof(char *), compare);

    for (int i = 0; i < n; i++) {
        permute(s[i], 0, strlen(s[i]) - 1);
    }

    for (int i = 0; i < n; i++) {
        free(s[i]);
    }
    free(s);

    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/94b02a3d-9c6d-4d9c-88a6-00a88ed4615b)

## Result:
Thus, the program is verified successfully
 
## EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.
## Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
## Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
## Program:
```
#include <stdio.h>

int main() {
    int n, i, j, min, len;
    scanf("%d", &n);
    len = n * 2 - 1;

    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {
            int top = i;
            int left = j;
            int right = (len - 1) - j;
            int bottom = (len - 1) - i;

            min = top < left ? top : left;
            min = min < right ? min : right;
            min = min < bottom ? min : bottom;

            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/3d7e924c-6772-4c88-a060-4839b9333821)

## Result:
Thus, the program is verified successfully

## EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

## Program:
```
#include <stdio.h>

int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result;
    result = square();
    printf("Square of the number is: %d\n", result);
    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/09183136-02a3-447f-acf2-eed36ce3448c)

## Result:
Thus, the program is verified successfully


























