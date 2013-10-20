/*Kullanıcı Bilgileri:
Hesap Numarası=100 Şifre =123456
Hesap Numarası=200 Şifre =123123
Hesap Numarası=300 Şifre =111111
*/


#include<stdio.h>
#include<stdlib.h>
#include<math.h>
#include<locale.h>
#include<Windows.h>

int main()
{
	int secim1,secim2,secim3,yanlis,sifre,havale=0,paraYatirma=0,paraCekme=0,burhanBakiye=10000,burakBakiye=15000,baranBakiye=21000,hesapNo;


	while(1) // Menüye Dönebilmek İçin Döngü
	{
		printf("\t\t\t  ======KDV BANKASI======\n\n ");
		printf("\t\t\t  KDV BANKASI GIRIS MENUSU\n\n");
		printf("\t\t\t 1)Giris Yap\n");
		printf("\t\t\t 2)Cikis\n\n");

		printf("Secim Yapiniz<1-2>");
		scanf("%d", &secim1);

	if(secim1!=1 && secim1!=2)	//1 ve 2'den farklı giriş yapılırsa hata mesajı
	{
		printf("Hatali Secim Yaptiniz.Lutfen Tekrar Deneyiniz\n");
		printf("---------------------------------------------\n\n");
	}
			switch(secim1)
		{
			case 1: //Giriş Yap Seçildiyse
				system("CLS");//Ekran Temizlemek İçin

				for(yanlis=1; yanlis<=3;) //3 Yanlış Şifre Hakkı İçin
				{
					printf("Lutfen Hesap Numarasini giriniz:\n\n");
					printf("Hesap Numarasi		:");
					scanf("%d", &hesapNo);
					printf("Lutfen Sifrenizi Giriniz:");
					scanf("%d",&sifre);
					
					printf("Kontrol Ediliyor\n\n\n");
					Sleep(1500);//Bekleme Yapması İçin 
					



			if((hesapNo==100 && sifre==123456) || (hesapNo==200 && sifre ==123123) || (hesapNo==300 && sifre ==111111))//Kullanıcı tanımı
			{
				system("CLS"); //Ekranı Temizlemek İçin

				do
				{
					if(hesapNo==100)
						printf("\t\t\t Hesap Numarasi:100\n");
					if(hesapNo==200)
						printf("\t\t\t Hesap Numarasi:200\n");
					if(hesapNo==300)
						printf("\t\t Hesap Numarasi:300\n");
					printf("\t\t\t	KDV BANKASI ISLEM MENUSU\n\n");
					printf("\t\t1)		Para Yatirma		:\n");
					printf("\t\t2)		Para Cekme		:\n");
					printf("\t\t3)		Bakiye Goruntule	:\n");
					printf("\t\t4)		Havale Islemleri	:\n");
					printf("\t\t5)		Cikis Yap		:\n");
					printf("Lutfen Islem Yapmak Icin Secim Yapiniz:(1-5)");
					scanf("%d", &secim2);

					if(secim2!=1 && secim2!=2 && secim2!=3 && secim2!=4 && secim2!=5)// 1-5 Dışında Seçim Yapılırsa Hata Mesajı
					{
						printf("Hatali Secim Yaptiniz.Lutfen Tekrar Deneyiniz\n");
						printf("-------------------------------------------------\n\n");
					}

					switch(secim2)
					{
					case 1: //Para Yatırma
						printf("Yatiracaginiz Para Miktarini Giriniz:\n");
						scanf("%d", &paraYatirma);
						if(hesapNo==100)
						{
							burhanBakiye=burhanBakiye+ paraYatirma;
							printf("\nHesabiniza %d TL yatiriliyor......\n",paraYatirma);
							Sleep(1500);
							printf("Isleminiz Basariyla gerceklestirildi \n");
							printf("Yeni Bakiyeniz %d TL dir.\n\n",burhanBakiye);
						}
						if(hesapNo==200)
						{
							baranBakiye=baranBakiye+ paraYatirma;
							printf("\nHesabiniza %d TL yatiriliyor......\n",paraYatirma);
							Sleep(1500);
							printf("Isleminiz Basariyla gerceklestirildi:\n");
							printf("Yeni Bakiyeniz %d TL dir.\n\n",baranBakiye);
						}
						if(hesapNo==300)
						{
							burakBakiye=burakBakiye+ paraYatirma;
							printf("\nHesabiniza %d TL yatiriliyor......\n",paraYatirma);

							printf("Isleminiz Basariyla gerceklestirildi:\n");
							printf("Yeni Bakiyeniz %d TL dir.\n\n",burakBakiye);
						}
						break;
					case 2: // Para Çekme
						printf("Cekeceginiz Para Miktarini Giriniz:\n");
						scanf("%d", &paraCekme);
						if(hesapNo==100 &&paraCekme<=burhanBakiye)
						{
							burhanBakiye=burhanBakiye - paraCekme;
							printf("\nHesabinizdan %d TL cekiliyor......\n",paraCekme);
							Sleep(1500);
							printf("Isleminiz Basariyla gerceklestirildi:\n");
							printf("Yeni Bakiyeniz %d TL dir.\n\n",burhanBakiye);
							break;
						}
						if(hesapNo==200 &&paraCekme<=baranBakiye)
						{
							baranBakiye=baranBakiye - paraCekme;
							printf("\nHesabinizdan %d TL cekiliyor......\n",paraCekme);
							Sleep(1500);
							printf("Isleminiz Basariyla gerceklestirildi:\n");
							printf("Yeni Bakiyeniz %d TL dir.\n\n",baranBakiye);
							break;
						}
						if(hesapNo==300 &&paraCekme<=burakBakiye)
						{
							burakBakiye=burakBakiye - paraCekme;
							printf("\nHesabinizdan %d TL cekiliyor......\n",paraCekme);
							Sleep(1500);
							printf("Isleminiz Basariyla gerceklestirildi:\n");
							printf("Yeni Bakiyeniz %d TL dir.\n\n",burakBakiye);
							break;
						}
						else if(paraCekme>burhanBakiye ||paraCekme>baranBakiye || paraCekme>burakBakiye) //Bakiyeden Fazla Para Çekmek İstenirse Hata Mesajı
						{	
							printf("\nHesabinizdan %d TL cekiliyor.....\n",paraCekme);
							Sleep(1500);
							printf("\nYETERSIZ BAKIYE  \n\n");
							printf("Isleminiz Gerceklestirilemedi   \n\n");

					}
					break;
				case 3: //Bakiye Görüntüleme
				if(hesapNo==100)
					printf("Mevcut Bakiyeniz: %d TL dir.\n\n",burhanBakiye);
				if(hesapNo==200)
					printf("Mevcut Bakiyeniz: %d TL dir\n\n",baranBakiye);
				if(hesapNo==300)
					printf("Mevcut Bakiyeniz: %d TL dir\n\n",burakBakiye);
				break;
				case 4: //Havale İslemleri 
					printf("Havale Icin Lutfen Hesap No Giriniz:\n");
					scanf("%d",&hesapNo);
					printf("Lutfen Miktari Giriniz:");
					scanf("%d",&havale);
					if(hesapNo==100  && havale<=burhanBakiye)
					{
						burhanBakiye=burhanBakiye-havale;
						printf("\nHesabinizdan %d TL gonderiliyor",havale);
						printf("\nYeni Bakiyeniz %d TL dir:",burhanBakiye);
					
					}
					break;
					if(hesapNo==200  && havale<=baranBakiye)
					{
						baranBakiye=baranBakiye-havale;
						printf("\nHesabinizdan %d TL gonderiliyor",havale);
						Sleep(1500);
						printf("\nYeni Bakiyeniz %d TL dir:",baranBakiye);
					
					}
					break;
					if(hesapNo==300  && havale<=burakBakiye)
					{
						burakBakiye=burakBakiye-havale;
						printf("\nHesabinizdan %d TL gonderiliyor",havale);
						Sleep(1500);
						printf("\nYeni Bakiyeniz %d TL dir:",burakBakiye);
					
					}
					break;
				case 5://Çıkış Yapmak İçin
					printf("Cikis Yapiliyor.	.	.");

					system("CLS");//Ekranı temizlemek için
					break;
				}
			}
				while(secim2!=5);

				break;
				}
				else //Yanlış Giriş Yapıldığında Hata Mesajı
				{
					printf("Hatali Giris Yaptiniz. %d deneme hakkiniz kaldi..",3-yanlis);
					printf("-------------------------------------------------\n\n");	
					yanlis++;
				}
					}
					if (yanlis==4) //3 Kere Yanlış Yapınca Menüye Geri Dönmek İçin
					{
						printf("3 kere yanlis sifre girdiniz.Menüye yönlendiriliyor");
						Sleep(1500);

						system("CLS");

						break;
					}
					break;
					
					case 2://Çıkış Mesajı
						printf("\nHoscakalin. Yine Bekleriz..\n\n");

						break;
		}
						if(secim1==2)// Menüde Çıkış Seçilirse Çıkmak İçin
							return 0;
	}
							system("pause");
							return 0;
}
							
