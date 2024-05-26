// function to check if the number is prime or not
bool Prime(int n) {
	
//if the number is one or less than one it is not prime
	
if (n <= 1) return false;
	
// Check for factors from 2 to n divided by 2
	
for (int i = 2; i <= n / 2; ++i) {
		
/*if n is divided by any number from n to n divied by 2 then the 
number  is not a prime number*/
			
if (n % i == 0) return false;
	
}
	
/*if no factors are found in the above case then the entered number is a prime number*/ 
		
return true;

}

#include<iostream>
#include<conio.h>
using namespace std;
int main() {
	
cout << "------------------------------------" << endl;
	
cout << "------Prime Number Checker----------" << endl;
	
cout << "------------------------------------" << endl;
	
while (true) {

		
//declared a variable with integer data type
		
int number;
		
cout << "Enter a number: ";
		
//will ask the user to enter a number 
		
cin >> number;
		
/*it will determine whether the entered number is prime or not using prime() function*/
		
if (Prime(number)) {
			
//if the entered number is prime display prime number and its factor 
			
cout << number << " is a prime number." << endl;
			
cout << "Factors of " << number << " are: 1 and " << number<<"." <<endl;

			
//to make it more presentable 
			cout << "---------------------------------------------------" 
<< endl;
		
}
		
//otherwise,display that the number is not prime
		
else {
			
cout << number << " is not a prime number." << endl;

			
//to make it more presentable
			
cout << "---------------------------------------------------" <<endl;
		
}
		
//declare variable to repeat the process
		
string answer, yes;
		
//prompt the user to decide whether he wants to repeat or not 
		
cout << "Do you want to perform another conversion (yes/no)";
		
//user's response
		
cin >> answer;
		
//check the response if it is not yes
		
if (answer != "yes") {
			
//if the response is not yes end the loop 
			
break;
		
}
	
}
	
return 0;
}

