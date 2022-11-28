# 11.-odev

/*bir kullan�c� celcius cinsinden verilen bir s�cakl�k de�erini fahrenheit fahrenheiti ise celcius cinsinden bulmak istiyor. kullan�c�yq hangi t�r se��im yapmak
istedi�ini sorun ve buna g�re �evirme yapan program� bulunuz. F/f girerse fahrenheite C/c girerse celicusa. C=5/9(F-32). iki ayr� fonskiyon yaz�n�z.*/

#include<stdio.h>

int cel_fah(int c)
{
	return (9*c/5+32);
}

int fah_cel(int f)
{
	return (f-32)*5/9;
}

int main(void)
{
	char sec;
	int derece;
	
	printf("fahrenheit-->celcius icin C/c \n");
	printf("celcius-->fahrenheit icin F/f \n");
	
	printf("seciminizi giriniz: \n");
	scanf("%c" , &sec);
	
	if(sec=='F' || sec=='f')
	{
		printf("celcius degerini giriniz: ");
		scanf("%d" , &derece);
		printf("fahrenheit degeri: %d" , cel_fah(derece));
	}
	
	else if(sec=='C' || sec=='c')
	{
		printf("fahrenheit degerini giriniz: ");
		scanf("%d" , &derece);
		printf("celcius degeri: %d" , fah_cel(derece));
	  	
	}
	
	else
	{
		printf("yanlis secim yaptiniz.");
	}
	
	return 0;
}
