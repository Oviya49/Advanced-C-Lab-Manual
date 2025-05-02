## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
## Aim:
To write a C program to create a function to find the greatest number

## Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
## Program:
```
#include<stdio.h>
int max_of_four(int n1,int n2,int n3,int n4){
    if((n1>n2)&&(n1>n3)&&(n1>n4)){
        return n1;
    }else if ((n2>n1)&&(n2>n3)&&(n2>n4)){
        return n2;
    }else if ((n3>n1)&&(n3>n2)&&(n3>n4)){
        return n3;
    }else{
        return n4;
    }
    
}
int main()
{
    int n1,n2,n3,n4;
    scanf("%d%d%d%d",&n1,&n2,&n3,&n4);
    printf("Greatest number is %d",max_of_four(n1,n2,n3,n4));
}
```
## Output:
![image](https://github.com/user-attachments/assets/79352a40-aabd-4040-9eb1-bcfbce984827)

## Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
## Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
## Program:
```
#include <stdio.h>

void calculate_the_maximum(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;

    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int a = i & j;
            int o = i | j;
            int x = i ^ j;

            if (a < k && a > max_and) max_and = a;
            if (o < k && o > max_or) max_or = o;
            if (x < k && x > max_xor) max_xor = x;
        }
    }

    printf("%d\n%d\n%d\n", max_and, max_or, max_xor);
}

int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
    return 0;
}

```
## Output:
![Screenshot 2025-05-02 110342](https://github.com/user-attachments/assets/3aaf0a05-620a-4c1b-ab3f-2ccf38d10c04)

## Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
## Aim:
To write a C program to write the logic for the requests

## Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
## Program:
```
#include<stdio.h>

int main() {
    int noshel, noque;
    scanf("%d %d", &noshel, &noque);

    int shelarr[noshel][100];
    int nobookarr[noshel];
    int i, j;

    for(i = 0; i < noshel; i++) {
        scanf("%d", &nobookarr[i]);
        for(j = 0; j < nobookarr[i]; j++) {
            scanf("%d", &shelarr[i][j]);
        }
    }

    int query, shelfNumber, bookIndex;
    for(i = 0; i < noque; i++) {
        scanf("%d", &query);

        if(query == 1) {
            scanf("%d %d", &shelfNumber, &bookIndex);
            shelfNumber--;
            if(bookIndex >= 1 && bookIndex <= nobookarr[shelfNumber]) {
                printf("Book at index %d exists on shelf %d\n", bookIndex, shelfNumber + 1);
            } else {
                printf("Book not found on shelf %d\n", shelfNumber + 1);
            }
        } else if(query == 2) {
            int newBook;
            scanf("%d", &shelfNumber);
            scanf("%d", &newBook);
            shelfNumber--;
            shelarr[shelfNumber][nobookarr[shelfNumber]] = newBook;
            nobookarr[shelfNumber]++;
            printf("Book added to shelf %d.\n", shelfNumber + 1);
        } else {
            printf("Invalid query. Please enter either 1 or 2.\n");
        }
    }

    return 0;
}

```
## Output:
![image](https://github.com/user-attachments/assets/836035d6-a39b-45de-9ab0-919bdc7b1d99)


## Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
## Aim:
To write a C program print the sum of the integers in the array.

## Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



## Program:
```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int arr[n];
    int sum=0;
    for (int i=0 ;i<n;i++){
        scanf("%d",&arr[i]);
    }
    for(int i=0;i<n;i++){
        sum+=arr[i];
    }
    printf("Sum is %d",sum);
    
}
```
## Output:
![image](https://github.com/user-attachments/assets/894d3f34-f7b9-4a71-a4e8-35950af4fcdf)

 


## Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



## Aim:

To write a C program that counts the number of words in a given sentence.

## Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



## Program:
```
#include<stdio.h>
int main()
{
char str[100];
scanf("%[^\n]",str);
int count=1;
for(int i=0;str[i]!='\0';i++)
{
if(str[i]==32)
{
count++;
}
}
printf("Total number of words in the string is :%d",count);
}

```
## Output:
![image](https://github.com/user-attachments/assets/ff8ed04b-d577-4a87-9509-efc89000b6dd)



## Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
