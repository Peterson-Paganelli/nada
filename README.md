/******************************************************************************

                              Online C++ Compiler.
               Code, Compile, Run and Debug C++ program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <iostream>
using namespace std;

void leitura(int &x, string letra) {
    do {
        cout << "Valor de " << letra << ": ";
        cin >> x;
        if(x <= 0) {
            cout << "Valor Invalido! Digite Novamente." << endl;
        }
    } while (x <= 0);
}

int MDC(int a, int b) {
    while(a != b) {
        (a > b) ? a - b : b = b - a;
    }
    return (a);
}

int main()
{
    int a, b;
    leitura(a, "A");
    leitura(b, "B");
    cout << endl << "Q MDC de " << a << " e " << b << " é " << MDC(a,b);
    return 0;
}



#include <iostream>
using namespace std;

void fibonacci(int &quant) {
    int aux, temp, ult = 1, penult = 0;
    
    cout << penult << endl << ult << endl;
    
    for(aux = 3; aux <= quant; aux++) {
        cout << (ult + penult) << endl;
        temp = penult;
        penult = ult;
        ult = ult + temp;
    }
}

int main()
{
    int quant;
    
    cout << "Exibir quantos termos: ";
    cin >> quant;
    fibonacci(quant);
    
    return 0;
}
