#include <iostream>
#include <fstream> //(1),(3)
#include <cstdio> //(2)
#include <string> //(4)

#pragma warning(disable:4996); //отключили ошибку

using namespace std;


//(5)
template <typename T>
void bubblesort(T* a,int n) { //void -если функция ничего не возвращает
	for (int i = n-1; i >0; i--) {
		for (int j = 0; j < i; j++) {
			if (a[j] > a[j + 1])
				swap(a[j], a[j + 1]);
		}
	}
}


int main(){ 


	int a[9] = {1,2,3,4,5,6,7,8,9};


	// (1)
	/*ofstream fout1("output1.txt"), fout2("output2.txt"); //ofstream - тип
	for (int i = 0; i < 9; i++) {
		fout1 << a[i] << ' ';
		fout2 << a[i] * a[i] << ' ';
	}
	fout1 << endl;
	fout2 << endl;
	fout1.close();
	fout2.close();*/


	//(2)
	/*FILE* f1 = fopen("output1.txt", "w"); //w- открыли на запись
	FILE* f2 = fopen("output2.txt", "w");
	for (int i = 0; i < 9; i++) {
		fprintf(f1, "%d", a[i]);
		//fprintf(f2, "%d ", a[i]*a[i]);
		fscanf(f2, "%d", &a[i]);
		printf("%d ", a[i]);
		if (feof(f2)) //feof если конец
			break;
	}
	fputs("\n", f1);
	fputs("\n", f2);
	fclose(f1);
	fclose(f2);*/


	//(3)
	/*ifstream fin1("output1.txt");
	for (int i = 0; i < 9; i++) {
		if (fin1.eof())
			break;
		fin1 >> a[i];
		cout << a[i] << ' ';
	}*/


	//(4)
	/*string s1 = "123";
	auto s2 = "456"s;
	auto x = 5;
	cout << s1.size() << endl;*/


	//(5)
	double x[] = { 6,2,4,8,1,7,5,9,3 };
	bubblesort(x, 9);
	for (int i = 0; i < 9; i++) {
		cout << x[i] << ' ';
	}

}	
