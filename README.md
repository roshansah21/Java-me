# Java-me

------------------------------------------------------------------------------------
01. Print Hello in Java

import java.util.*;
    public class Hello{
    public static void main(String[] args) {
        System.out.println("Hello");
}
}
-----------------------------------------------------------------------------------

02. Sum of Two  number 

package Java;
import java.util.Scanner;
public class SumOfTwoNum {
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		
		System.out.println("Enter the value of num1 : ");
		int num1 = sc.nextInt();
		System.out.println("Enter the value of num2 :");
        int num2 = sc.nextInt();
    System.out.println("Addition of Two numbers are "+(num1+num2));
	}
}

------------------------------------------------------------------------------------
03. Program to Find Quotient and Remainder

import java.util.Scanner;
public class QueNrem {

	public static void main(String[] args) {
		int dvd,dir;
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the dvd : ");
		dvd = sc.nextInt();
		System.out.println("Enter the dir : ");
		dir = sc.nextInt();
		int rem = dvd%dir;
		int que = dvd/dir;
		System.out.println("Remainder : "+rem+"\n"+"Quotient : "+que);
	}
}

-----------------------------------------------------------------------------------------

04. to Swap Two Numbers Without Using third variable
import java.util.Scanner;
public class SwapTwoNumber {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int a,b;
		System.out.println("Enter the value of a : ");
		a = sc.nextInt();
		System.out.println("Enter the value of b : ");
	    b = sc.nextInt();
		
		// Logical part of this code !!
		
		a = a + b;
		b = a - b;
		a = a - b;
		System.out.println("After swap : " +"\n"+a+"\n"+b);

	}
}

--------------------------------------------------------------------------------------
05. Chech Given character are Upper,Lower,special,Number

public static void main(String[] args) {
		char ch;
		
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the String : ");
		ch = sc.next().charAt(0);
	    
	    // Logical part of this code !!
	    
	    if(ch>=65 && ch<=90) {
	    	System.out.println("upper");
	    }
	    else if(ch >= 97 && ch <= 122) {
	    	System.out.println("Lower");
	    }
	    else if(ch >= 48 && ch <= 57) {
	    	System.out.println("Digit");
	    }
	    else
	    {
	    	System.out.println("Special");
	    }
	    
	}

------------------------------------------------
