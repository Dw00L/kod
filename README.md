# kod
// Example program
#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

using namespace std;

void wylosujLiczby (int tablica[], int ile_liczb, int a, int b)
{
    a=a;
    b-=3;
    int licznik=0;
    for(licznik=0; licznik<ile_liczb; licznik++)
    {
        tablica[licznik]=(rand()%b)+a;
    }
}
void wypiszLiczby (int tablica[], int ile_liczb)
{
    int licznik=0;
    for(licznik=0; licznik<ile_liczb;licznik++)
    {
        cout<<tablica[licznik]<<endl;
    }
}

int obliczSume (int tablica[], int ile_liczb)
{
    int suma=0;
    int licznik=0;
    
    for(licznik=0; licznik< ile_liczb; licznik++)
    {
      suma+=tablica[licznik];
    }
      
}

int main()
{
    srand(time(NULL));

 int tablica[ 999 ];
    wylosujLiczby( tablica, 999, 4, 10 );
    wypiszLiczby( tablica, 999 );
    int iSuma = obliczSume( tablica, 999 );
    std::cout << "Suma liczb wynosi: " << iSuma << std::endl;
    system ("pause");
}
