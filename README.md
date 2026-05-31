# 19AI304 - Fundamentals of C Programming - Even Junior - 2026

# IAPR-3 - Module 3

# Exp.1 : Calculate Age using Function (With Return Type and With Arguments)

## Aim:

To calculate the current age of a person using a function with return type and arguments.

## Algorithm:

1. Start the program.
2. Define a function cage(int num1, int num2) that calculates the difference between the current year and the birth year.
3. In the main function, initialize two integer variables:
4. num1 as the current year (2020).
5. num2 as the birth year (1983).
6. Call the function cage(num1, num2) to compute the difference.
7. Subtract 1 from the result to adjust the age according to the birth date.
8. Print the calculated age.
9. End the program.

## Program:

```c
#include <stdio.h>

int cage(int num1, int num2)
{
    int age = num1 - num2;
    return age;
}

int main()
{
    int num1 = 2020, num2 = 1983;
    int age = cage(num1, num2);
    printf("Present Age is : %d", age - 1);
    return 0;
}
```

## Output:

<img width="522" height="172" alt="502989370-6af5eb8c-7173-4980-9815-a1c4202d086e" src="https://github.com/user-attachments/assets/e0397fee-fccd-4ee7-831c-f6d7e58f6715" />

## Result:

Thus, The C program to calculate the current age of a person using a function with return type and arguments was successfully executed. 

***

# Exp.2 : Check Whether a Number is an Armstrong Number or Not

## Aim:

To check whether the entered number is an Armstrong number using loops and mathematical operations.

## Algorithm:

1. Start the program.
2. Declare variables: num, sum, count, original, and temp.
3. Read the integer number num from the user.
4. Store the value of num in original to preserve the original number.
5. Count the number of digits in num by dividing it repeatedly by 10.
6. Reassign temp = num.
7. Extract each digit of temp using modulus (% 10) and compute its power raised to the total digit count using pow().
8. Add each powered digit to sum.
9. After the loop, compare sum with original:
   * If both are equal → it is an Armstrong number.
   * Otherwise → it is not an Armstrong number.
10. Display the result.
11. End the program.

## Program:

```c
#include <stdio.h>
#include <math.h>

int main()
{
    int num, sum = 0, count = 0;
    int original, temp;

    scanf("%d", &num);
    original = num;

    for (temp = num; temp != 0; ++count)
    {
        temp = temp / 10;
    }

    for (temp = num; temp != 0; temp /= 10)
    {
        int digit = temp % 10;
        sum += pow(digit, count);
    }

    if ((int)sum == original)
    {
        printf("%d is armstrong number", original);
    }
    else
    {
        printf("%d is not a armstrong number", original);
    }

    return 0;
}
```

## Output:

<img width="765" height="167" alt="502989608-f57fb6d5-0fa0-4edd-bb3e-57219a162c97" src="https://github.com/user-attachments/assets/a431845f-06c7-46b4-aaec-7c49f4d28118" />

## Result:

Thus, The C program to check whether the entered number is an Armstrong number using loops and mathematical operations was successfully executed.

***

# Exp.3 : Print the Elements of the Last Column of an n × n Matrix

## Aim:

To read the elements of an n × n matrix and print the elements of its last column.

## Algorithm:

1. Start the program.
2. Declare a two-dimensional array a[n][n].
3. Read the value of n (the size of the matrix).
4. Use nested for loops to input all elements of the matrix.
5. After reading the matrix, use a single for loop to access the last column elements.
6. Print each element of the last column along with its position.
7. End the program.

## Program:

```c
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);
    int a[n][n];

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            scanf("%d", &a[i][j]);
        }
    }

    for (int i = 0; i < n; i++)
    {
        printf("a[%d][%d] is %d\n", i, n - 1, a[i][n - 1]);
    }

    return 0;
}
```

## Output:

<img width="731" height="310" alt="502989787-73f99ec3-7945-45ee-aed1-307c579c33ce" src="https://github.com/user-attachments/assets/aecca59a-7078-4f00-99bb-13c51dabebd2" />

## Result:

Thus, The C program to read the elements of an n × n matrix and print the elements of its last column was successfully executed.

***

# Exp.4 : Sort Elements of an Array in Ascending Order

## Aim:

To write a C program that reads elements into an array and sorts them in ascending order using the Bubble Sort algorithm.

## Algorithm:

1. Start the program.
2. Declare an integer array arr[n] and variables for loops and swapping.
3. Read the size of the array n.
4. Input n elements into the array.
5. Use Bubble Sort technique:
   * Repeat the process n-1 times.
   * Compare each pair of adjacent elements.
6. Swap them if they are in the wrong order.
7. Print the sorted array elements.
8. End the program.

## Program:

```c
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);
    int arr[n];
    int i, j, temp;

    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

## Output:

<img width="743" height="117" alt="502990053-8aec992d-5091-43ab-aa6e-2757d25496cd" src="https://github.com/user-attachments/assets/e67abe44-bcb5-47bb-b27d-42e0c56c5749" />

## Result:

Thus, The C program to reads elements into an array and sorts them in ascending order using the Bubble Sort algorithm was successfully executed.

***

# Exp.5 : Count Even and Odd Numbers in an Array

## Aim:

To write a C program that reads an array of integers and counts the number of even and odd elements using loops.

## Algorithm:

1. Start the program.
2. Declare variables for array size n, counter variables count (for even) and acount (for odd).
3. Input the size of the array n.
4. Read n integers into the array arr.
5. Use a loop to traverse each element:
   * If the element is divisible by 2, increment the even counter.
   * Otherwise, increment the odd counter.
6. Display the count of even and odd numbers.
7. End the program.

## Program:

```c
#include <stdio.h>

int main()
{
    int n, i, count = 0, acount = 0; // initialize acount = 0 to avoid garbage value
    scanf("%d", &n);

    int arr[n];

    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }

    for (i = 0; i < n; i++)
    {
        if (arr[i] % 2 == 0)
        {
            count++;
        }
        else
        {
            acount++;
        }
    }

    printf("Even numbers: %d\n", count);
    printf("Odd numbers: %d\n", acount);
    return 0;
}
```

## Output:

<img width="586" height="138" alt="502990261-b2954207-3da5-44fd-beee-1dba311649bd" src="https://github.com/user-attachments/assets/c9c12d5e-d899-4e8e-b82e-eb4dc4aacd18" />

## Result:

Thus, The C program to reads an array of integers and counts the number of even and odd elements using loops was successfully executed.
