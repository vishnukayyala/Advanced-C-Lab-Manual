EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Name: VISHNU KM 

Reg.No: 212223240185

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include <stdio.h>
struct eligible {
    int age;
    char n[100];
};

int main() {
    struct eligible e;
    scanf("%d %s", &e.age, e.n);
    if (e.age <= 6) {
        printf("Vaccine Eligibility: No\n");
    } else {
        printf("Vaccine Eligibility: Yes\n");
    }
    printf("Details:\nAge: %d\nName: %s\n", e.age, e.n);
    return 0;
}


```
Output:
![Screenshot 2025-04-26 211823](https://github.com/user-attachments/assets/5d0a7ac3-6801-464b-afff-dbc4d28d7e20)

![Screenshot 2025-04-26 211848](https://github.com/user-attachments/assets/f91b3f97-f39f-4ac2-9d82-08ec1da3a0f9)


Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION

Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:
```
#include <stdio.h>
struct numbers {
    int a;
    int b;
};
int add(struct numbers n) {
    return n.a + n.b;
}
int main() {
    struct numbers n;
    scanf("%d %d", &n.a, &n.b);
    int result = add(n);
    printf("Sum: %d\n", result);
    return 0;
}

```

Output:

![image](https://github.com/user-attachments/assets/466a6704-72f4-4e24-9f47-eadaecf14868)




Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>  // for exit()

int main() {
    FILE *p;
    char name[100];

    printf("Enter the file name: ");
    scanf("%s", name);

    printf("Creating file '%s'...\n", name);

    p = fopen(name, "w");  // Open the file in write mode

    if (p == NULL) {
        printf("Error: Could not create the file.\n");
        return 1;  // Non-zero status for error
    }

    printf("File '%s' opened successfully.\n", name);

    fclose(p);
    printf("File '%s' closed.\n", name);

    return 0;
}

```

Output:
![image](https://github.com/user-attachments/assets/6b4ed998-7c27-4552-a099-9e296bd49fa1)


![Screenshot 2025-04-26 212558](https://github.com/user-attachments/assets/ab53cf21-9e4f-4446-90fa-8ff719b0c0ef)


![image](https://github.com/user-attachments/assets/1d8caa4d-2dba-4d39-9d9a-1c456fc25966)


Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE

Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>  // for exit()

int main() {
    FILE *p;
    char name[100], text[100];
    int num, i;

    printf("Enter the file name: ");
    scanf("%s", name);

    printf("Enter the number of strings: ");
    scanf("%d", &num);

    p = fopen(name, "w");  // Open file in write mode

    if (p == NULL) {
        printf("Error: Could not create or open the file.\n");
        return 1;  // Exit with error
    }

    printf("File '%s' opened successfully.\n", name);

    // Clear input buffer (optional, if mixing scanf and fgets)
    getchar();

    for (i = 0; i < num; i++) {
        printf("Enter string %d: ", i + 1);
        fgets(text, sizeof(text), stdin); // Read a full line (including spaces)

        fputs(text, p); // Write to file
    }

    fclose(p);

    printf("Data added successfully to '%s'.\n", name);

    return 0;
}


```
Output:

![image](https://github.com/user-attachments/assets/6887365d-4fb7-4801-83cf-d34d7a668b3a)

![image](https://github.com/user-attachments/assets/603482a4-460d-4e7f-847e-74e2347177f0)

![image](https://github.com/user-attachments/assets/01211991-46fc-425b-b150-485c3de2fc56)



Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

```
#include <stdio.h>
#include <stdlib.h>

struct subject {
    char name[100];
    int marks;
};

int main() {
    int n, i;
    struct subject *s;

    printf("Enter the number of subjects: ");
    scanf("%d", &n);

    // Dynamically allocate memory
    s = (struct subject *)malloc(n * sizeof(struct subject));

    if (s == NULL) {
        printf("Memory allocation failed.\n");
        return 1;  // Exit with error
    }

    // Input details
    for (i = 0; i < n; i++) {
        printf("Enter name of subject %d: ", i + 1);
        scanf("%s", s[i].name);

        printf("Enter marks for subject %d: ", i + 1);
        scanf("%d", &s[i].marks);
    }

    // Display details
    printf("\nSubject Details:\n");
    for (i = 0; i < n; i++) {
        printf("Subject %d: Name = %s, Marks = %d\n", i + 1, s[i].name, s[i].marks);
    }

    // Free allocated memory
    free(s);

    return 0;
}


```

Output:
![image](https://github.com/user-attachments/assets/a53f1528-11dd-4dce-96e2-082d21a110fc)


![image](https://github.com/user-attachments/assets/22a2a11b-a3e7-4468-ac9e-7b87e850d989)


Result:
Thus, the program is verified successfully
