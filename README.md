#include <iostream>
#include <string>
#include <iomanip>
#include <cstdlib>
#include<ctime>
using namespace std;
int main()
{ 
	double deposit;
	double rate = 0.05;

	// simple c++ program
	do
	{
		cout << " How much money do you want to deposit" << endl;
		cin >> deposit;
		if (cin.fail() || deposit < 0)
		{
			cout << "Invalid entry, Please try again" << endl;
			cin.clear();
			cin.ignore(INT_MAX, '\n');

		}


	} while (deposit <= 0);
		for (int  year = 1;  year <= 10 ;  year++)
		{
			double interest = deposit * rate;
			deposit = interest + deposit;

			cout << year << " you made  " << deposit<< endl;


		}

	
	system("PAUSE");
	return 0;

}
