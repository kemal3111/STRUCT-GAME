#include <iostream>
using namespace std;

struct makanan {
	string nama, nama2;
	int skorRasa;
	int kadarMicin;
};

struct manusia {	
	int umur;
	string nama, nama2; 
	int tingkatKecerdasan;
	
	makan(makanan objekMakanan) {
		tingkatKecerdasan = tingkatKecerdasan - objekMakanan.kadarMicin;
		cout << nama << " memukul " << nama2 << " dengan " << objekMakanan.nama << "\n";
		printKecerdasan();
	}
	
	printKecerdasan() {
		cout << "HP " << nama2 << " berkurang jadi " << tingkatKecerdasan << "\n"; 
	}
};

int main(){
	makanan makanan1;
	makanan1.nama = "Tongkat";
	makanan1.kadarMicin = 10;
	
	makanan makanan2;
	makanan2.nama = "Palu";
	makanan2.kadarMicin = 50; 
	
	manusia m1;
	m1.nama = "Pasha";
	m1.nama2 = "Kemal";
	m1.tingkatKecerdasan = 100;
	
	m1.makan(makanan1);
	m1.makan(makanan1);
	m1.makan(makanan2);
	m1.makan(makanan2);

	
	if (m1.tingkatKecerdasan <= 0){
	cout << m1.nama2 << " meninggal, " << m1.nama << " menang!!" ;
}
	
	
}
