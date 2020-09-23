<div align="center">

## link list 2\.0


</div>

### Description

Performs all the operations of a singly linked list.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Syed Yasir Imtiaz](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/syed-yasir-imtiaz.md)
**Level**          |Beginner
**User Rating**    |5.0 (25 globes from 5 users)
**Compatibility**  |C
**Category**       |[Data Structures](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/data-structures__3-8.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/syed-yasir-imtiaz-link-list-2-0__3-8102/archive/master.zip)





### Source Code

```
#include<iostream.h>
#include<graphics.h>
#include<process.h>
#include<conio.h>
#include<stdio.h>
#include<dos.h>
void node();
void create();
void insert();
void fr_insert();
void la_insert();
void bet_insert();
void bef_insert();
void af_insert();
void deleat();
void fr_deleat();
void la_deleat();
void bet_deleat();
void same_deleat();
void bef_deleat();
void aft_deleat();
int search();
void ascend();
void descend();
void display();
void horizontal(char z,char z1,char z2,char chr) // to draw horizontal line
 {
 for(int i=z1;i<=z2;i++)
 {
 gotoxy(i,z); printf("%c",chr);
 }
 }
void vertical(char z ,char z1,char z2,char chr) //to draw horizontal line
 {
 for(int i=z1;i<=z2;i++)
 {
 gotoxy(z,i); printf("%c",chr);
 }
 }
void yasir(int cls,int rs,int cle,int re)
   {
	gotoxy(cls,rs);textcolor(1);cprintf("Ú");
	gotoxy(cls+cle+1,rs);cprintf("¿");
	gotoxy(cls+cle+1,rs+re+1);cprintf("Ù");
	gotoxy(cls,rs+re+1);cprintf("À");
	textcolor(15);
	vertical(cls,rs+1,rs+re,'³'); //"456 È" "442º" " 4441/4 "
	vertical(cls+cle+1,rs+1,rs+re,'³');
	horizontal(rs,cls+1,cls+cle,'Ä');
	horizontal(rs+re+1,cls+1,cls+cle ,'Ä');
   }
struct link
{
int n;
link *next;
};
link *h=NULL,*t,*l=NULL,*s,*sb,*sbb;
/////////////////////////////////////////////////////////////////////
void main()
 {
 int choice;
 do
 {
 clrscr();
    yasir(5,3,74,44);
    yasir(26,4,30,1);
    gotoxy(32,5);
    printf("L I N K E D L I S T ");
    yasir(22,45,38,1);
    gotoxy(28,46);
    printf("Syed Yasir Imtiaz ... Bcs-3");
    int rs=11;
    yasir(7,7,16,27);
    for(int i=0;i<6;i++)
    {
    horizontal(rs,8,23,'Ä');
    rs+=4;
    }
 gotoxy(9,9);
 printf("1.C r e a te ");
 gotoxy(9,13);
 printf("2.I n s e r t ");
 gotoxy(9,17);
 printf("3.D e l e t e ");
 gotoxy(9,21);
 printf("4.D i s p l a y");
 gotoxy(9,25);
 printf("5.S o r t  ");
 gotoxy(9,29);
 printf("6.S e a r c h ");
 gotoxy(9,33);
 printf("7.E x i t  ");
 gotoxy(8,37);
 printf("Enter your choice");
 gotoxy(8,39);
 scanf("%d",&choice);
 switch(choice)
  {
case 1:
	yasir(25,7,51,35);
	yasir(38,8,23,2);
	gotoxy(44,10);
	cout<<"CREATE A LIST";
	create();
	break;
case 2:
	yasir(25,7,51,35);
	yasir(38,8,23,2);
	gotoxy(44,10);
	cout<<"INSERT A NODE";
	insert();
    break;
case 3:
	yasir(25,7,51,35);
	yasir(38,8,23,2);
	gotoxy(44,10);
	cout<<"DELETE THE NODE";
	deleat();
	break;
case 4:
	clrscr();
	yasir(1,1,77,48);
	yasir(28,2,22,1);
	gotoxy(31,3);
	cout<<"DISPALY THE LIST";
	display();
   break;
case 5:
	yasir(25,7,51,35);
	yasir(38,8,23,2);
	gotoxy(44,10);
	cout<<"SORT THE LIST";
	yasir(26,12,20,3);
	yasir(55,12,20,3);
	gotoxy(28,14);
	printf("1.Ascending Order");
	gotoxy(57,14);
	printf("2.Descending Order");
	int b;
	gotoxy(27,18);
	printf("Enter Choice");
	gotoxy(27,19);
	scanf("%d",&b);
switch(b)
 {
  case 1:
	ascend();
	display();
   break;
  case 2:
	descend();
	display();
   break;
  }
  gotoxy(26,40);
  printf("Press Any Key To Continue...");
  getch();
  clrscr();
  break;
case 6:
	yasir(25,7,51,35);
	yasir(38,8,23,2);
	gotoxy(44,10);
	cout<<"SEARCH THE LIST";
	search();
	getch();
	break;
case 7:
exit(0);
break;
}    // End Switch
}    // End While
while(choice!=0);
char ch;
 do
 {
 create();
 ch=getch();
 }
 while(ch=='y'||ch=='Y');
} // End Main
///////////////////////////////////////////////////////////
void create()
 {
 int a=36,b=14;
 t=new link;
 gotoxy(a,b);
 printf("Enter value for n");
 gotoxy(a,b+1);
 scanf("%d",&t->n);
 t->next=h;
 h=t;
 }
////////////////////////////////////////////
void display()
 {
 int ct=0,a1=2,b1=6,c1=10,d1=2;
 t=h;
 while(t->next!=NULL)
 {
 ct++;
 if(ct>4&&ct<6||ct>8&&ct<10||ct>12&&ct<14||ct>16&&ct<18||ct>20&&ct<22)
 a1=2,b1+=5;
 yasir(1,1,77,48);
 yasir(a1,b1,c1,d1);
 yasir(a1,b1,c1-8,d1);
 gotoxy(a1+12,b1+2);
 printf("-->");
 gotoxy(a1+1,b1+2);
 printf("%d",t->n);
 gotoxy(a1+5,b1+2);
 printf("%d",t->next);
 delay(500);
 t=t->next;
 a1+=15;c1+=0;
 }
 if(t->next==NULL)
 yasir(a1,b1,c1,d1);
 yasir(a1,b1,c1-8,d1);
 gotoxy(a1+1,b1+1);
 gotoxy(a1+1,b1+2);
 printf("%d",t->n);
 gotoxy(a1+5,b1+2);
 printf("%d",t->next);
 getch();
}
////////////////////////////////////////////
void insert()
{
yasir(26,12,15,3);
yasir(43,12,14,3);
yasir(59,12,16,3);
gotoxy(28,14);
printf("1.Front Insert");
gotoxy(45,14);
printf("2.Last Insert");
gotoxy(60,14);
printf("3.Between Insert");
int b;
gotoxy(27,18);
printf("Enter Choice");
gotoxy(27,19);
scanf("%d",&b);
switch(b)
{
 case 1:
	clrscr();
	yasir(25,7,51,35);
	yasir(37,8,25,2);
	gotoxy(44,10);
	printf("FRONT INSERT");
	while(t!=NULL)
	{
	t=t->next;
	}
	t=new link;
	gotoxy(29,14);
	cout<<"Enter the value for n";
	gotoxy(29,16);
	cin>>t->n;
	t->next=h;
	h=t;
	break;
 case 2:
	clrscr();
	yasir(25,7,51,35);
	yasir(37,8,25,2);
	gotoxy(44,10);
	printf("LAST INSERT");
	t=h;
	while(t!=NULL)
	{
	t=t->next;
	}
	t=new link;
	gotoxy(29,14);
	cout<<"Enter the value for n";
	gotoxy(29,16);
	cin>>t->n;
	t->next=h;
	h=t;
	break;
 case 3:
	clrscr();
	yasir(25,7,51,35);
	yasir(37,8,25,2);
	gotoxy(44,10);
	printf("BETWEEN INSERT");
	yasir(42,12,16,3);
	gotoxy(44,14);
	printf("After Insert");
	t=h;
	while(t!=NULL)
	{
	t=t->next;
	}
	int n;
	gotoxy(28,20);
	printf("Enter the Number after which you want to insert");
	gotoxy(28,22);
	cin>>n;
	 s=h;
	while((s!=NULL)&&(s->n!=n))
	{
	s=s->next;
	}
	if(s->n==n)
	{
	t=new link;
	gotoxy(28,28);
	printf("Enter Element to be inserted");
	gotoxy(28,30);
	cin>>t->n;
	t->next=s->next;
	s->next=t;
	}
} // End Switch
} // End Function
////////////////////////////////////////////
void deleat()
  {
  int k;
  yasir(26,12,15,3);
  yasir(43,12,14,3);
  yasir(59,12,16,3);
  gotoxy(28,14);
  printf("1.Front Delete");
  gotoxy(45,14);
  printf("2.Last Delete");
  gotoxy(60,14);
  printf("3.Between Delete");
  int b;
  gotoxy(27,18);
  printf("Enter Choice");
  gotoxy(27,19);
  scanf("%d",&b);
switch(b)
  {
  case 1:
	   clrscr();
	   yasir(25,7,51,35);
	   yasir(33,8,25,2);
	   gotoxy(40,10);
	   printf("FRONT DELETE");
	   fr_deleat();
	   break;
  case 2:
	   clrscr();
	   yasir(25,7,51,35);
	   yasir(33,8,25,2);
	   gotoxy(40,10);
	   printf("LAST DELETE");
	   la_deleat();
	   break;
  case 3:
	   clrscr();
	   yasir(25,7,51,35);
	   same_deleat();
	   break;
  } //End Switch
} // End Function
void fr_deleat()
  {
  t=h;
  s=t->next;
  delete h;
  h=s;
  }
void la_deleat()
{
s=h;
while(s!=NULL)
{
sbb=sb;
sb=s;
s=s->next;
}
delete sb;
sbb->next=NULL;
}
void same_deleat()
{
	yasir(37,8,25,2);
	gotoxy(44,10);
	printf("BETWEEN Delete");
	yasir(42,12,16,3);
	gotoxy(44,14);
	printf("SAME Delete");
s=h;
while(s!=NULL)
{
sbb=sb;
sb=s;
s=s->next;
}
delete sb;
sbb->next=NULL;
}
void bef_deleat()
{
sbb->next=s;
delete sb;
}
void aft_deleat()
{
sb=s->next;
s->next=sb->next;
delete sb;
}
////////////////////////////////////////////
   ////// SORTING FUNCTIONS ///////////
void ascend(void)
{
clrscr();
	yasir(1,1,77,48);
	yasir(28,2,22,1);
	gotoxy(31,3);
	cout<<"Ascending Order";
   t=h;
   int counter=0;
   while(t->next!=NULL)
	 {
	 t=t->next;
	 counter=counter+1;
	 }
   for(int j=0; j<counter; j++)
	 {
	 t=h;
	 while(t->next!=NULL)
	    {
	    if(t->n > t->next->n)
	    {
	    int temp;
	    temp=t->next->n;
	    t->next->n=t->n;
	    t->n=temp;
	    } // End If
	    else
	    t=t->next;
	    } // End While
	 } // End For
} //End Function
void descend(void)
{
clrscr();
	yasir(1,1,77,48);
	yasir(28,2,22,1);
	gotoxy(31,3);
	cout<<"Descending Order";
   t=h;
   int counter=0;
   while(t->next!=NULL)
	 {
	 t=t->next;
	 counter=counter+1;
	 }
   for(int j=0; j<counter; j++)
	 {
	 t=h;
	 while(t->next!=NULL)
	    {
	    if(t->n < t->next->n)
	    {
	    int temp;
	    temp=t->next->n;
	    t->next->n=t->n;
	    t->n=temp;
	    }  //End If
	    else
	    t=t->next;
	    } // End While
	 } // End For
}  // End Function
 int search()
  {
  int n;
  gotoxy(37,14);
  cout<<"Enter value to search";
  gotoxy(37,16);
  cin>>n;
  t=h;
  while( t!=NULL && t->n!=n)
   {
   sbb=sb;
   sb=t;
   t=t->next;
   }
  if(t->n==n)
   {
   gotoxy(37,18);
   cout<<"VALUE FOUND";
   return 1;
   }
  else
  {
  gotoxy(37,18);
  cout<<"VALUE NOT FOUND";
   return 0;
   }
}
     ////////// E N D O F P R O G R A M //////////
```

