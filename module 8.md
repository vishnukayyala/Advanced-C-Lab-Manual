EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

Name:VISHNU KM

Reg.no: 212223240185

Aim:
To write a C program print the lowercase English word corresponding to the number

Algorithm:
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
 
Program:
```
#include<stdio.h>
int main()
{
    int a;
    printf("Enter a number:");
    scanf("%d",&a);
    if(a>=71 && a<=79)
    {
        switch(a)
        {
            case 71:
            printf("seventy one");
            break;
            
            case 72:
            printf("seventy two");
            break;
            
            case 73:
            printf("seventy three");
            break;
            
            case 74:
            printf("seventy four");
            break;
            
            case 75:
            printf("seventy five");
            break;
            
            case 76:
            	printf("seventy six");
            	break;
            case 77:
            	printf("seventy seven");
            	break;
            case 78:
            	printf("seventy eight");
            	break;
            case 79:
            	printf("seventy nine");
            	break;
            
        }
    }
    else
    {
        printf("Greater than 79");
    }
}
```


Output:


![Screenshot 2025-04-26 223943](https://github.com/user-attachments/assets/13998f0f-4637-48c0-834c-a80a8e08b0c4)

![Screenshot 2025-04-26 224015](https://github.com/user-attachments/assets/61b473de-19c7-4780-9a9c-d31e68b1e6ef)




Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

```
#include <stdio.h>

int main() {
    char a[50];
    int h, i, c;

    printf("Enter the string of digits: ");
    scanf("%s", a);

    for (h = 0; h <= 9; h++) {
        c = 0;
        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] == (h + '0')) { 
                c++;
            }
        }

        printf("%d ", c);
    }

    return 0;
}

```

Output:

![image](https://github.com/user-attachments/assets/88e32f51-932f-4fff-a971-afe49533729a)


Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
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
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int next_permutation(int n, char **s)
{

    int k = -1;
    for (int i = 0; i < n-1; i++) {
        if (strcmp(s[i], s[i+1]) < 0)
            k = i;
    }
    if (k == -1) return 0; 

    int l = -1;
    for (int i = k+1; i < n; i++) {
        if (strcmp(s[k], s[i]) < 0)
            l = i;
    }

    char *tmp = s[k];
    s[k] = s[l];
    s[l] = tmp;

    int i = k+1, j = n-1;
    while (i < j) {
        tmp = s[i];
        s[i++] = s[j];
        s[j--] = tmp;
    }

    return 1; 
}

int main()
{
	char **s;
	int n;
	scanf("%d", &n);
	s = calloc(n, sizeof(char*));
	for (int i = 0; i < n; i++)
	{
		s[i] = calloc(11, sizeof(char));
		scanf("%s", s[i]);
	}
	do
	{
		for (int i = 0; i < n; i++)
			printf("%s%c", s[i], i == n - 1 ? '\n' : ' ');
	} while (next_permutation(n, s));
	for (int i = 0; i < n; i++)
		free(s[i]);
	free(s);
	return 0;
}
```



Output:
![image](https://github.com/user-attachments/assets/2a42e40e-c0b7-44aa-88f3-ae2e7ac159d4)

![Screenshot 2025-04-26 233518](https://github.com/user-attachments/assets/77f56d19-b3be-4cec-bbf6-432c0c3a5994)





Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
int single(int x,int y)
{
    return x>y?x:y;
}
int main()
{
    int a;
    scanf("%d",&a);
    for(int i=0;i<(a*2)-1;i++){
        for(int j=0;j<(a*2)-1;j++)
        {
         printf("%d ",single(abs(a-i-1),abs(a-j-1))+1);   
        }printf("\n");
    }
}

```


Output:
![image](https://github.com/user-attachments/assets/9e3c07a7-b71a-4e78-8d58-645854814cb6)


![image](https://github.com/user-attachments/assets/7b3cf4af-be2b-41ed-a078-4b1715a7f2c0)

Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

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

Program:
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

    printf("Square of the number: %d\n", result);

    return 0;
}

```


Output:

![image](https://github.com/user-attachments/assets/09ece90a-d42d-49cf-90dc-c80239616845)




Result:
Thus, the program is verified successfully



























