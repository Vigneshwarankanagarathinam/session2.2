a) Write a Java code with the class name, “acad,” and a method called “main.”
Hard code the program with two integers and print the sum of those two integers.

import java.util.*;

public class acad {
	public static void main(String args[])
	{
		int number1 = 25;		//assigning value for number1
		int number2 = 35;		//assigning value for number2
		number1= number1+number2;	//adding two integers
		System.out.println(number1);	//printing the output
	}
}

b) Rewrite the above code, wherein the inputs are provided by the user at
runtime and the output is printed.

import java.util.*;

public class acad {
	public static void main(String args[])
	{
		Scanner s=new Scanner(System.in);
		int number1 = s.nextInt();		//getting value for number1 from user
		int number2 = s.nextInt();		//getting value for number2 from user
		number1= number1+number2;		//adding two integers
		System.out.println(number1);	//printing the output
	}
}

c) Write a program with the method name, “sum()” that accepts two parameters from the user and print the sum of those two numbers. The output format should be:
First number is:
Second number is:
Sum is:

import java.util.Scanner;

public class acad
{
	public static int sum(int a,int b)
	{
		int d = a+b;
		return d;
	}
	public static void main(String args[])
	{
		Scanner s =new Scanner(System.in);
		int number1 = s.nextInt();		//getting value for number1 from user
		int number2 = s.nextInt();		//getting value for number2 from user
		System.out.println("First number is: "+number1);	//printing number1
		System.out.println("Second number is: "+number2);	//printing number2
		System.out.println("Sum is: "+sum(number1,number2));	//adding and printing sum of two integers
}}
d) Write a program to accept two numbers from “stdin” and find all the odd as well as even numbers present in between them.

import java.util.Scanner;

public class acad
{
	public static void main(String args[])
	{
	StringBuffer stringBuffer1 = new StringBuffer();//declaring new StringBuffer
	StringBuffer stringBuffer2 = new StringBuffer();//declaring new StringBuffer
	Scanner ss =new Scanner(System.in);
	int number1 = ss.nextInt();		//getting value for number1 from user
	int number2 =ss.nextInt();			//getting value for number2 from user
	for (int i = number1; i <= number2; i++)
	{
		if(i%2==0)
		{
			stringBuffer1.append(i);		//appending even numbers 
			stringBuffer1.append("\n");
		}
		else
		{
			stringBuffer2.append(i);		//appending odd numbers
			stringBuffer2.append("\n");
		}
	}
	System.out.println("Even numbers:");
	System.out.println(stringBuffer1.toString());
	System.out.println("Odd number:");
	System.out.println(stringBuffer2.toString());
}
}

e) Joe is scared to go to school. When her dad asked for the reason, Joe said that she was unable to complete the task given to her by her teacher. The task was to find the “first 10 multiples” of the number entered from “stdin”. 

import java.util.Scanner;

public class acad
{
	public static void main(String args[])
	{
		Scanner ss= new Scanner(System.in);
		System.out.println("Enter the number:");
		int number1 = ss.nextInt();		//getting number1 from user
		System.out.println("The "+number1+" tables is:");
		for (int i = 1; i <=10; i++)
		{
			System.out.println(number1+"x"+i+"="+i*number1);		//printing tables of number1
		}
	}
}

f) Write a program consisting the method “sum()” and demonstrate the concept of method overloading using this method.

import java.util.*;

public class acad
{
	public static void sum(int num1 , int num2)	
//overloaded method sum with integer parameters
	{
		int sum=num1+num2;
		System.out.println(sum);    //adding input numbers     
	}
	public static void sum(String st1 ,String st2)    
//overloaded method sum with string parameters
	{
		String string = st1+st2;	//adding input strings
		System.out.println(string);
	}
	public static void main(String args[])
	{
		Scanner ss= new Scanner(System.in);
		int num1 = ss.nextInt();	//getting num1 from user
		int num2 = ss.nextInt();	//getting num2 from user
		String st1 = ss.next();	//getting st1 from user
		String st2 = ss.next();	//getting st2 from user
		sum(num1,num2);		//calling method sum with integer parameters
		sum(st1,st2);		//calling method sum with string parameters
	}
}

g) Can you overload a method with the same return type? Explain your answer with proper logic.
  
  Yes we can overload method with same return type but the argument list size should be different. If this is the case that arguments are of same name as that of the other then at least the sequence of the arguments should be different.
  Method Overloading means to have two or more methods with same name in the same class with different arguments. The benefit of method overloading is that it allows you to implement methods that support the same semantic operation but differ by argument number or type.

Important Points:

1.	Overloaded methods MUST change the argument list.
2.	Overloaded methods CAN change the return type.
3.	Overloaded methods CAN declare new or broader checked exceptions.
4.	A method can be overloaded in the same class or in a subclass.

import java.util.*;

public class acad
{
	public static int sum(int num1 , int num2)
	{
		int sum=num1+num2;		//adding two given integers
		return sum;			
	}
	public static int  sum(char char1)    
	{
		int num =(int)char1;	//converting char type into int type
		return num;
	}
	public static void main(String[] args)
	{
		Scanner ss= new Scanner(System.in);
		int num1 = ss.nextInt();	//getting num1 from user
		int num2 = ss.nextInt();	//getting num2 from user
		char char1='A';				//declaring character char1
		System.out.print("Sum of the integers: ");
		System.out.println(sum(num1,num2));	
//calling method sum with integer type as input
		System.out.print("ASCII value of 'A' is: ");
		System.out.println(sum(char1));		
//calling method sum with character type as input
	}
}
  Here in the above program the method sum has the same return type but argument list is different one gives actual sum and the other gives the ASCII value of the character.

h) Write a program in Java using Arrays, which sorts the element in a descending order.

import java.util.*;
 
public class acad
{
	public static void main(String args[])
	{
		Scanner ss= new Scanner(System.in);
		Integer[] arrayInt = new Integer[10];	
//declaring an integer array of size 10
		for (int i = 0; i < 10; i++)
		{
			arrayInt[i]=ss.nextInt();		//getting array values from user 
		}
		Arrays.sort(arrayInt, Collections.reverseOrder());		
//sorting the array in descending order
		System.out.println("The given array in descending order: ");
		for (int i = 0; i < arrayInt.length; i++)
		{
			System.out.println(arrayInt[i]);	     //printing the sorted array
		}
	}
}
