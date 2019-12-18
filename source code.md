#include<iostream>
#include<conio.h>
#include<process.h>
#include<fstream>
#include<windows.h>
#include<ctime>
#include<cstdlib>

using namespace std;

void rprint()
{
 // font size change 
  
	CONSOLE_FONT_INFOEX cfi;
	cfi.cbSize = sizeof(cfi);
	cfi.nFont = 0;
	cfi.dwFontSize.X = 0;                   // Width of each character in the font
	cfi.dwFontSize.Y = 24;                  // Height
	cfi.FontFamily = FF_DONTCARE;
	cfi.FontWeight = FW_NORMAL;
	std::wcscpy(cfi.FaceName, L"Consolas"); // Choose your font
	SetCurrentConsoleFontEx(GetStdHandle(STD_OUTPUT_HANDLE), FALSE, &cfi);
   
   			cout<<"Enter { 0 } for exiting the program";
    		cout<<endl<<endl;
    		cout<<"Enter { 1 } for existing the item rate entry";
    		cout<<endl<<endl;
			cout<<"Enter { 2 } for renter the rates or aborting previous token";
     		cout<<"\n\n\nPress enter to continue - ";
    		getch();
    		system("cls");
   
   			float sale[10000];
    		for(int i=0;i<10000;i++)
     			{
    	 			 sale[i]=0;
				}
    		int i;
   			int q=0;
    		for(int g=0;g<10000;g++)
    		{
 

    			float rate[100];
    			float sumtotal=0;
    			float moneygive=0;
    			float moneychange=0;
    			float amount[100];
				float tempo[100];
   
   


				y : ;                 //goto y
   

    			int i;
    			int m=0;

    			for(i=0;i<100;i++)
    			{
       			 rate[i]=0;
        		 amount[i]=0;
    			}
    			for(i=1;i<=100;i++)
    			{
    			system("cls");
        			cout<<"\nenter the rate - ";
        			cin>>rate[i];
       


       	if(rate[i]==1)
        {
            goto ex;
        }
       
        else
            if(rate[i]==0)
            {
                goto x;
            }
            else
            if(rate[i]==2)
{
goto y;
}
            cout<<"\nenter amount - ";
        cin>>amount[i];
            m++;
           

        cout<<"\n\n"<<rate[i]<<"   ||   "<<amount[i];
        cout<<"\n\nOK";
        cout<<"\n\npress enter to continue ";
        getch();
        system("cls");

    }
    ex : ;

    system("cls");

    for(i=1;i<=m;i++)
    {  
   
    tempo[i]=rate[i]*amount[i];
        sumtotal=sumtotal+tempo[i];    
}
 

    cout<<"SUM TOTAL = "<<sumtotal;

    cout<<"\n\npress enter to continue - ";
    getch();

    system("cls");

    srand (time (0));                    //for generating truely random numbers 
//or you can use srand (time (NULL));





//ENTERING PRINTING MODE 
			    for(i=1;i<=m;i++)
			    {
			    ofstream file;
				file.open("SHOP_NAME.txt");             //SHOP NAME 

			{

			file<<"\n***************************\n   ";    
			file<<"\n";
			file<<"!Thank you for your purchase!\n\n\n";
			file<<"TOKEN AMOUNT = "<<tempo[i];
			file<<"\n\n\n"<<rate[i]<<"*"<<amount[i];
			long int randNum , randMax , randMin ;
			randMax=999999;
			randNum=1;
			randMin=111111;

			randNum = rand () % (randMax - randMin) + randMin;

			file<<"\n\nunique LID number -\n ";
			file<<randNum;

			file<<"\n\n**************************\n\n";
			   time_t now = time(0);
			   char* dt = (ctime(&now));
			   file << dt << endl;
			file.close();
			system("notepad /p SHOP_NAME.txt");
			printf("\nprinting");
			system("cls");
			}}
    

	cout<<"finished !!!!!!";
    cout<<"\n\npress enter to continue  - ";
    getch();
    system("cls");
           z : ;
       }
    x : ;
    system("cls");
    double saleop=0;
    for(int g=0;g<q;g++)
    {
    saleop = saleop + sale[g];
    }
    cout<<"sale - "<<saleop<<endl<<endl;
    cout<<"press enter to continue";
    getch();
}


int main()
{
rprint();
system("cls");
cout<<"you are existing the program >>>>>>>>>>>>>>> press enter to exit !";
getch();

return 0;
}


