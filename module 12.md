Name: VISHNU KM

Reg.no: 212223240185

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
struct Node   
{  
char data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *p;
    while(p!=NULL)
    {
        printf("%c\n",p->data);
        p = p->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/415ce2f5-3edd-43a5-bb65-0fa8ef3e251d)



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.

Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

```
struct Node   
{  
char data[50];  
struct Node *next;  
}*head;  
void pop()  
{
    struct Node *ptr;
    if(head==NULL){
        printf("stack is empty\n");
    }
    else{
        ptr=head;
        head=ptr->next;
        free(ptr);
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/638f5471-ffa0-4fe5-ab32-dbdcce901e35)




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL,*head;
void display()
{
    struct Node *p;
    p = front;
    if(p==NULL)
    {
        printf("queue is empty\n");
    }
    else
    {
        printf("queue elements:\n");
        while(p!=NULL)
        {
            printf("%c\n",p->data);
            p=p->next;
        }
        
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/546c4461-b5a3-4195-89d1-203caeeff653)


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node *p = (struct Node *)malloc(sizeof(struct Node));
    p->data = data;
    p->next = NULL;
    if(front == NULL)
    {
        front = rear = p;
    }
    else
    {
        rear->next = p;
        rear = p;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/78a76712-5001-4966-afce-5b0c3e1912cb)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%d",front->data);
}
```

Output:

![image](https://github.com/user-attachments/assets/78517c91-a75c-457d-bc94-892370ccbd5a)


Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


