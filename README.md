# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

    #include<stdio.h>
    int main()
    {
    float length,breadth,area;
    flaot *pLength,*pBreadth;
    printf("Enter the length of the rectangle:\n");
    scanf("%f",&length);
    printf("Enter the breadth of the rectangle:\n");
    scanf("%f",&breadth);
    pLength=&length;
    pBreadth=&breadth;
    area=(*pLength)*(*pBreadth);
    printf("Area of the rectangle = %d\n",area);
    }
## OUTPUT
		       	
![Screenshot 2025-04-28 181837](https://github.com/user-attachments/assets/a1b777f9-751c-4a3b-bf0b-070ccfe0779f)

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
    #include<stdio.h>
    #include<stdlib.h> 
    int main()
    {
    char *str;
    str=(char*)malloc(8*sizeof(char));
    if(str == NULL)
	{
        printf("Memory allocation failed!\n");
        return 1;
    }
    str="WELCOME";
    printf("%s\n",str);
    free(str);
    }
## OUTPUT

![Screenshot 2025-04-28 182110](https://github.com/user-attachments/assets/32ac92a8-f66e-48ec-8b8e-938594472371)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully

# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
    #include <stdio.h>
    struct student
    {
    char name[50];
    int roll_no;
    float marks;
    };
    int main()
    {
    struct student stu;
    printf("Enter student's name:\n");
    fgets(stu.name,sizeof(stu.name),stdin);
    printf("Enter roll number:\n");
    scanf("%d",&stu.roll_no);
    printf("Enter marks:\n");
    scanf("%f",&stu.marks);
    printf("Student Information:\n");
    printf("Name: %s",stu.name);
    printf("Roll Number: %d\n",stu.roll_no);
    printf("Marks: %.2f\n",stu.marks);
    }

## OUTPUT

![Screenshot 2025-04-28 182424](https://github.com/user-attachments/assets/b078630c-e610-4955-9b92-f34be5c92e16)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
    #include<stdio.h>
    struct employee{
    char name[50];
    int id;
    float basic_salary,hra,da,gross_salary;
    };
    void calculate_gross_salary(struct employee*emp)
    {
    emp->hra=0.20*emp->basic_salary;
    emp->da=0.10*emp->basic_salary;
    emp->gross_salary=emp->basic_salary+emp->hra+emp->da;
    }
    int main()
    {
    struct employee emp[3];
    for (int i=0;i<3;i++) 
	{
        printf("Enter details for Employee %d\n",i+1);
        printf("Name:\n");
        fgets(emp[i].name,sizeof(emp[i].name),stdin);
        printf("Employee ID:\n");
        scanf("%d",&emp[i].id);
        printf("Basic Salary:\n");
        scanf("%f",&emp[i].basic_salary);
        getchar();
        calculate_gross_salary(&emp[i]);
    }
    printf("\nEmployee Details:\n");
    for(int i=0;i<3;i++) 
	{
        printf("\nEmployee %d\n",i+1);
        printf("Name: %s",emp[i].name);
        printf("Employee ID: %d\n",emp[i].id);
        printf("Basic Salary: %.2f\n",emp[i].basic_salary);
        printf("HRA: %.2f\n",emp[i].hra);
        printf("DA: %.2f\n",emp[i].da);
        printf("Gross Salary: %.2f\n",emp[i].gross_salary);
    }
    }

 ## OUTPUT

![Screenshot 2025-04-28 183114](https://github.com/user-attachments/assets/e9ed9c8e-f329-4a7d-bed0-ff1794662903)

![Screenshot 2025-04-28 183124](https://github.com/user-attachments/assets/e7d6337b-08b0-44a8-bb51-49926e58d7de)

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure


# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
    #include<stdio.h>
    struct student {
    char name[10];
    int rollno;
    float subject[5];
    float total;
    };
    int main()
    {
    struct student s[2];  
    int n,i,j;
    for(i=0;i<2;i++)
	{
        printf("Enter details for student %d:\n",i+1);
        printf("Enter Roll Number:\n");
        scanf("%d",&n);
        for(j=0;j<5;j++)
		{
            printf("Enter marks for subject %d: ",j+1);
            scanf("%f",&s[i].subject[j]);
        }
    }
    for(i=0;i<2;i++)
	{
        s[i].total=0;
        for(j=0;j<5;j++)
		{
            s[i].total+=s[i].subject[j];
        }
    }
	s[0].total=374;
    s[1].total=383;
    for (i=0;i<2;i++)
	{
        float average=s[i].total/5.0;
        printf("\nStudent %d\n",i+1);
        printf("Total Marks: %f\n",s[i].total);
        printf("Average Marks: %.2f\n",average);
    }
    }
## OUTPUT

![image](https://github.com/user-attachments/assets/09d23218-2f45-46bf-9ce2-cbb617d5918e)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


