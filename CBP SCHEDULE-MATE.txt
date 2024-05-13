//CBP SCHEDULE-MATE
#include<stdio.h>
#include<conio.h>
#include<math.h>
#include<string.h>
#include<unistd.h>
#include<stdlib.h>
#include<time.h>
#include<windows.h>
int yr,dt,day,mon,y;
char ch,dayrem[20],b;
int dayr(int dt,int mon,int yr)
{   
int i;
 char s;  
int k,m,h,c,c1,y;
system("cls");
if(yr%4==0&&yr%100!=0||yr%400==0)
{ 
k=yr%100;
y=yr%100;
y/=4;
y += dt;
switch(mon)
{ case 1 : m=1;
break;
 case 2 : m=4;
break;
 case 3 : m=4;
break;
 case 4 : m=0;
break;
 case 5 : m=2;
break;
 case 6 : m=5;
break;
 case 7 : m=0;
break;
 case 8 : m=3;
break;
 case 9 : m=6;
break;
 case 10: m=1;
break;
 case 11 : m=4;
break;
 case 12 : m=6;
break;
}
y += m;
if(mon==1||mon==2)
y -= 1;
if(yr>=1700&&yr<2100)
c=yr/100;
else 
{
while (yr>=1700&&yr<2100)
yr -= 400;
c = yr/100;
}
switch(c)
{ case 17 : c1=4;
break;
case 18 : c1=2;
break;
case 19 : c1=0;
break;
case 20 : c1=6;
break;
}
y += c;
y += k;
y %= 7;
day = y;
switch(y)
{ case 0 :printf("Saturday\n");
           break;
case 1 : printf("Sunday\n");
           break;
 case 2 : printf("Monday\n");
           break;
 case 3 : printf("Tuesday\n");
           break;
case 4 : printf("Wednesday\n");
           break;
case 5 : printf("Thursday\n");
           break;
case 6 : printf("Friday\n");
           break;
	
}
}
else 
{
y=yr%100;
c=yr/100;
if(mon<=12&&mon>=1) 
switch(mon)
{ case 1 : m=13;
           y=y-1;
           break;
case 2 : m=14;
         y=y-1;
        break;
default : m=mon;
           break;
}
else 
printf("\nEntered month is Invalid\n");
h=dt + ((13*(m+1))/5) + ((5*y)/4) + ((21*c)/4);
h=h%7;
day = h;
switch(h)
{ case 0 : printf("Saturday\n");
           break;
case 1 :   printf("Sunday\n");
           break;
 case 2 : printf("Monday\n");
           break;
 case 3 : printf("Tuesday\n");
           break;
case 4 : printf("Wednesday\n");
           break;
case 5 : printf("Thursday\n");
           break;
case 6 : printf("Friday\n");
           break;
}
}
return day;
}

