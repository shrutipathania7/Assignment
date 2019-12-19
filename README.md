# ASSIGNMENT

NAME - _**SHRUTI PATHANIA**_
BRANCH - _**CSE (B)**_
ROLL NO. - _**1915075**_

# !!! . . . PPS ASSIGNMENT . . . !!!

#### Q1. Write a program to add two numbers ?
```c 
 #include<stdio.h>
int main()
{
int a=100,b=120;
int sum;
sum=a+b;
printf("sum=%d",sum);
return 0;
}
```
#### Q2. Write a program to print the table using for loop ?
```c 
#include<stdio.h>
int main()
{
int i,result;

for(i=1;i<=10;i++)
{
result=i*2;
printf("%d\n",result);
}
return 0;
}
```
#### Q3. Write a program to check whether the numbers is armstrong or not ?
```c 
#include<stdio.h>
int main()
{
int n,r,c,sum=0,temp;
printf(" Enter n value:");
scanf("%d",&n);
temp=n; 
while(n>0)    
{
r=n%10;
c=r*r*r;
sum=sum+c;
n=n/10;
}
n=temp;
if(n==sum)
printf("armstrong no.");
else
printf("Not an armstrong no:");
return 0;            
}
```
#### Q4. Write to program to find the average of 'n' numbers ?
```c
#include<stdio.h>
void main()     
{
        int n;
        float sum=0;
        printf("enter number of elements \n");

        scanf("%d",&n);
        int a[n];
        printf(" now enter %d elements\n",n);
        for(int i=1;i<=n;i++)
        {       
                scanf("%d",&a[i]);
                sum+=a[i];
        }
        float avg;
        avg = sum/n;
        printf("average of %d elements is %0.2f \n",n,avg);
}
```
#### Q5. Write a program for binary search ?
```c 
#include<stdio.h>
int check(int b[],int m,int o)
{       
        int p=-1,mid;
 int f=1,l=m;
 mid=(f+l)/2;           
while(f<=l)
 {
        mid=(f+l)/2;
        if(b[mid]==o)
        {
                p=mid;
                break;
        }
        else if(o>b[mid])
        {
                f=mid+1;
        }
    else if (o<b[mid])
    {
        l=mid-1;
    }
        
}       
return p;      
} 
void main()
{       
        int n,num,index;
        printf("enter the array size\n");
        scanf("%d",&n);
        int a[n];
        printf("enter the array elements in assending order\n");
        for(int i=1;i<=n;i++)
        {
                scanf("%d",&a[i]);
        }
        printf("now enter the number which you want to check\n whether it is present or not in entered array\n");
        
        scanf("%d",&num);
        index=check(a,n,num);
        if(index==-1)   
        printf("element is not found\n");
        else
        printf("element is found at the position %d \n",index);

}

```
#### Q6. Write a program for bubble sort ?
```c 
#include<stdio.h>
int main()
{ 
int a[20],i,n,k,temp;
printf("\n Enter size of array<=19:");
scanf("%d",&n);
printf("\n Enter %d element of array\n",n);
for(i=0;i<n;i++)
{ 
scanf("%d",&a[i]);
}
for(k=0;k<n-1;k++)
{
        for(i=0;i<n-k-1;i++) 
        {
        if(a[i]>a[i+1])
        {
        temp=a[i];
        a[i]=a[i+1];
        a[i+1]=temp;
        }
        }
}
printf("\n Array element after returning\n");
for(i=0;i<n;i++)
printf("\n %d \n",a[i]);
printf("\n");
return 0;
}
```
#### Q7. Write a program to print calculator using puts ?
```c
#include<stdio.h>
int  main()
{
puts("_________________");
puts("|_______________|");
puts("| 1 | 2 | 3 |   |");
puts("|___|___|___|   |");
puts("| 4 | 5 | 6 | + |");
puts("|___|___|___|___|");
puts("| 7 | 8 | 9 | - |");
puts("|___|___|___|___|");
puts("|    0      | * |");
puts("|___________|___|");
return 0;
}
```
#### Q8. Write a program to print weekdays using switch statement ?
```c 
#include<stdio.h>
int main()
{
int code;
printf("enter weekday in number :");
scanf("%d", &code);
if (code==1)
printf("monday");
else if(code==2)
printf("Tuesday");
else if(code==3)
printf("Wednesday");
else if(code==4)
printf("Thursday");
else if(code==5)
printf("Friday");
else if (code==6)
printf("Saturday");
else if(code==7)
printf("Sunday");                                                         
else
printf("Invaild output");
return 0;
}
```
#### Q9. Write a program to find whether the number is even or odd ?
```c 
#include<stdio.h>
int main()
{
int a;
printf("enter a number");
scanf("%d",&a);
if (a%2==0)                                              
printf("a is even");
else
printf("a is odd");
return 0;
}
```
#### Q10. Write a program to find the factorial of a number ?
```c 
#include<stdio.h>
int main()
{
int fct=1,num,i;
printf(" Enter any number:");                 
scanf("%d",&num);                                 
if(num==0)
fct=1;
else
{                                                                        
for(i=1;i<=num;i++)
fct=fct*i;
}
printf("The factorial of %d is: %d\n",num,fct);
return 0;
}
```
#### Q11. Write a program for fizz buzz ?
```c
#include<stdio.h>
int main()
{
int n
for(n=1;n<=30;n++)
{
if(n%3==0 && n%5==0)
printf("FizzBuzz\n");
else if (n%3==0)
printf("Fizz\n");
else if (n%5 ==0)
printf(" Buzz\n");
else
printf("\n %d \n",n);
}
return 0;
}

```
#### Q12. Write a program to find the sum of first 100 numbers ?
```c 
#include<stdio.h>
int main()
{
int sum=0,number;
number=1;
while(number<=100)
{
sum+=number;
number++;
}
printf("sum of first 100 positive integer number=%d\n",sum);
return 0;
}
```
#### Q13. Write a program to find gcd of numbers ?
```c
#include<stdio.h>
int main()
{
int m,n,r=1;
printf("\n Enter value for m,n:");
scanf("%d%d", &m,&n);
while(r!=0)
{
r= n%m;
n= m;
m= r;
}
printf("\n GCD=%d\n",m);
return(0);
}
```
#### Q14. Write aprogram to find the greater of 2 numbers ?
```c 
#include<stdio.h>
int main()
{
 int a,b;
printf("Enter any 2 number:");
scanf("%d %d",&a,&b);
if(a>b)
{
printf("a is grater");
}
else
{
printf("b is greater");
}
return 0;
}
```
#### Q15. Write a program to find the greater of 3 numbers ?
```c 
 #include<stdio.h>
int greater(int a,int b,int c);
int main(){
	int x,y,z;
	scanf("%d %d %d",&x,&y,&z);
          greater(x,y,z);
	  return 0;
}
int greater(int a,int b,int c){
	printf("Greater no is:\n");
	if(a>b && a>c){
		printf("%d\n",a);
	}
	else if(b>a && b>c){
		printf("%d\n",b);
	}
	else
		printf("%d\n",c);
}
```
#### Q16. Write a program to find whether the year is leap year or not ?
```c 
#include<stdio.h>
int main()
{
int year;
printf("Enter the value of year");
scanf("%d",&year);
if(year%4==0)
printf("The year is Leap \n");
else
 printf("\n The year is not leap \n");
return 0;
}
```
#### Q17. Write a program for linear search ?
```c 
#include<stdio.h>
int main()
{
int array[100],i,n,search;
printf("\n Enter size of array\n");
scanf("%d",&n);
printf("Enter the element of array \n");                                    
for(i=0;i<n;i++)
scanf("%d",&array[i]);
printf("\n Enter the number to be search\n");
scanf("%d",&search);
for(i=0;i<n;i++)
{
if(array[i]==search)                                                      
printf("Search is successful\n");
else
printf("Search is unsuccessful\n");
}
return 0;
} 
```
#### Q18. Write a program for matric addition ?
```c 
#include<stdio.h>
void main()
{
int a[10][10],b[10][10],c[10][10];
int n,m,i,j;
printf("Enter size of matrix A as m,n:");
scanf("%d %d",&m,&n);
printf("\n Enter element of matrix A row wise\n",m*n);
for(i=0;i<m;i++)
{
 for(j=0;j<n;j++)
 {
 scanf("%d",&a[i][j]);
 }
}
printf("Enter size of B as m,n:");
scanf("%d %d",&m,&n);
printf("\n Enter element of matrix B row wise\n",m*n);
for(i=0;i<m;i++)
{
 for(j=0;j<n;j++)
 {
scanf("%d",&b[i][j]);
 }
}
for(i=0;i<m;i++)
{
 for(j=0;j<n;j++)                                        
 {
 c[i][j]=a[i][j]+b[i][j];
 }
}
printf("The sum of two matrices is:");
for(i=0;i<m;i++)
{
 for(j=0;j<n;j++)
 {
 printf("%d \n",c[i][j]);
 }
printf("\n");
}
}
```
#### Q19. Write a program  to find transpose of a matric ?
```c
#include<stdio.h>
void main()
{
int a[10][10],b[10][10];
int n,m,i,j;
printf("Enter size of matrix A as m,n:");
scanf("%d %d",&m,&n);
printf("\n Enter element of matrix A row wise\n",m*n);
        for(i=0;i<m;i++)
        {
        for(j=0;j<n;j++)
        {
        scanf("%d",&a[i][j]);
        }
        }
        for(i=0;i<m;i++)
        {
        for(j=0;j<n;j++)
        {
        b[j][i]=a[i][j];
        }
        }
printf("\n Transpose is\n");
for(i=0;i<n;i++)
{
for(j=0;j<m;j++)
{
printf("%d ",b[i][j]);
}
printf("\n");
}
}       
```
#### Q20. Write a program to find the sum of digits of a number ?
```c 
#include<stdio.h>
int main()
{
int sum=0,digit;
int number,temp;
printf("enter any positive number:");
scanf("%d",&number);
temp=number;
while(temp>0)
{
digit=temp%10;
temp/=10;
sum+=digit;
}
printf("\n sum of digit of %d=%d\n",number,sum);
return 0;
}
```
#### Q21. Write a program to check whether the number is palindrome or not ?
```c 
#include<stdio.h>
int main()
{
int sum=0,digit;
int number,temp;
printf("\n Enter any positive integer no:");
scanf("%d",&number);
temp=number;
while(temp>0)
{
digit=temp%10;
temp/=10;
sum=sum*10+digit;
}
if(number==sum)
printf("\n %d is a pallindrome number\n",number);
else
printf("\n %d is not a pallindrome number\n",number);
return 0;
}
```
#### Q22. Write a program swap two numbers using call by value method ?
```c 
#include<stdio.h>
void swap(int a,int b);
void main()
{
int x,y;
printf("\n Enter value of x:");                 //10
scanf("%d",&x);                                 //12
printf("\n Enter value of y:");
scanf("%d",&y);
printf("\n Befor calling swap funtion\n");               
printf("\n value of x=%d , value of y=%d\n",x,y);
swap(x,y);
printf("\n After returning from swap function");
printf("\n value of x=%d , value of y=%d\n",x,y);
}
void swap(int a,int b)
{                                                                        
int temp;
printf("\n value of a=%d , value of b=%d before swap\n",a,b);
temp=a;
a=b;
b=temp;
printf("\n value of a=%d , value of b= %d after swap\n",a,b);
}
```
#### Q23. Write a program to swap two number using call by refrence method ?
```c 
#include<stdio.h>
void swap(int*a,int*b);
void main()
{
int x,y;
printf("\n Enter value of x:");
scanf("%d",&x);
printf("\n Enter value of y:");
scanf("%d",&y);
printf("\n Before calling swap function\n");
printf("\n Value of x = %d ,value of y = %d\n",x,y);
swap(&x,&y);
printf("\n after returning from swap function\n");
printf("\n Value of x = %d,value of y = %d\n",x,y);                       
}
void swap(int*a,int*b)
{
int temp;
printf("\n Inside the function\n");
printf("\n Value of a = %d,value of b = %d before swap\n",*a,*b);
temp=*a;
*a=*b;
*b=temp;
printf("\n Value of *a = %d,value of *b = %d after swap\n",*a,*b);
}
```
#### Q24. Write a program to enter the details of employees using structures ?
```c 
#include<stdio.h>
#include<string.h>
struct employee
{
int code;
char name[25];
char department[25];
float salary;
};
void main()
{
struct employee aemployee;
printf("Enter Employee's code:");
scanf("%d",&aemployee.code);
printf("Enter Employee's name:");
scanf("%s",aemployee.name);
printf("Enter Employee's department:");
scanf("%s",aemployee.department);
printf("Enter employee's salary:");
scanf("%f",&aemployee.salary);
printf("\n\n Particulars of employee are:");
printf("\n Employee's code:%d",aemployee.code);
printf("\n Employee's name:%s",aemployee.name);
printf("\n Employee's department:%s",aemployee.department);
printf("\n Employee's salary:%f\n",aemployee.salary);
}
```
#### Q25. Write a program to find the fractions using structures ?
```c     
#include<stdio.h>
struct fraction
{       
        int num;
        int den;
};      
int main()
{       
        int rnum,rden;
        struct fraction f1,f2;
        printf("Enter numerator and denominator of first fraction\n");
        scanf("%d%d",&f1.num,&f1.den);
        printf("Enter numerator and denominator of second fraction\n");
        scanf("%d%d",&f2.num,&f2.den);
        rnum=f1.num*f2.num;
        rden=f1.den*f2.den;
        printf("\n Product is :%d/%d\n",rnum,rden);
return 0;
}
```





