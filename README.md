#include<iostream>
#include<string>
using namespace std;

struct Cong_Nhan
{
	string Ten;
	double Luong;
	int Tuoi;
	string chucVu;
};

int main()
{
	Cong_Nhan *congNhan;
	int n;
	cout << "Nhap so cong nhan: ";
	cin >> n;
	congNhan = new Cong_Nhan[n];
	for (int i = 0; i < n; i++)
	{
		cout << "Nhap thong tin cong nhan thu " << i << ": ";
		cout << "\nTen cong nhan: ";
		fflush(stdin);
		getline(cin, congNhan[i].Ten);
		cout << "Chuc vu: ";
		fflush(stdin);
		getline(cin, congNhan[i].chucVu);
		cout << "Tuoi: ";
		fflush(stdin);
		cin >> congNhan[i].Tuoi;
		cout << "Luong: ";
		fflush(stdin);
		cin >> congNhan[i].Luong;
	}

	system("pause");
}