//MAIN//
int main()
{ HANDLE h=GetStdHandle(STD_OUTPUT_HANDLE);
 int n,i,j,p=1,d1,o,o1;
 char q;
 int dayr(int,int,int);

 do
 {  system("cls");  
 printf("******************************************************************\n");
 printf("\n");

 printf("                ");
 SetConsoleTextAttribute(h,6);
  printf("!!");
   SetConsoleTextAttribute(h,15);
 printf("S");
  SetConsoleTextAttribute(h,12);
printf("C");
 SetConsoleTextAttribute(h,15);
 printf("H");
  SetConsoleTextAttribute(h,12);
printf("EDULE-");
 SetConsoleTextAttribute(h,15);
 printf("M");
  SetConsoleTextAttribute(h,12);
  printf("ATE");
   SetConsoleTextAttribute(h,6);
   printf("!!");
 printf("\n");
  SetConsoleTextAttribute(h,15);
 printf("___________________________________________________________________\n");
 printf("\n"); 
 SetConsoleTextAttribute(h,15);
 printf("\n SELECT OPTION : \n");
 SetConsoleTextAttribute(h,3);
 printf("\n 1.) MENU \n");
 SetConsoleTextAttribute(h,12);
 printf("\n 2.) REMINDER \n");
 SetConsoleTextAttribute(h,6);
 printf("\n 3.) HELP\n");
 SetConsoleTextAttribute(h,10);
 printf("\n 4.) ABOUT US \n");
 SetConsoleTextAttribute(h,14);
 printf("\n 5.) CONTACT \n");
 SetConsoleTextAttribute(h,15);
 printf("\n 6.) FEEDBACK\n");
 SetConsoleTextAttribute(h,11);
 printf("\n 7.) REPORT \n");
 SetConsoleTextAttribute(h,13);
 printf("\n 8.) EXIT\n");
 scanf("%d",&o1);
 SetConsoleTextAttribute(h,14);
 system("cls");
 if(o1==1)
 {
 Z:system("cls");
	n=0;
 	i=0;
 	j=0;
 	p=1;
 	d1=0;
 	o=0;
 	yr=0;
 	dt=0;
 	day=0;
 	mon=0;
 	y=0;
 	SetConsoleTextAttribute(h,10);
printf("\nEnter 1 For Day predictor: \n");
SetConsoleTextAttribute(h,11);
printf("\nEnter 2 For Printing Calender: \n");
SetConsoleTextAttribute(h,12);
printf("\nEnter 3 For Creating ToDo List: \n");
SetConsoleTextAttribute(h,13);
printf("\nEnter 4 For ADDING Tasks To ToDo list: \n");
SetConsoleTextAttribute(h,14);
printf("\nEnter 5 For Viewing the ToDo list: \n");
SetConsoleTextAttribute(h,9);
printf("\nEnter 6 To Create a Reminder list: \n");
SetConsoleTextAttribute(h,15);
printf("\nEnter 7 To Return to Main Menu:\n");
scanf("%d",&o);
 if(o==1)
 { system("cls");
 printf("DAY PREDICTOR : \n");
 printf("\n");
 printf("************************************************************************************************************************\n");
 printf("\n");
 SetConsoleTextAttribute(h,10);
 printf("\nEnter Date,Month,Year by seperating them with spaces: \n");
scanf("%d%d%d",&dt,&mon,&yr);
printf("**************************************************************************************************************************\n");
day=dayr(dt, mon, yr);
SetConsoleTextAttribute(h,15);
printf("Press Enter to Return to MENU");
fflush(stdin);
scanf("%c",&b);
if(b=='\n')
 goto Z;
 }
else if(o==2)
{ system("cls");
printf("CALENDER : \n");
printf("\n");
printf("****************************************************************************************************************************\n");
printf("\n");
SetConsoleTextAttribute(h,11);
printf("\nEnter Month and Year by seperating them with spaces: \n");
scanf("%d%d",&mon,&yr);
printf("*****************************************************************************************************************************\n");
printf("\n");
dt=1;
day= dayr(dt,mon,yr);
switch(mon)
{ case 1 : n=31;
break;
 case 2 : if(yr%4==0&&yr%100!=0||yr%400==0)
            n=29;
            else 
            n=28;
break;
 case 3 : n=31;
break;
 case 4 : n=30;
break;
 case 5 : n=31;
break;
 case 6 : n=30;
break;
 case 7 : n=31;
break;
 case 8 : n=31;
break;
 case 9 : n=30;
break;
 case 10: n=31;
break;
 case 11 : n=30;
break;
 case 12 : n=31;
break;
}
SetConsoleTextAttribute(h,10);
if(day==0)
d1=6;
else 
d1=day-1;
char cal[7][7]={'S','M','T','W','t','F','s'};
for(i=0;i<1;i++)
for(j=0;j<7;j++)
printf("%c   ",cal[i][j]);
printf("\n");
for(i=1;i<2;i++)
for(j=0;j<d1;j++)
{ 
cal[i][j]=' ';
printf("%c   ",cal[i][j]);
}
SetConsoleTextAttribute(h,14);
for(i=1;i<2;i++)
for(j=d1;j<7;j++)
if(p<=n)
 { cal[i][j]=p;
 printf("%d",cal[i][j]);
 switch(p)
 {case 1 : printf("   ");
break;
 case 2 : printf("   ");
break;
 case 3 : printf("   ");
break;
 case 4 : printf("   ");
break;
 case 5 : printf("   ");
break;
 case 6 : printf("   ");
break;
 case 7 : printf("   ");
break;
 case 8 :printf("   ");
break;
case 9 :printf("   ");
break;
default : printf("  ");
 }
p++;
}
printf("\n");
for (i=2;i<7;i++)
{
for(j=0;j<7;j++)
 if(p<=n)
 { cal[i][j]=p;
 if(j==0)
 {
 SetConsoleTextAttribute(h,12);
 printf("%d",cal[i][j]);}
 else
 {
 SetConsoleTextAttribute(h,14);
 printf("%d",cal[i][j]);}
switch(p)
 {case 1 : printf("   ");
break;
 case 2 : printf("   ");
break;
 case 3 : printf("   ");
break;
 case 4 : printf("   ");
break;
 case 5 : printf("   ");
break;
 case 6 : printf("   ");
break;
 case 7 : printf("   ");
break;
 case 8 :printf("   ");
break;
case 9 :printf("   ");
break;
default : printf("  ");
 }
p++;
}
printf("\n");
}
SetConsoleTextAttribute(h,15);
printf("______________________________________________________________________________________________________________________________\n");
printf("Press Enter to Return to MENU");
fflush(stdin);
scanf("%c",&b);
if(b=='\n')
 goto Z;
}

if(o==3)
{char c;
system("cls");
printf("TO-DO-LIST CREATOR : \n");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
SetConsoleTextAttribute(h,4);
printf("\nEnter Date in DD-MM-YYYY Format\n");
scanf("%s",dayrem);
FILE *fptr;
if(access(dayrem,F_OK)==0)
{
printf("\nThe Entered file to the respective data already exists...please give a valid date\n");
printf("\nThe Existing Date has tasks as follows:\n");
	FILE *ef;
	ef=fopen(dayrem,"r");
	if(ef==NULL)
	 printf("\nFile doesn't exist\n");
	else
	{ef=fopen(dayrem,"r");
		while(feof(ef)==0)
		{
			c=getc(ef);
			printf("%c",c);
		}
	}
	fclose(ef);
}
else
{fptr=fopen(dayrem,"w");
if(fptr==NULL)
printf("\nCould not create file\n");
printf("\nFile of respective date is created\nPlease Enter Task and ctrl+z to stop\n");
while ((ch=getchar())!=EOF)
fputc(ch,fptr);
fclose(fptr);
}
SetConsoleTextAttribute(h,15);
printf("Press Enter to Return to MENU");
fflush(stdin);
scanf("%c",&b);
if(b=='\n')
 goto Z;
}
if(o==5)
{   system("cls");
	char fname[20],c;
	FILE *vf;
	printf("TO-DO-LIST VIEWER : \n");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
	SetConsoleTextAttribute(h,14);
	printf("\nEnter Date in DD-MM-YYYY Format to see to do list\n");
	scanf("%s",fname);
	printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
	vf=fopen(fname,"r");
	if(vf==NULL)
	 printf("\nFile doesn't exist\n");
	else
	{   SetConsoleTextAttribute(h,12);
		while(feof(vf)==0)
		{
			c=getc(vf);
			printf("%c",c);
		}
	}
	fclose(vf);
	printf("_________________________________________________________________________________________________________________________________________________\n");
	printf("\n");
	SetConsoleTextAttribute(h,15);
	printf("Press Enter to Return to MENU");
	fflush(stdin);
scanf("%c",&b);
if(b=='\n')
 goto Z;
}
if(o==4)
  { char fname[20],c;
  	FILE *af;
  	system("cls");
  	printf("TO-DO-LIST EDITOR : \n");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
  	SetConsoleTextAttribute(h,13);
  	printf("\nEnter Date in DD-MM-YYYY Format to add tasks\n");
  	scanf("%s",fname);
  	printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
  	af=fopen(fname,"a");
  	printf("Enter task that you want to add\n");
  	while((c=getchar())!=EOF)
  	 fputc(c,af);
  	 fclose(af);
  	 	printf("_________________________________________________________________________________________________________________________________________________\n");
	printf("\n");
  	 SetConsoleTextAttribute(h,15);
	   printf("Press Enter to Return to MENU");
	   fflush(stdin);
scanf("%c",&b);
if(b=='\n')
 goto Z;	 
  }
if(o==6)
{
	   char c,l,q[20],d[3],m[3],y[5],h[3],min[3],sec[3],final[20]={"\0"};
 FILE *fp;
 system("cls");
 	printf("REMINDER LIST CREATOR : \n");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
 SetConsoleTextAttribute(h,11);
 printf("\nGive file in the format Date-Month-Year<space>hours_minutes\nMake sure you not give zero's(i.e dont give 0 before any single digit number )\n");
  Q:
  printf("\nEnter a file name and click enter to create\n");
  fflush(stdin);
  scanf("%[^\n]s",q);
  fp=fopen(q,"w");
  fflush(stdin);
  printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
  printf("Enter the task\n");
  while((c=getchar())!=EOF)
  fputc(c,fp);
  fclose(fp);
  printf("_________________________________________________________________________________________________________________________________________________\n");
  printf("\n");
  SetConsoleTextAttribute(h,4);
  printf("Do u want to Create another file press 'Y'/'y' or Or Else Press 'N'/'n'\n");
  fflush(stdin);
  scanf("%c",&l);
  printf("___________________________________________________________________________________________________________________________________________________\n");
  printf("\n");
  if(l=='y'||l=='Y')
  goto Q;
  else
  {
  printf("____________________________________________________________________________________________________________________________________________________\n");
  printf("\n");
  SetConsoleTextAttribute(h,15);
  printf("Press Enter to Return to MENU");
  fflush(stdin);
scanf("%c",&b);
if(b=='\n')
 goto Z;
}
}

}
if(o1==2)
{ FILE *fp;
	//REMINDER//
    char c,q,d[3],m[3],y[5],h[3],min[3],sec[3],final[20]={"\0"};
	SYSTEMTIME t;
printf("REMINDER HAS BEEN STARTED !!!\n");
printf("ALARM WILL BE PLAYED AND YOU WILL BE REMINDED AS PER YOUR SAVED TASKS : \n");
printf("PLEASE OPEN THE APPLICATION AGAIN TO CONTINUE WITH OTHER OPTIONS\n(Make Sure you not close this application)");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
	SetConsoleTextAttribute(h,12);
	while(1)
	{
	GetLocalTime(&t); 
	sprintf(d,"%d",t.wDay);
	sprintf(min,"%d",t.wMinute);
	sprintf(h,"%d",t.wHour);
	sprintf(m,"%d",t.wMonth);
	sprintf(y,"%d",t.wYear);
	strcpy(final,d);
	strcat(final,"-");
    strcat(final,m);
	strcat(final,"-");
	strcat(final,y);
	strcat(final," ");
	strcat(final,h);
	strcat(final,"_");
	strcat(final,min);
	fp=fopen(final,"r");
	 if(fp!=NULL)
		{
		while((c=getc(fp))!=EOF)
		{
		SetConsoleTextAttribute(h,14);
		printf("%c",c);
        }
		printf("\nPress 'Q' to stop the song\n");
    PlaySound(TEXT("avengers.wav"),NULL,SND_FILENAME|SND_LOOP|SND_ASYNC);  
    fflush(stdin);
	scanf("%c",&q);
	if(q=='Q'||q=='q')
	 PlaySound(0,0,0); 
		fclose(fp);}
    sleep(60);}
}

if(o1==3)
{FILE *h;
char m1,E;
system("cls");
printf("HELP : \n");
printf("FREQUENTLY ASKED QUESTIONS (FAQ'S)\n");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
h=fopen("HELP(FAQ_S).txt","r");
SetConsoleTextAttribute(h,14);
while(feof(h)==0)
		{
			m1=getc(h);
			printf("%c",m1);
		}
fclose(h);
printf("____________________________________________________________________________________________________\n");
printf("Press any key to return to MAIN MENU : ");
fflush(stdin);
scanf("%c",&E);
}


if(o1==4)
 {  char a;
 system("cls");
 SetConsoleTextAttribute(h,12);
	printf("ABOUT US : \n");
	printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
SetConsoleTextAttribute(h,14);
	printf("\nThe Schedule-mate involves a remainder application with functionality of alarm embedded with day planner and a calendar in combination with a day predictor. \n");
	printf("We help the user in planning his  schedule and remind them at the planned time or prior to it.\n");
	printf("It is a console application created as a part of our major graduate during the Under Graduation program(B-TECH) at VNRVJIET in the stream of CSE.");	
printf("\n");
    printf("The schedule-mate application accredits the user to opt for a selective preference which are : \n");
printf("1.) Day predictor \n");
printf("2.) Monthly Calender \n");
printf("3.) Make/View a  To-do list\n");
printf("4.) A Reminder Alarm \n");
printf("This enables the user to plan or complete their tasks without any truancy.\n" );
 printf("In our current chaotic lives it may be used for a convenient completion of tasks according to the scheduled plan.\n");
printf("We have our own organistaion/team name as SHM. For any queries you can also contact us through team mail\n");
printf("\n");
printf("\n");
printf("******************************************************************************************************************************\n");
printf("\n");
printf("\n");
printf("ORGANISATION DETAILS :\n");
printf("\n");
printf("NAME : SHM\n");
printf("\n");
printf("_______________________________________________________________________________________________________________________________\n");
printf("\n");
printf("TEAM MEMBERS :\n");
printf("\n");
printf("1.) T.SAI SUSHANTH\n");
printf("2.) L.HARI CHARAN\n" );
printf("3.) S.MAYAN BRAHMAM\n");
printf("\n");
printf("********************************************************************************************************************\n");
printf("Press any key to return to Main Menu : ");
fflush(stdin);
scanf("%c",&a);
}

if(o1==5)
{FILE *cu;
char m3,C;
SetConsoleTextAttribute(h,10);
printf("CONTACT US : \n");
printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
cu=fopen("CONTACT US.txt","r");
SetConsoleTextAttribute(h,14);
while(feof(cu)==0)
		{
			m3=getc(cu);
			printf("%c",m3);
		}
fclose(cu);
printf("____________________________________________________________________________________________________\n");
printf("Press any key to return to MAIN MENU : ");
fflush(stdin);
scanf("%c",&C);
}

if(o1==6)
{FILE *fe;
char m4,name[20],F,n1[5]="FBK";
SetConsoleTextAttribute(h,5);
	printf("FEEDBACK COLLECTOR : \n");
	printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
SetConsoleTextAttribute(h,11);
printf("ENTER USERNAME : ");
scanf("%s",name);
strcat(name,n1);
fe=fopen(name,"w");
printf("\n PLEASE GIVE YOUR FEEDBACK.....IT MEANS A LOT TO US\n");
printf("\n Click Ctrl+z to terminate\n");
while((m4=getchar())!=EOF)
fputc(m4,fe);
fclose(fe);
printf("THANK YOU FOR THE FEEDBACK!!\n");
printf("Kindly Forward the (username)FBK file to the Mail provided!(shm181407@gmail.com)\n");
printf("____________________________________________________________________________________________________\n");
printf("\n");
printf("Press any key to return to MAIN MENU : ");
fflush(stdin);
scanf("%c",&F);
}

if(o1==7)
{FILE *re;
SetConsoleTextAttribute(h,10);
char m5,R,name1[20],n2[5]="REP";
	printf("REPORT COLLECTOR : \n");
	printf("\n");
printf("*************************************************************************************************************************************************\n");
printf("\n");
SetConsoleTextAttribute(h,6);
printf("ENTER USERNAME : ");
scanf("%s",name1);
strcat(name1,n2);
re=fopen(name1,"w");
printf("\n PLEASE NOTIFY US WITH THE BUGS THAT YOU COME ACROSS WHILE USING SCHEDULE-MATE\n");
printf("\n Click Ctrl+Z to stop \n");
while((m5=getchar())!=EOF)
fputc(m5,re);
fclose(re);
printf("THANK YOU FOR THE REPORT.WE WILL PUT OUR COMPLETE EFFORTS IN RESOLVING THE ISSUE!!\n");
printf("Kindly forward the (username)REP file to the mail provided!(shm181407@gmail.com)\n");
printf("____________________________________________________________________________________________________\n");
printf("\n");
printf("Press any key to return to MAIN MENU : ");
fflush(stdin);
scanf("%c",&R);
}
}
while(o1<=7);
return 0;

}