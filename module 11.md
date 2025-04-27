EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER.

Name:VISHNU KM 

Reg.no: 212223240185

Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max(int x, int y)
{
    return (x>y)?x:y;
}
int max_of_num(int a,int b,int c,int d)
{
    int set1,set2;
    set1 = max(a,b);
    set2 = max(b,c);
    return max(set1,set2);
}
int main()
{
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    printf("%d",max_of_num(a,b,c,d));
}
```

Output:
![image](https://github.com/user-attachments/assets/5d5251b5-2f25-4c30-8707-b0047b294df4)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>
void calculate_the_maximum(int n, int k) {
    int max_and = 0;
    int max_or = 0;
    int max_xor = 0;
    for (int a = 1; a < n; a++) {
        for (int b = a + 1; b <= n; b++) {
            int and_val = a & b;
            int or_val = a | b;
            int xor_val = a ^ b;
            if (and_val < k && and_val > max_and) {
                max_and = and_val;
            }
            if (or_val < k && or_val > max_or) {
                max_or = or_val;
            }
            if (xor_val < k && xor_val > max_xor) {
                max_xor = xor_val;
            }
        }
    }
    printf("%d\n", max_and);
    printf("%d\n", max_or);
    printf("%d\n", max_xor);
}

int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
    return 0;
}

```

Output:
![image](https://github.com/user-attachments/assets/a43a1653-ff78-4366-bd0b-2a07f7e8cc71)


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS.

Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
int* total_no_of_books;
int** total_no_of_pages;
int main()
{
    int total_no_of_shelves;
    scanf("%d",&total_no_of_shelves);
    
    int total_no_of_queries;
    scanf("%d",&total_no_of_queries);
    
    total_no_of_books = (int *)malloc(sizeof(int)*total_no_of_shelves);
    total_no_of_pages = (int **)malloc(sizeof(int *)*total_no_of_shelves);
    
    for(int i=0;i<total_no_of_shelves;i++)
    {
        *(total_no_of_books + i) = 0;
    }
    while(total_no_of_queries--)
    {
        int type_of_query;
        scanf("%d",&type_of_query);
        if(type_of_query == 1)
        {
            int x,y;
            scanf("%d %d",&x,&y);
            int booksInShelf = *(total_no_of_books + x);
            *(total_no_of_pages + x) = (int*)realloc(*(total_no_of_pages+x),sizeof(int)*(booksInShelf+1));
            *(*(total_no_of_pages + x) + booksInShelf) = y;
            *(total_no_of_books + x) +=1;
        }
        else if(type_of_query == 2)
        {
            int x,y;
            scanf("%d %d",&x,&y);
            printf("%d\n",*(*(total_no_of_pages + x) + y));
        }
        else
        {
            int x;
            scanf("%d",&x);
            printf("%d\n",*(total_no_of_books + x));
        }
    }
    if(total_no_of_books)
    {
        free(total_no_of_books);
    }
    for(int i=0;i<total_no_of_shelves;i++)
    {
        if (*(total_no_of_pages + i))
        {
            free(*(total_no_of_pages + i));
        }
    }
    if(total_no_of_pages)
    {
        free(total_no_of_pages);
    }
    return 0;
}
```

Output:
![image](https://github.com/user-attachments/assets/06d6d043-843c-4085-83c9-9e28dd2606b1)


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n,*p;
    scanf("%d",&n);
    p=(int*)malloc(sizeof(int)*n);
    int sum=0;
    for(int i=0;i<n;i++)
    {
        scanf("%d",&p[i]);
        sum=sum+p[i];
    }
    printf("%d",sum);
}
```

Output:
![image](https://github.com/user-attachments/assets/816fb5b5-e337-4b7d-9700-b79a4ff927a7)

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
   #include<stdio.h>
   #include<string.h>
   int main()
   {
       char str[100];
       fgets(str,sizeof(str),stdin);
       int len=sizeof(str);
       int count=1;
        for(int i=0;i<len-1;i++){
            if(str[i]==' ')
            count++;
            
        }
        printf("Total number of words in the string is :%d",count);
       return 0;
   }
```

Output:
![image](https://github.com/user-attachments/assets/05b0cd3b-4908-41a8-ab54-fb43b365ba6a)



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
