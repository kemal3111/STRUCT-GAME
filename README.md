#include <iostream>
using namespace std;

struct pemainInti {
	string nama, nama2;
	int pukulan;
};

struct pemain {	
	string nama, nama2; 
	int banyakHp;
	int pukulan;
	
	makan(pemainInti objekpemainInti) {
		banyakHp = banyakHp - objekpemainInti.pukulan;
		cout << nama << " memukul " << nama2 << " dengan " << objekpemainInti.nama << "\n";
		printKecerdasan();
	}
	
	printKecerdasan() {
		cout << "HP " << nama2 << " berkurang jadi " << banyakHp << "\n"; 
	}
};

int main(){
	pemain m1;
	m1.nama = "Pasha";
	m1.nama2 = "Kemal";
	m1.banyakHp = 100;
	
	pemainInti pemainInti1;
	pemainInti1.nama = "Tongkat Kayu";
	pemainInti1.pukulan = 10;
	
	pemainInti pemainInti2;
	pemainInti2.nama = "Palu";
	pemainInti2.pukulan = 50; 
	
	m1.makan(pemainInti1);
	m1.makan(pemainInti1);
	m1.makan(pemainInti2);
	m1.makan(pemainInti2);

	
	if (m1.banyakHp <= 0){
	cout << m1.nama2 << " meninggal, " << m1.nama << " menang!!" ;
}
	
	
}
