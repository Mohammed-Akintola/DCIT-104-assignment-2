# DCIT-104-assignment-2 STUDENT ID-10980326
Calculating the sum of Prime numbers within a range 

// this is a c++ code that check and calculate the sume of prime numbers within a range 
#include <iostream>
using namespace std;

bool checkPrime(int numberToCheck)
{
	if(numberToCheck == 1) {
		return false;
	}
	for (int i = 2; i*i <= numberToCheck; i++) {
		if (numberToCheck % i == 0) {
			return false;
		}
	}
	return true;
}

// Method to iterate the loop from l to r
// If the current number is prime, sum the value
int primeSum(int l, int r)
{
	int sum = 0;
	for (int i = r; i >= l; i--) {

		// Check for prime
		bool isPrime = checkPrime(i);
		if (isPrime) {

			sum = sum + i;
		}
	}
	return sum;
}

int main()
{
	int l = 2, r = 43;
	cout << primeSum(l, r);
}
