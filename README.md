#include <iostream>
#include <fstream>
using namespace std;

int main(){ 

	int a[9] = {1,2,3,4,5,6,7,8,9};
	ofstream fout1("output1.txt"), fout2("output2.txt"); //ofstream - тип
	for (int i = 0; i < 9; i++) {
		fout1 << a[i] << ' ';
		fout2 << a[i] * a[i] << ' ';
	}
	fout1 << endl;
	fout2 << endl;
	fout1.close();
	fout2.close();
}	
