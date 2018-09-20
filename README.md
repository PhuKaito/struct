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
		cout << "Nhap thong tin cong nhan thu " << i + 1 << ": ";
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
	double Max = 0;
	string Maxluong;
	Max = congNhan[0].Luong;
	for (int i = 0; i < n; i++)
	{
		if (congNhan[i].Luong > Max)
		{
			Max = congNhan[i].Luong;
			Maxluong = congNhan[i].Ten;
		}
	}
	cout << "===============================================";
	cout << "\nCong nhan co luong cao nhat la: " << Maxluong;
	double SumLuong = 0;
	for (int i = 0; i < n; i++)
	{
		SumLuong = SumLuong + congNhan[i].Luong;
	}
	cout << "\nTong so luong phai tra la: " << fixed<<SumLuong;
	cout << "\nSap xep cong nhan theo chuc vu: \n";
	for (int i = 0; i < n; i++)
	{
		if (congNhan[i].chucVu == "Giam doc")
		{
			cout << congNhan[i].Ten << endl;
		}		
	}
	for (int i = 0; i < n; i++)
	{
		if (congNhan[i].chucVu == "Truong phong")
		{
			cout << congNhan[i].Ten << endl;
		}
	}
	for (int i = 0; i < n; i++)
	{
		if (congNhan[i].chucVu == "Nhan vien")
		{
			cout << congNhan[i].Ten << endl;
		}
	}
	cout << endl;
	system("pause");
}
