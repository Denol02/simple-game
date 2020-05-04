# simple-game
//This is a simple quest game made at 14 years old.
#include <iostream>
#include <windows.h>
#include<ctime>
#include <cstdlib>
#include <clocale>

using namespace std;




int main()
{
    setlocale(LC_ALL, "Rus");

    int p = 40;
    int h = 100;
    int p1 = 30;
    int h1 = 80;


    cout << " \t Cave " << "\n" << "\tTreasure. " << endl;

    cout << " The protagonist Daniel, a tomb raider, finds a map on his next trip that reads: “about a secret cave in the depths of Siberia, in which there is wealth for life and ...”. The legend breaks off due to the torn half. The traveler immediately went to the cave, since the map survived." << "\n" << endl;

    cout << "He meets three passes and a sign that says: “difficulties will await in 1 pass, but at the end there will be a reward, in 2 treasures at once, and in 3, danger and adventure ”  " << endl;

    int c;

    cin >> c;

    switch (c)
    {
    case 1:
    {


        system("cls");

        cout << "You meet a spider \n You can attack by choosing 1 or heal by choosing 2" << endl;

        cout << "You have " << h << "HP " << p << " Power" << endl;

        int a;
        int b = rand() % 1;


        for (a <= 0; b <= 0;)
        {
            cin >> a;

            if (a == 1)
            {
                h1 = h1 - p;

            }
            else
            {
                h = h + p;
            }

            cout << "You have " << h << "HP " << p << "Power " << endl;
            cout << "The enemy has " << h1 << "HP " << p1 << "Power \n" << endl;

            if (b == 0)
            {
                h = h - p1;
            }
            else
            {
                h1 = h1 + p1;
            }
            cout << "You have " << h << "HP " << p << "Power" << endl;
            cout << "The enemy has " << h1 << "HP " << p1 << "Power" << endl;
            if (h1 <= 0)
            {
                cout << "\n \t You managed and opened the tomb, on this your journey ended" << endl;
            }
            else
            {
                cout << "You died" << endl;
            }
        }

        break;
    }
    case 2:
    {
        system("cls");
        srand((unsigned)time(NULL));
        int g = rand() % 100;
        if (g > 90)
        {
            cout << "You have dealt with 10 traps and opened the tomb, this is the end of your journey" << endl;
        }
        else
        {
            cout << "You died in one of 10 traps" << endl;
        }
        system("pause");
        exit(0);
        break;
    }
    case 3:
    {
        system("cls");
        {
            int a, b, c, d;

            cout << "Solve 4 examples and you will open the entrance to the tomb" << endl;

            cout << "1: 69 + 27 = " << endl;

            cin >> a;

            if (a == 96)
            {
                cout << "Farther" << endl;
            }
            else
            {
                cout << "You made a mistake and fell to the floor" << endl;
                system("pause");
                exit(0);
            }

            cout << "2:  234 - 129 = " << endl;

            cin >> b;

            if (b == 105)
            {
                cout << "Good" << endl;
            }
            else
            {
                cout << "You made a mistake and gas poisoned you" << endl;
                system("pause");
                exit(0);
            }

            cout << "3: (10 * 9) - (425 / 5)  = " << endl;

            cin >> c;

            if (c == 5)
            {
                cout << "Fine" << endl;
            }
            else
            {
                cout << "You were mistaken and pierced by an arrow" << endl;
                system("pause");
                exit(0);
            }

            cout << "4: 5 - |10| = " << endl;

            cin >> d;

            if (d == 15)
            {
                cout << "You managed and opened the tomb, on this your journey ended" << endl;
                system("pause");
                exit(0);
            }
            else
            {
                cout << "A door opens before you, from which a swarm of poisonous spiders flee " << endl;
                system("pause");
                exit(0);
            }


        }
        break;
    }
    }

    return 0;
}


