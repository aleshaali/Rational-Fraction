# Rational-Fraction
This project utilizes a class "rational" that allows us to manipulate fractions. It also utilizes overloaded operators
/*  This rational class practice basics of defining and using class.
 */
//this file enables us to implement the class rational, asking the user to enter which overloaded operator they would like to test for class rational
#include <iostream>
#include <stdlib.h>
#include "rational8.h"
#include <string>
using namespace std;

int main ()
{
    char cont; //Will ask the user if they would like to test another operator
    rational a;//to be entered by the user
    rational b;//to be entered by the user
    rational c;//set by me depending on what the user enters
    string choice;//operator the user wants to test

    do {
        cout << "Enter the operator you want to test for rational class (+,-,*,/,==,!=,<,<=,>=,>, and -1 for negation). " <<endl;
        cin >> choice;
        cout << "Testing " << choice << endl;
        switch (choice[0])//checking first character of the string
        {
            case '+':
                if (choice != "+")
                {
                    cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }
                else
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    c = a+b;
                    cout <<"The sum of op1 and op2 is: ";
                    cout << c;
                    cout <<endl;
                }

                break;

            case '-':
                if (choice == "-1")
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    c=-a;
                    cout << "-op1 = " << c << endl;
                }
                else if (choice != "-")
                {
cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }
                 else
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    c = a-b;
                    cout <<"The difference of op1 and op2 is: ";
                    cout << c;
                    cout <<endl;
                }

                break;

            case '*':
                if (choice!="*")
                {
                    cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }

                else
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    c = a*b;
                    cout <<"The product of op1 and op2 is: ";
                    cout << c;
                    cout <<endl;
                }

                break;

            case '/':
                if (choice!="/")
                 {
                    cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }
                else
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;c = a/b;
                    cout <<"The quotient of op1 and op2 is: ";
                    cout << c;
                    cout <<endl;
                }

                break;

            case '=':
                if (choice == "==")
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    if (a==b)
                        cout << a << "and " << b << " are equal." << endl;
                    else
                        cout << a << " and " << b << " are not equal." << endl;
                }

                else
                {
                    cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }

                break;

            case '!':
                if (choice == "!=")
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                     cin >> b;

                    if (a!=b)
                        cout << a << " and " << b << " are not equal." << endl;
                    else
                        cout << a << " and " << b << " are equal." << endl;
                }

                else
                {
                         cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }

                break;

            case '<':if (choice == "<=")
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    if (a <= b)
                        cout << a << " is less than or equal to " << b << endl;
                    else
                        cout << a << " is greater than " << b << endl;
                }
                else if (choice!="<")
                {
                    cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }
                else
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    if (a < b)
                        cout << a << " is less than " << b << endl;
                    else
                        cout << a << " is greater than or equal to " << b << endl;
                }
               break;

            case '>':
                if (choice == ">=")
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    if (a >= b)
                       cout << a << " is greater than or equal to " << b << endl;
                    else
                        cout << a << " is less than " << b << endl;
                }
                else if (choice!=">")
                {
                    cout << "Invalid choice. Aborting program. " << endl;
                    exit (1);
                }
                else
                {
                    cout <<"Enter op1 (in the format of p/q):";
                    cin >> a;
                    cout <<"Enter op2 (in the format of p/q):";
                    cin >> b;

                    if (a>b)
                        cout << a << " is greater than " << b << endl;
                    else
                        cout << a << " is less than or equal to " << b << endl;
                }

                break;

            default:
                cout << "Invalid choice. Aborting program. " << endl;
                exit (1);
        }
        cout << "Want to try again? (Y/N)" << endl;
        cin >> cont;
    } while (cont == 'Y' || cont == 'y');//do until the user says no

    cout << "Exiting Program... Have a good day!" << endl;
    return 0;

}
