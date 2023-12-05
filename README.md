//TO-DO: KeLI Cardenas
//TO-DO: 11.17.23
//CS1428 Lab
//Lab 11
//Description: this program will keep track of a dealership inventory

//****************This is the line of 80 characters in length*******************
//############Your code should not exceed the length of the above line##########


#include <iostream>
#include <iomanip>

using namespace std;

//TODO: Create your struct
struct CarDealership {
string make;
int year;
int inventory;
};
int main()
{
    const int SIZE = 3;
    CarDealership car[SIZE];
    int total = 0,
        HighestInventory = 0,
        LowestInventory = 99999;
  string Highestmake;
  string Lowestmake;

    for(int i = 0; i < SIZE; i++)
    {
        //TODO: Prompt/read car information
      cout<<"enter make:";
      cin>>car[i].make;
      cout<<"enter year:";
      cin>>car[i].year;
      cout<<"intentory:";
      cin>>car[i].inventory;
        //adds inventory of each make to the total inventory
        total += car[i].inventory;
        //TODO: Find the make with the highest inventory
        if(car[i].inventory > HighestInventory){
          HighestInventory=car[i].inventory;
      Highestmake=car[i].make;
        }
        //TODO: Find the make with the lowest inventory
      if(car[i].inventory < LowestInventory){
        LowestInventory=car[i].inventory;
         Lowestmake=car[i].make;
      }

        cout << endl << endl;
        
    }

    //TODO: output the total inventory, the make with the highest inventory,
  cout<<"total inventory:"<<total<<endl;
  cout<<"Highest inventory:"<<Highestmake<<endl;
    //and the make with the lowest inventory.
  cout<<"Lowest inventory:"<<Lowestmake<<endl;

    return 0;
}
