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

----------------------------------------------------------------
                           ARRAYS
			   
1) sum Two(easy)

class Solution {
    public int[] twoSum(int[] nums, int target) {

        HashMap <Integer,Integer> map = new HashMap();
        // Fill this HashMap

        for(int i = 0 ; i<nums.length;i++){
            map.put(nums[i],i);
        }

        // Searching
        for(int i = 0 ; i < nums.length ;i++){ // 2, 7, 11, 15  target = 9
            int num = nums[i]; // 2
            int rem = target -  num; // remaining value 9 - 2 = 7
            if(map.containsKey(rem)){
                int index = map.get(rem);
                if(index==i)continue;
                return new int[]{i,index};

            }
        }
        return new int[]{};

        
    }
}

----------------------------------------

26. Remove Duplicates from Sorted Array

class Solution {
    public int removeDuplicates(int[] nums) {
        if(nums.length==0) return 0;
        int curr = nums[0];
        int count = 1;
        for(int i = 0 ; i < nums.length; i++){
            if(curr == nums[i]){
                continue;
            }
            else{
                nums[count] = nums[i];
                curr = nums[i];
                count+=1;
            }
        }
        return count;
        
        
    }
}









-------------------------------------------------------------------------


CHECK GRAPH IS CYCLIC OR NOT


def is_cyclic(graph):
    visited = set()  
    for vertex in graph:
        if vertex not in visited:
            if dfs(graph, vertex, visited, -1):
                return True
    return False

def dfs(graph, vertex, visited, parent):
    visited.add(vertex)
    for neighbor in graph[vertex]:
        if neighbor not in visited:
            if dfs(graph, neighbor, visited, vertex):
                return True
        elif neighbor != parent:
            return True
    return False
graph = {1: [1, -1], 2: [2, 1], 3: [3, 1],4: [],5:[5,2],6: [],7:[7,5]}
print(is_cyclic(graph))
