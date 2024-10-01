/*
Bryce Lombardo and Tj Wangchuk
9/30/24
Extra: ascii art
*/
#include <iostream>
#include <string>
#include <vector>
#include <iomanip> 

using namespace std;

int main(){
    //create variables
    char continueShopping;
    double subtotal = 0.0;  
    const double salesTaxRate = 6.625 / 100;  
    int totalItems = 0;  

    do {
        //create all the variables
        int curtam; 
        int curtsize;
        int sdAm;  
        int tabletopAm;  
        int tableLegsAm; 
        string materialChoice;
        string sizeChoice;
        string legColor;
        int smallAm = 0;
        int mediumAm = 0;
        int largeAm = 0;
        int woodenAm = 0; 
        int marbleAm = 0;
        int graniteAm = 0;
        int blackLegAm = 0; 
        int brownLegAm = 0;
        int yellowLegAm = 0;
        string product;
        //start the welcome also our extra
        cout << "Welcome to IKEA!!!" << endl;
        cout << " ___      ___  __        _______       ________     " << endl;
        cout << "|\\  \\    |\\  \\|\\  \\     |\\  ___ \\     |\\   __  \\    " << endl;
        cout << "\\ \\  \\   \\ \\  \\/  /|_   \\ \\   __/|    \\ \\  \\|\\  \\   " << endl;
        cout << " \\ \\  \\   \\ \\   ___  \\   \\ \\  \\_|/__   \\ \\   __  \\  " << endl;
        cout << "  \\ \\  \\   \\ \\  \\\\ \\  \\   \\ \\  \\_|\\ \\   \\ \\  \\ \\  \\ " << endl;
        cout << "   \\ \\__\\   \\ \\__\\\\ \\__\\   \\ \\_______\\   \\ \\__\\ \\__\\ " << endl;
        cout << "    \\|__|    \\|__| \\|__|    \\|_______|    \\|__|\\|__| " << endl;

       //give the user the different options they can choose from
        cout << "\nHere is a list of our products: \n"
             << "A) Standing Desks (Small: $350, Medium: $360, Large: $370)\n"
             << "B) Blackout Curtains (Sizes 50 inch and under: $35, 51 inch and over: $40)\n"
             << "C) Tabletops ($200 each)\n"
             << "D) Table Legs ($10 each)\n";
        cout << "Please select a product: ";
        cin >> product;
//if statments based on users answer 
        if (product == "a" || product == "A"){
            cout << "How many Standing Desks would you like? ";
            cin >> sdAm;
            totalItems += sdAm;  
//different results from users different size choices
            for (int i = 1; i <= sdAm; i++) {
                cout << "Choose size for Desk " << i << " (Small: $350, Medium: $360, Large: $370): ";
                cin >> sizeChoice;

                for (auto &c : sizeChoice) c = tolower(c);

                
                if (sizeChoice == "small") {
                    smallAm++;
                    subtotal += 350;  
                } else if (sizeChoice == "medium") {
                    mediumAm++;
                    subtotal += 360;  
                } else if (sizeChoice == "large") {
                    largeAm++;
                    subtotal += 370;  
                } else {
                    cout << "Invalid choice, please select Small, Medium, or Large.\n";
                    i--; 
                }
            }
//tells user which they selected
            cout << "\nYou selected " << sdAm << " Standing Desks:\n";
            cout << smallAm << " Small\n";
            cout << mediumAm << " Medium\n";
            cout << largeAm << " Large\n";
            //condtion what happens if user selected b
        } else if (product == "b" || product == "B") {
            cout << "How many Blackout Curtains do you want? ";
            cin >> curtam;
            totalItems += curtam;  

            vector<int> curtsizes; 

            for (int i = 0; i < curtam; i++) {
                //asks user which size
                cout << "Our sizes range from 45 inch to 54 inch curtains.\n"
                     << "Curtains 50 inches and under cost $35, curtains 51 inches and over cost $40.\n"
                     << "Select the size for Curtain " << i+1 << ": ";
                cin >> curtsize;
//determines what happens based on users size and input
                
                if (curtsize >= 45 && curtsize <= 54) {
                    curtsizes.push_back(curtsize); 
                    if (curtsize <= 50) {
                        subtotal += 35;  
                    } else {
                        subtotal += 40;  
                    }
                } else {
                    cout << "Invalid size. Please select a size between 45 and 54 inches.\n";
                    i--; 
                }
            }

            cout << "\nYou selected the following curtain sizes: " << endl;
            for (int i = 0; i < curtsizes.size(); i++) {
                cout << curtsizes[i] << " inches" << endl;
                //if user enters c what will happen
            }
        } else if (product == "c" || product == "C") {
            cout << "How many Tabletops would you like? ";
            cin >> tabletopAm;
            totalItems += tabletopAm;  
            subtotal += tabletopAm * 200;  

            for (int i = 1; i <= tabletopAm; i++) {
                cout << "Choose material for Tabletop " << i << " (Wooden, Marble, Granite - All $200 each): ";
                cin >> materialChoice;

                for (auto &c : materialChoice) c = tolower(c);

                if (materialChoice == "wooden") {
                    woodenAm++;
                } else if (materialChoice == "marble") {
                    marbleAm++;
                } else if (materialChoice == "granite") {
                    graniteAm++;
                } else {
                    cout << "Invalid choice, please select Wooden, Marble, or Granite.\n";
                    i--; 
                }
            }

            cout << "\nYou selected " << tabletopAm << " Tabletops:\n";
            cout << woodenAm << " Wooden\n";
            cout << marbleAm << " Marble\n";
            cout << graniteAm << " Granite\n";
//what will happen if user enters d
        } else if (product == "d" || product == "D") {
            cout << "How many Table Legs would you like? ";
            cin >> tableLegsAm;
            totalItems += tableLegsAm;  
            subtotal += tableLegsAm * 10;  

            for (int i = 1; i <= tableLegsAm; i++) {
                cout << "Choose color for Table Leg " << i << " (Black, Brown, Yellow - All $10 each): ";
                cin >> legColor;

                for (auto &c : legColor) c = tolower(c);

                if (legColor == "black") {
                    blackLegAm++;
                } else if (legColor == "brown") {
                    brownLegAm++;
                } else if (legColor == "yellow") {
                    yellowLegAm++;
                } else {
                    cout << "Invalid choice, please select Black, Brown, or Yellow.\n";
                    i--; 
                }
            }

            cout << "\nYou selected " << tableLegsAm << " Table Legs:\n";
            cout << blackLegAm << " Black\n";
            cout << brownLegAm << " Brown\n";
            cout << yellowLegAm << " Yellow\n";
        }

        cout << "\nWould you like to buy more products? (y/n): ";
        cin >> continueShopping;
//loop meant to ask user if they want to continue or stop
    } while (continueShopping == 'y' || continueShopping == 'Y');

    double salesTax = subtotal * salesTaxRate;
    double total = subtotal + salesTax;
//the price added up and printed
    cout << fixed << setprecision(2);  
    cout << "\n-------------------- Final Bill --------------------\n";
    cout << "Total items ordered: " << totalItems << endl;
    cout << "Subtotal: $" << subtotal << endl;
    cout << "Tax: $" << salesTax << endl;
    cout << "Total: $" << total << endl;
    cout << "\nThank you for shopping at IKEA!\n";
    //thank you messgage
    cout << " _________    ___  ___      ________      ________       ___  __             ___    ___  ________      ___  ___      ___      \n";
    cout << "|\\___   ___\\ |\\  \\|\\  \\    |\\   __  \\    |\\   ___  \\    |\\  \\|\\  \\          |\\  \\  /  /||\\   __  \\    |\\  \\|\\  \\    |\\  \\     \n";
    cout << "\\|___ \\  \\_| \\ \\  \\\\\\  \\   \\ \\  \\|\\  \\   \\ \\  \\\\ \\  \\   \\ \\  \\/  /|_        \\ \\  \\/  / /\\ \\  \\|\\  \\   \\ \\  \\\\\\  \\   \\ \\  \\    \n";
    cout << "     \\ \\  \\   \\ \\   __  \\   \\ \\   __  \\   \\ \\  \\\\ \\  \\   \\ \\   ___  \\        \\ \\    / /  \\ \\  \\\\\\  \\   \\ \\  \\\\\\  \\   \\ \\  \\   \n";
    cout << "      \\ \\  \\   \\ \\  \\ \\  \\   \\ \\  \\ \\  \\   \\ \\  \\\\ \\  \\   \\ \\  \\\\ \\  \\        \\/  /  /    \\ \\  \\\\\\  \\   \\ \\  \\\\\\  \\   \\ \\__\\  \n";
    cout << "       \\ \\__\\   \\ \\__\\ \\__\\   \\ \\__\\ \\__\\   \\ \\__\\\\ \\__\\   \\ \\__\\\\ \\__\\     __/  / /       \\ \\_______\\   \\ \\_______\\   \\|__|  \n";
    cout << "        \\|__|    \\|__|\\|__|    \\|__|\\|__|    \\|__| \\|__|    \\|__| \\|__|    |\\___/ /         \\|_______|    \\|_______|       ___ \n";
    cout << "                                                                           \\|___|/                                        |\\__\\\n";
  


return 0;
}
