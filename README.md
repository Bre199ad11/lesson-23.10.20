#include <iostream>
//#include <fstream>
#include <cstdio>

#pragma warning(disable:4996); //отключили ошибку

using namespace std;

int main(){ 

	int a[9] = {1,2,3,4,5,6,7,8,9};
	/*ofstream fout1("output1.txt"), fout2("output2.txt"); //ofstream - тип
	for (int i = 0; i < 9; i++) {
		fout1 << a[i] << ' ';
		fout2 << a[i] * a[i] << ' ';
	}
	fout1 << endl;
	fout2 << endl;
	fout1.close();
	fout2.close();*/

	FILE* f1 = fopen("outut1.txt", "w"); //w- открыли на запись
	FILE* f2 = fopen("outut2.txt", "w");
	for (int i = 0; i < 9; i++) {
		fprintf(f1, "%d", a[i]);
		fprintf(f2, "%d", a[i]*a[i]);
	}
	fputs("\n", f1);
	fputs("\n", f2);
	fclose(f1);
	fclose(f2);
}	
