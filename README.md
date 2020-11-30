# v0.11.cpp

#include <iostream>
#include <fstream>
#include <iomanip>
#include <windows.h>
#include <time.h>
using namespace std;
struct baze{string vardas; string pavarde; float vid;}; 
baze b[1000];
main() {		
long m;
float sum=0,vid,t,med;
cout <<"iveskite eiluciu skaiciu: ";
cin >> m;
for(long i=1;i<=m;i=i+1) {
cout << "iveskite" << i << " : ";
cin >> b[i].vardas >> b[i].pavarde >> b[i].vid;
}
for(long i=1;i<=m;i=i+1) sum=sum+b[i].vid;
vid=sum/m;
cout << fixed << setprecision(2);
cout <<"vidurkis yra: " << vid << endl;


for (long j=1; j<=m-1; j++)
for (long i=1; i<=m-1; i++){
	if( b[i].vid>b[i+1].vid){
		t=b[i].vid;
		b[i].vid=b[i+1].vid;
		b[i+1].vid=t;
	}}
	if(m%2==1) med=b[(m+1)/2].vid; else med=( b[m/2].vid+b[(m/2)+1].vid )/2;
	
	cout <<"mediana yra: " << med << endl; 
	
}
