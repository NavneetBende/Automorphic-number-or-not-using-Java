# Automorphic-number-or-not-using-Java

Automorphic number or not using Java
java program to find automorphic number or not
Check Whether Or Not the Number is an Automorphic Number in Java
Given an integer input, the Objective is to check whether the square of the number ends with the same number or not. Therefore, we’ll write a code to Check Whether or Not the Number is an Automorphic Number in Java Language.

Example
Input : 5
Output : Yes, it's an Automorphic Number
Check Whether or Not the Number is an Automorphic Number in Java
Given an integer input, the objective is to check whether or not the Number is an automorphic number or not. To do so we’ll check whether the square if the number ends with the number itself of not. For a number to be Automorphic, it’s square has to end with the number itself. Let’s implement the above mentioned logic in Java Language.

Automorphic Number
A Number that when squared ends with the number itself is known as the Automorphic Number.
Let's try and understand the concept of Automorphic Number,

Example
Input : 5
Output : 25
Explanation : Number = 5
when squared you get 25
as 25 ends with 5
From the above example, we prove that the number 5 is an Automorphic Number.
Java Code
Run
public class Main
{
	public static void main(String[] args) {
	   
	int n = 376, sq = n * n ;
    if(isAutomorphic(n) == 1)
        System.out.println("Num: "+ n + ", Square: " + sq + " - is Automorphic");
    else
        System.out.println("Num: "+ n + ", Square: " + sq + " - is not Automorphic");
	   
		
	}
	
	static int isAutomorphic(int n){
    int square = n * n;
    while(n != 0)
    {
        // means not automorphic number
        if(n % 10 != square % 10){
            return 0;
        }
        // reduce down numbers
        n /= 10;
        square /= 10;
    }
    // if reaches here means automorphic number
    return 1;
}
}
Output
Num: 376, Square: 141376 - is Automorphic
