#include <iostream>
#include<Windows.h>
#include<string>
#include <locale>
#include <cctype>
#include <vector>
using namespace std;

void  Dlina(int  mera_izm)
{
    cout << "Хорошо, введите километры: " << endl;
    cin >> mera_izm;
    cout << "Километры = " << mera_izm << endl;
    cout << "Метр = " << mera_izm * 1000 << endl;
    cout << "Дециметр = " << mera_izm * 10000 << endl;
    cout << "Сантиметр = " << mera_izm * 100000 << endl;
    cout << "Миллиметр = " << mera_izm * 1000000 << endl;
}

void  Massa(int  mera_izm)
{
    cout << "О ма гад, введите килограмы : " << endl;
    cin >> mera_izm;
    cout << "Килограммы = " << mera_izm << endl;
    cout << "Граммы = " << mera_izm * 1000 << endl;
    cout << "Фунты = " << mera_izm * 2.204623 << endl;
    cout << "Унция = " << mera_izm * 35.27396 << endl;
}

void Temperature(string& temp, int & mera_izm)
{
    locale loc("ru_RU.UTF-8");
    while (temp != "цельсий" and temp != "фаренгейт" and temp != "кельвин")
    {
        cout << "Выбирите одну из трех единиц измерений (цельсий или кельвин или фаренгейт): " << endl;
        cin >> temp;
        for (int i = 0; i < temp.size(); i++)
        {
            temp[i] = tolower(temp[i]);
        }

        cout << endl;
    }
    cout << "Введите кол-во градусов: " << endl;
    cin >> mera_izm;
    if (temp == "цельсий")
    {
        cout << "Цельсий = " << mera_izm << endl;
        cout << "Фаренгейт = " << mera_izm * 9.00 / 5.00 + 32 << endl;
        cout << "Кельвин = " << 273.15 + mera_izm * 1 << endl;
    }
    if (temp == "фаренгейт")
    {
        cout << "Фаренгейт = " << mera_izm << endl;
        cout << "Цельсий = " << (mera_izm - 32.000) * 5 / 9 << endl;
        cout << "Кельвин = " << (mera_izm - 32) * 5 / 9.0 + 273.15 << endl;
    }
    if (temp == "кельвин")
    {
        cout << "Кельвин = " << mera_izm << endl;
        cout << "Цельсий  = " << mera_izm - 273.15 << endl;
        cout << "Фаренгейт = " << (mera_izm - 273.15) * 9 / 5 + 32 << endl;
    }
} 

void Valyta(string& valute, int & mera_izm)
{
    while (valute != "1" and valute != "2" and valute != "3" and valute != "4" and valute != "5" and valute != "6" and valute != "7")
    {
        cout << "Выберите одну из далее предосталвенных валют: " << endl << "1)Рубль-родненький" << endl << "2)Беларусский рубль-брат по крови" << endl << "3)Тенге-покровитель чакчака степного" << endl << "4)Доллар США-банкноты заморские" << endl << "5)Юань-всему голова" << endl << "6)Австралийский доллар - для богатых этаких" << endl << "7)Евро - окупант таковой" << endl;
        cin >> valute;
    }
    cout << "Введите кол-во: " << endl;
    cin >> mera_izm;
    if (valute == "1")
    {
        cout << "Рубль =" << mera_izm << endl;
        cout << "Тенге =" << mera_izm * 6.44 << endl;
        cout << "Беларусский рубль =" << mera_izm * 0.0377 << endl;
        cout << "Доллар =" << mera_izm * 0.0126 << endl;
        cout << "Юань =" << mera_izm * 0.0914 << endl;
        cout << "Австралийский доллар =" << mera_izm * 0.019 << endl;
        cout << "Евро =" << mera_izm * 0.011 << endl;
    }
    else if (valute == "2")
    {
        cout << "Беларусский рубль =" << mera_izm << endl;
        cout << "Тенге =" << mera_izm * 170.6 << endl;
        cout << "Рубль =" << mera_izm * 26.5 << endl;
        cout << "Доллар =" << mera_izm * 0.3338 << endl;
        cout << "Юань =" << mera_izm * 2.4 << endl;
        cout << "Австралийский доллар =" << mera_izm * 0.5135 << endl;
        cout << "Евро =" << mera_izm * 0.2884 << endl;
    }
    else if (valute == "3")
    {
        cout << "Тенге =" << mera_izm << endl;
        cout << "Беларусский рубль =" << mera_izm * 0.0058 << endl;
        cout << "Рубль =" << mera_izm * 0.1554 << endl;
        cout << "Доллар =" << mera_izm * 0.0019 << endl;
        cout << "Юань =" << mera_izm * 0.0140 << endl;
        cout << "Австралийский доллар =" << mera_izm * 0.003 << endl;
        cout << "Евро =" << mera_izm * 0.001 << endl;
    }
    else if (valute == "4")
    {
        cout << "Доллар =" << mera_izm << endl;
        cout << "Тенге =" << mera_izm * 512.36 << endl;
        cout << "Беларусский рубль =" << mera_izm * 3 << endl;
        cout << "Рубль =" << mera_izm * 79 << endl;
        cout << "Юань =" << mera_izm * 7.18 << endl;
        cout << "Австралийский доллар =" << mera_izm * 1.54 << endl;
        cout << "Евро =" << mera_izm * 0.86 << endl;
    }
    else if (valute == "5")
    {
        cout << "Юань =" << mera_izm << endl;
        cout << "Тенге =" << mera_izm * 71.29 << endl;
        cout << "Беларусский рубль =" << mera_izm * 0.4164 << endl;
        cout << "Рубль =" << mera_izm * 10.93 << endl;
        cout << "Доллар =" << mera_izm * 0.1393 << endl;
        cout << "Австралийский доллар =" << mera_izm * 0.2146 << endl;
        cout << "Евро =" << mera_izm * 0.1205 << endl;
    }
    else if (valute == "6")
    {
        cout << "Австралийский доллар =" << mera_izm << endl;
        cout << "Юань =" << mera_izm * 4.66 << endl;
        cout << "Тенге =" << mera_izm * 332.24 << endl;
        cout << "Беларусский рубль =" << mera_izm * 1.95 << endl;
        cout << "Рубль =" << mera_izm * 51.49 << endl;
        cout << "Доллар =" << mera_izm * 0.649 << endl;
        cout << "Евро =" << mera_izm * 0.5617 << endl;
    }
    else if (valute == "7")
    {
        cout << "Евро =" << mera_izm << endl;
        cout << "Австралийский доллар =" << mera_izm * 1.78 << endl;
        cout << "Юань =" << mera_izm * 8.3 << endl;
        cout << "Тенге =" << mera_izm * 591.54 << endl;
        cout << "Беларусский рубль =" << mera_izm * 3.47 << endl;
        cout << "Рубль =" << mera_izm * 90.01 << endl;
        cout << "Доллар =" << mera_izm * 1.16 << endl;
    }
}
int main()
{
    SetConsoleCP(1251);
    SetConsoleOutputCP(1251);
    int vibor = 0;
    int mera_izm = 0;
    string temp;
    string valute;
    cout << "1)Длина\n2)Масса\n3)Температура\n4)Валюта" << endl;
    cout << "Выбирите один из преобразователей: " << endl;
    cin >> vibor;
    switch (vibor)
    {
    case 1:
    {
        Dlina(mera_izm);
        break;
    }
    case 2:
    {
        Massa(mera_izm);
        break;
    }
    case 3:
    {

        Temperature(temp, mera_izm);
        break;
    }
    case 4:
    {
        Valyta(valute, mera_izm);
        break;
    }
    }
}
