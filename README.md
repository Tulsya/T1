#include <iostream>
#include <fstream>
#include <vector>

using namespace std;

int main() {
    ifstream fin("in.txt");
    ofstream fout("out.txt");

    int n, m;
    fin >> n;
    vector<int> arr_n(n);
    for (int i = 0; i < n; i++) {
        fin >> arr_n[i];
    }
    fin >> m;
    vector<int> arr_m(m);
    for (int i = 0; i < m; i++) {
        fin >> arr_m[i];
    }

    fout << m << endl;
    
    fout << arr_m[m-1] << " ";

    for (int i = 0; i < m - 1; i++) {
        fout << arr_m[i] << " ";
    }

    fout << endl;
    fout << n << endl;

    for (int i = 1; i < n; i++) {
        fout << arr_n[i] << " ";
    }

    fout << arr_n[0] << " ";
}