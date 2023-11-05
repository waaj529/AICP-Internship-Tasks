# AICP-Internship-Tasks

Here is Task 1:

I wrote the code in CPP:

-----------------------------------Here is the Code------------------------------------

#include <iostream>
using namespace std;
#include <string>

int main() {
//declaration of variables,contants and arrays
    const float initial_price = 200.0;
    int count = 0;
    string case_code = "", ram_code = "", main_disk_code = "";
    string case_description = "", ram_description = "", main_disk_description = "";
    string item_code[18];
    string item_description[18];
    float case_price = 0.0, ram_price = 0.0, main_disk_price = 0.0, total_price = 0.0;
    float item_price[18];
//Assigning values to 3 different Arrays

    item_code[1] = "A1";
    item_code[2] = "A2";
    item_code[3] = "B1";
    item_code[4] = "B2";
    item_code[5] = "B3";
    item_code[6] = "C1";
    item_code[7] = "C2";
    item_code[8] = "C3";
    item_code[9] = "D1";
    item_code[10] = "D2";
    item_code[11] = "E1";
    item_code[12] = "E2";
    item_code[13] = "E3";
    item_code[14] = "F1";
    item_code[15] = "F2";
    item_code[16] = "G1";
    item_code[17] = "G2";

    item_description[1] = "Case Compact";
    item_description[2] = "Case Tower";
    item_description[3] = "RAM 8 GB";
    item_description[4] = "RAM 16 GB";
    item_description[5] = "RAM 32 GB";
    item_description[6] = "Main Hard Disk Drive 1 TB HDD";
    item_description[7] = "Main Hard Disk Drive 2 TB HDD";
    item_description[8] = "Main Hard Disk Drive 4 TB HDD";
    item_description[9] = "Solid State Drive 240 GB SSD";
    item_description[10] = "Solid State Drive 480 GB SSD";
    item_description[11] = "Second Hard Disk Drive 1 TB HDD";
    item_description[12] = "Second Hard Disk Drive 2 TB HDD";
    item_description[13] = "Second Hard Disk Drive 4 TB HDD";
    item_description[14] = "Optical Drive DVD/Blu-Ray Player";
    item_description[15] = "Optical Drive DVD/Blu-Ray Re-writer";
    item_description[16] = "Operating System Standard Version";
    item_description[17] = "Operating System Professional Version";

    item_price[1] = 75.00;
    item_price[2] = 150.00;
    item_price[3] = 79.99;
    item_price[4] = 149.99;
    item_price[5] = 299.99;
    item_price[6] = 49.99;
    item_price[7] = 89.99;
    item_price[8] = 129.99;
    item_price[9] = 59.99;
    item_price[10] = 119.99;
    item_price[11] = 49.99;
    item_price[12] = 89.99;
    item_price[13] = 129.99;
    item_price[14] = 50.00;
    item_price[15] = 100.00;
    item_price[16] = 100.00;
    item_price[17] = 175.00;

    cout << "New sale initiated - Default basic set of components costing $200 is added." << endl;
    cout << "One case, one RAM, and one Main Hard Disk Drive is required to be added." <<endl;

    cout << "The following are the case item codes along with their descriptions and prices:" << endl;
    //For Loop use for details of output
    for (count = 1; count <= 2; count++) {
        std::cout << "Item code: " << item_code[count] << std::endl;
        std::cout << "Item description: " << item_description[count] <<endl;
        std::cout << "Item price: " << item_price[count] << std::endl;
    }

    cout << "Enter the case item code (A1 or A2): ";
    cin >> case_code;

    while (case_code != "A1" && case_code != "A2") {
        cout << "Wrong case item code. It should be either A1 or A2 only." <<endl;
        cout << "Enter the case item code (A1 or A2): ";
        cin >> case_code;
    }

    cout << "The following are the RAM item codes along with their descriptions and prices:" << endl;
    for (count = 3; count <= 5; count++) {
        cout << "Item code: " << item_code[count] <<endl;
        cout << "Item description: " << item_description[count] << endl;
        cout << "Item price: " << item_price[count] <<endl;
    }

    cout << "Enter the RAM item code (B1 or B2 or B3): ";
    cin >> ram_code;

    while (ram_code != "B1" && ram_code != "B2" && ram_code != "B3") {
        cout << "Wrong RAM item code. It should be either B1, B2, or B3 only." <<endl;
        cout << "Enter the RAM item code (B1 or B2 or B3): ";
        cin >> ram_code;
    }

    cout << "The following are the Main Hard Disk Drive item codes along with their descriptions and prices:" <<endl;
    for (count = 6; count <= 8; count++) {
        cout << "Item code: " << item_code[count] <<endl;
        cout << "Item description: " << item_description[count] << endl;
        cout << "Item price: " << item_price[count] <<endl;
    }

    cout << "Enter the Main Hard Disk Drive item code (C1 or C2 or C3): ";
    cin >> main_disk_code;

    while (main_disk_code != "C1" && main_disk_code != "C2" && main_disk_code != "C3") {
        cout << "Wrong Main Hard Disk Drive item code. It should be either C1, C2, or C3 only." << endl;
        cout << "Enter the Main Hard Disk Drive item code (C1 or C2 or C3): ";
        cin >> main_disk_code;
    }

    for (count = 1; count <= 8; count++) {
        if (item_code[count] == case_code) {
            case_price = item_price[count];
            case_description = item_description[count];
        }
        if (item_code[count] == ram_code) {
            ram_price = item_price[count];
            ram_description = item_description[count];
        }
        if (item_code[count] == main_disk_code) {
            main_disk_price = item_price[count];
            main_disk_description = item_description[count];
        }
    }

    total_price = initial_price + case_price + ram_price + main_disk_price;

    cout << "The case, RAM, and Main Hard Disk Drive bought along with their codes, descriptions, and prices are:" <<endl;
    cout << case_code << ", " << case_description << ", " << case_price << endl;
    cout << ram_code << ", " << ram_description << ", " << ram_price << std::endl;
    cout << main_disk_code << ", " << main_disk_description << ", " << main_disk_price << endl;
    cout << "The total price of the computer after buying the required items is: $" << total_price <<endl;

    return 0;
}
