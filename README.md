# kpo-lab-1-2014812jp2
#include <iostream>
#include <cmath>
 
using namespace std;
 
int main() {
 
    //Поддержка Русского языка в консоле
    setlocale(LC_ALL, "Russian");
    double S = 0, a, x,b=2;
    int n = 1;
    cout << "Введите x:";
    cin >> x;
    a = x;
    while (1)
    {
        S +=a;
        a = pow(-1, n - 1) * pow(x, n);
        n+=2;
        if (n > 4) break; // тестирование первых 2х членов
        if (fabs(a) < 1e-15) break;
    }
 
    cout << S << '\t'<< x-(pow(x,2)/2)+(pow(x,4)/24)<<endl;//проверка
    //cout << S << endl;
    return 0;
}

