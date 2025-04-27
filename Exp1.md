EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Name: VISHNU KM

Reg.no: 212223240185

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
#include<stdio.h>
struct vaccine
{
    int age;
    char name[20];
    
}v;
int main()
{
    
    scanf("%d%s",&v.age,v.name);
    printf("Age:%d\nName:%s\n",v.age,v.name);
    if(v.age>6)
    {
        printf("Eligibility:Yes!");
    }
    else
    {
        printf("Eligibility:No!");
    }
}

```
Output:
![Screenshot 2025-04-26 205517](https://github.com/user-attachments/assets/b874adc0-d1f0-48f1-9853-f8d2f4e4916a)

![Screenshot 2025-04-26 205541](https://github.com/user-attachments/assets/b8a310ea-ce6a-4945-9393-409f5fbacb31)

Result:
Thus, the program is verified successfully.
