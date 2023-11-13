#include <iostream>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <string.h>
#include <stdlib.h>
#include <cstring>
#include <conio.h>
#include <iomanip>
#include <process.h>
#include <ctime>
#include <cstdlib>



using namespace std;
class gamma {
private:
    static int total;
    int id;
public:
    gamma() {
        total++;
        id = total;
    }
    ~gamma() {
        total--;
        cout << "Deleted ID " << id << endl;
    }
    static void showtotal() {
        cout << "In total: " << total << endl;
    }
    void showid() {
        cout << "ID: " << id << endl;
    }
};
int gamma::total = 0;


int main()
{
    gamma g1;
    gamma::showtotal();

    gamma g2, g3;
    gamma::showtotal();

    g1.showtotal();
    g2.showtotal();
    g3.showtotal();
    cout << "End of the program\n";

    return 0;
}
