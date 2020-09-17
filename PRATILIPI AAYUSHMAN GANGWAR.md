# Pratilipi-Assignment
#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<string.h>
void main()
{
	clrscr();
	int tit[3];
	for (int k=0;k<3;k++)
	{
		tit[k]=0;
	}
	int uchoice,tno;
	char title[3][50]={"day and night","birds","bubbles"};
	char content[3][80]={"day and nights are checked by calendar and clock",
											 "birds are animals that fly",
											 "bubbles are formed by surface tension"};
	int nop=0;
	int un,i,flag=0,flag1=0;
	char username[5][20]={"aayushman","abhishek","rahul","kirat","vansh"};
	char password[5][20]={"aayush","abhi","rah","kir","van"};
	char user1[20];
	char pass1[20];
	char ans;
	do
	{
		cout<<"\nNumber of persons seeing the story: "<<nop<<endl;
		cout<<"\n........................................................\n";
		cout <<"ENTER THE USERNAME:";
		gets(user1);
		cout<<"\n........................................................\n";
		for (i=0;i<5;i++)
		{
			if (strcmp(username[i],user1)==0)
			{
				flag=1;
				un = i;
				break;
			}
		}
		if (flag==0)
		{
			cout<<"Username is incorrect!!!!!";
		}
		else if (flag==1)
		{
			cout<<"Enter the password:";
			gets(pass1);
			if (strcmp(password[un],pass1)==0)
			{
				flag1=1;
			}
			if (flag1==0)
			{
				cout<<"\n........................................................\n";
				cout<<"Password is incorrect!!!!!";
				cout<<"\n........................................................\n";
			}
		}
		if (flag==1 && flag1==1)
		{
			cout<<"\n........................................................\n";
			cout<<"\n------Welcome for Story View------\n";
			cout<<"\n........................................................\n";
			cout<<"\n1. See the story";
			cout<<"\n2. Exit";
			cout<<"\n........................................................\n";
			cout<<"\n Enter the choice:";
			cin>>uchoice;
			cout<<"\n........................................................\n";
			switch (uchoice)
			{
				case 1:
								for (i=0;i<3;i++)
								{
									cout<<"\n"<<i+1<<" : "<<title[i];
								}
								cout<<"\nEnter the title number to see the story:";
								cin>>tno;
								cout<<"\nNumber of people seeing the story: "<<tit[tno-1];
								tit[tno-1]+=1;
								cout<<"\n........................................................\n";
								cout<<"\nStory is:\n";
								cout<<"\n........................................................\n";
								cout<<content[tno-1];
								cout<<"\n........................................................\n";
				break;
				case 2:
								cout<<"\nExiting!!!!!";
								cout<<"\n........................................................\n";
				break;
				default : cout<<"\nWrong choice!!!!!";
			}
			nop++;
			cout<<"\nNumber of users visited till now : "<<nop;
			cout<<"\nWant another user to continue(y/n)? ";
			cin>>ans;
		}
		getch();
		clrscr();
	}while(ans=='y'||ans=='Y');
	cout<<"\nTitle\t\tNumber of user viewed:\n";
	for(k=0;k<3;k++)
	{
		cout<<"\n........................................................\n";
		cout<<"\n"<<title[k]<<"\t\t\t"<<tit[k];
	}
	getch();
}


