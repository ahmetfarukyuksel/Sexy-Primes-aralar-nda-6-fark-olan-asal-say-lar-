# Sexy-Primes-aralar-nda-6-fark-olan-asal-say-lar-
Sexy Primes(aralarında 6 fark olan asal sayılar)'ı c++ koduyla yazdım
#include <iostream>
using namespace std;
bool asalmi (int a) {
    if (a < 2) return false;
    for (int i = 2; i <= a / 2; i++) {
        if (a % i == 0) return false;
    }
    return true;
}
int main() {
    int maksimum;
    cout << "Sexy Primes (Farki 6 olan asal sayilar)" << endl;
    cout << "Kacinci sayiya kadar bakmak istersin ?: ";
    cin >> maksimum;
    for (int i = 2; i <= maksimum; i++) {
        if (asalmi(i) && asalmi(i + 6)) {
            cout << i << " , " << (i + 6) << endl;
        }
    }
    return 0;
}
