//header files

#include<iostream.h>
#include<conio.h>
#include<fstream.h>
#include<process.h>
#include<math.h>
#include<string.h>
#include<ctype.h>
#include<iomanip.h>
#include<stdio.h>


void pattern1()           //function for border
{
 clrscr();
   char a='.';
for(int i=18;i<47;i++)
  {
   gotoxy(i,3);
   cout<<a;
  }
 for(i=18;i<47;i++)
 {
   gotoxy(i,23);
   cout<<a;
 }

 for(i=3;i<24;i++)
  {
   gotoxy(18,i);
   cout<<a;
  }
 for(i=4;i<24;i++)
  {
   gotoxy(46,i);
   cout<<a;
  }

}
void main();

class Reminders1                   //class for reminders
{
 char Reminder[50];                 //public members
 int no1;
 public :
 void Add(int k)                   //member function to input public members
 {
  no1=k; gotoxy(19,6);
  cout<<"\n \t\t .Enter the text :";
  cout<<"\n \t\t .";
  gets(Reminder);
 }

 int retno1()                      //member function to return no:
 {
  return no1;
 }
 char *retnote()                   //member function to return reminder
 {
  return Reminder;
 }
 void sort1(int n)                 //member function to assign nos to sort
 {
 no1=n;
 }
 void display()                     //member function to display
 {
  gotoxy(19,6);
  cout<<"\n \t\t ."<<no1<<'\n';
  gotoxy(19,8);
  puts(Reminder);
  cout<<"\n \t\t .";
 }
};

class Notes1                          //class for notes
{
 char Note[100];                       //private members
 int no;
 public :
 void Add(int k)                     //function to input data members
 {
   no=k;
   gotoxy(19,6);
   cout<<"\n \t\t .Enter the text:";
   cout<<"\n \t\t .";
   gets(Note);
 }
 void sort(int s)                  //member function to assign nos to sort
 {
  no=s;
 }
 char *retnote()                    //member function to return note
 {
  return Note;
 }
 int retno()                        //member function to return no
{ return no;
}
 void display()                     //member function to display
 { gotoxy(19,6);
  cout<<"\n \t\t .No: "<<no;
  cout<<"\n \t\t .";
  puts(Note);
  cout<<"\n \t\t .";
 }
};

class Contacts1                             //class for contacts
{
 char name[20];                              //private members
 char no[15];
 public :
 void Add()                                //function to input data members
 {
  gotoxy(19,6);
  cout<<"\n \t\t .Enter Name : ";
  gets(name);
  cout<<"\n \t\t .Enter number : ";
  gets(no);
 }

 char *retno()                   //member function to return no
 {
   return no;
 }
 char *retname()                   //member function to return name
 {
  return name;
 }
 void display()                         //member function to display
 {
  gotoxy(19,6);
  cout<<"\n \t\t .Name:: ";
  puts(name);
  cout<<"\n \t\t .Number:: ";
  puts(no);cout<<'\n';
 }
};

int csort()                     //function to sort all contacts
 {
 int k=0,j;
 ifstream f("contacts.dat",ios::binary);
 Contacts1 c,b,a[100];
 ofstream f1("temp.dat",ios::binary);
 for(int i=0;f.read((char*)&c,sizeof(c));i++)    //loop to check no of contacts
 {  a[i]=c;
    ++k;
 }

 for(i=0;i<k;i++)                               //sorting
 {
  for(j=0;j<k-i-1;j++)
   {
     if(strcmp(a[j].retname(),a[j+1].retname())>0)
      { b=a[j];
	a[j]=a[j+1];
	a[j+1]=b;
      }
   }
 }
 for(i=0;i<k;i++)
  f1.write((char*)&a[i],sizeof(a[i]));
  remove("contacts.dat");
  rename("temp.dat","contacts.dat");
  f1.close();
  return 0;
}

int nsort()                    //function to sort notes
{
 int k=0,j;
 ifstream f("notes.dat",ios::binary);
 Notes1 c,b,a[100];
 ofstream f1("temp.dat",ios::binary);
 for(int i=0;f.read((char*)&c,sizeof(c));i++)   //loop for checking no of notes
 {
  a[i]=c;
  ++k;
 }
 for(i=0;i<k;i++)                    //sorting
 {
  for(j=0;j<k-i-1;j++)
   {
     if(a[j].retno()>a[j+1].retno())
      { b=a[j];
	a[j]=a[j+1];
	a[j+1]=b;
      }
   }
 }
 for(i=0;i<k;i++)
 {
  a[i].sort(i);
  f1.write((char*)&a[i],sizeof(a[i]));
 }
 remove("notes.dat");
 rename("temp.dat","notes.dat");
 f1.close();
 return 0;
}

int rsort()                      //function to sort reminders
{
 int k=0,j;
 ifstream f("rem.dat",ios::binary);
 Reminders1 c,b,a[100];
 ofstream f1("temp.dat",ios::binary);
 for(int i=0;f.read((char*)&c,sizeof(c));i++)       //loop to check no of reminders
 {
  a[i]=c;
  ++k;
 }
 for(i=0;i<k;i++)                               //sorting
 {
  for(j=0;j<k-i-1;j++)
   {
     if(a[j].retno1()>a[j+1].retno1())
      { b=a[j];
	a[j]=a[j+1];
	a[j+1]=b;
      }
   }
 }
 for(i=0;i<k;i++)
 {
  a[i].sort1(i);
  f1.write((char*)&a[i],sizeof(a[i]));
 }
 remove("rem.dat");
 rename("temp.dat","rem.dat");f1.close();
 return 0;
}

int Contacts()                        //function for contacts
 {
  clrscr();
  Contacts1 co;                       //declaration
  int ch1;
  fstream fc;
  while(1)

 { clrscr();
  pattern1();
   gotoxy(19,6);
  cout<<"\t 1. SEARCH\n";
   gotoxy(19,8);
  cout<<"\t 2. ADD NEW\n";
   gotoxy(19,10);
  cout<<"\t 3. EDIT\n";
   gotoxy(19,12);
  cout<<"\t 4. DELETE\n";
   gotoxy(19,14);
  cout<<"\t 5. BACK\n";
   gotoxy(19,16);
 cin>>ch1;
 char name1[20];
 int flag=-1;
 switch(ch1)
 {
  case 1  : ifstream fs;            // searching
	    fs.open("contacts.dat",ios::binary);  //opening binary file
	    clrscr(); pattern1();               //calling pattern function
	    gotoxy(19,6);
	    cout<<"\n \t\t .Enter the name: ";
	    gets(name1);
	    while(fs.read((char*)&co,sizeof(co)))
	    {
	     if(strcmpi(name1,co.retname())==0)    //checking the required contact
	      {
		cout<<"\n \t\t .Number:: "<<co.retno();
		flag=0;
		break;
	      }
	     }
	     if(flag!=0)
	     cout<<"\n \t\t .NOT FOUND!!\n";
	    fs.close();                        //file close
	    break;

  case 2  :  Contacts1 co2;                   //declaration of object
	     fc.open("contacts.dat",ios::binary|ios::app); //opening file
	     clrscr(); pattern1();
	     co2.Add();          //calling Add() function
	     fc.write((char*)&co2,sizeof(co2));   //writing the record
	     fc.close();                          //file close
	      csort();                            //calling sort function
	    break;

  case 3  : fstream fr;
	    ofstream fw;     //declaration of stream object
	    Contacts1 co1;
	    char ch2;
	    fr.open("contacts.dat",ios::binary|ios::in|ios::out|ios::app); //opening contacts.dat
	    fw.open("temp.dat",ios::binary);                               //opening temp.dat
	    clrscr();
	    pattern1();
	    gotoxy(19,6);
	    cout<<"\n \t\t .Enter the name: ";
	    gets(name1);
	    while(fr.read((char*)&co1,sizeof(co1)))
	    {
	     if(strcmpi(name1,co1.retname())==0)  //checking the contact
	       {
		cout<<"\n \t\t .Number:: "<<co1.retno();
	       flag=fr.tellg();
	       }
	      else
		fw.write((char*)&co1,sizeof(co1));  //writing to temp.dat
	     }
	     if(flag==-1)
	     cout<<"\n \t\t .NOT FOUND!!\n";
	     else
	     {
	      fr.seekp(flag,ios::beg);
	      fr.read((char*)&co1,sizeof(co1)); //reading the record to be editted
	      clrscr();
	      pattern1();
	      co1.Add();
	      fw.write((char*)&co1,sizeof(co1)); //writing the editted record
	      cout<<"\n \t\t .Contact updated succesfully\n";
	     }
	      remove("contacts.dat");
	      rename("temp.dat","contacts.dat");
	    getch();
	    fw.close();             //file close
	    csort();                //calling sort function
	    break;

  case 4  : ifstream g("contacts.dat",ios::binary); //opening contacts.dat
	    Contacts1 cs;                           //declaration of object
	    int a;
	    char b1;
	    ofstream g1("temp.dat",ios::binary);   //opening temp.dat
	    clrscr();
	    pattern1();
	    gotoxy(19,6);
	    cout<<"\n \t\t .1.Delete by name";
	    cout<<"\n \t\t .2.Delete one by one\t";
	    cin>>a;    int h=1;
	    if(a==2)
	    {
		while(g.read((char*)&cs,sizeof(cs)))
		{  clrscr(); pattern1();
		   cs.display();             //display contacts
		   cout<<"\n \t\t .Delete?(Y or N)\t";
		   cin>>b1;
		   if(b1=='n'||b1=='N')
		   g1.write((char*)&cs,sizeof(cs));
		   if(b1=='Y'||b1=='y')
		   h=0;
		}
	       remove("contacts.dat");
	       rename("temp.dat","contacts.dat");
	       if(h==0)
	       cout<<"\n \t\t .Contact deleted successfully!\n";
	       else
	       cout<<"\n \t\t .NO CONTACTS DELETED!\n";
	       g1.close();              //file close
	       csort();                 //sort function called
	    }
	    if(a==1)                    //delete by name
	    { clrscr(); pattern1();
	      cout<<"\n \t\t .Enter the name: ";
	      gets(name1);
	      while(g.read((char*)&cs,sizeof(cs)))
	      {
		if(strcmpi(name1,cs.retname())==0) //checking the contact
		 {
		  flag=g.tellg();
		 }
		else
		g1.write((char*)&cs,sizeof(cs));
	      }
	       if(flag==-1)
	       cout<<"\n \t\t .NOT FOUND!!\n";
	       remove("contacts.dat");
	       rename("temp.dat","contacts.dat");
	       g1.close();                   //file close
	       csort();                      //sort function called
	    }
	    break;

  case 5  : main();    //back to main menu

 }

 getch();
}
 }
int nsort();

int Notes()                     //function for notes
 {
  Notes1 n;
  clrscr();
  fstream fn;
  int ch1;
 while(!0)
 {
  clrscr();
  pattern1();
   gotoxy(19,6);
  cout<<"\t 1. VIEW ALL\n";
   gotoxy(19,8);
  cout<<"\t 2. ADD NEW\n";
   gotoxy(19,10);
  cout<<"\t 3. EDIT\n";
   gotoxy(19,12);
  cout<<"\t 4. DELETE\n";
   gotoxy(19,14);
  cout<<"\t 5. BACK\n";
   gotoxy(19,16);
  cin>>ch1;
 switch(ch1)
 {
  case 1  : Notes1 c;
	    int p=0;
	    ifstream fn1;
	    fn1.open("Notes.dat",ios::binary|ios::in); //opening the file
	    clrscr();
	    pattern1();
	    while(fn1.read((char*)&c,sizeof(c)))
	    {
	     c.display();    //displaying notes
	     ++p;
	     getch();
	    }
	    if(p==0)
	    {
	    gotoxy(19,6);
	    cout<<"\n \t\t .No notes added!!";
	    }
	    fn1.close();                 //close file
	    getch();
	    break;

  case 2  : ifstream gr;
	    gr.open("Notes.dat",ios::binary|ios::in); //opening file
	    int k=-1;
	    clrscr();
	    pattern1();
	    while(gr.read((char*)&n,sizeof(n))) //loop to check no of notes
	     {
	       ++k;
	     }
	     gr.close();                       //file close
	     fn.open("Notes.dat",ios::binary|ios::out|ios::app);//opening the file again
	     n.Add(++k);                       //Add() function called
	     fn.write((char*)&n,sizeof(n));    //writing to file
	     fn.close();                       //closing file
	     nsort();                          //sort function called
	     break;

  case 3  : fstream fr1;
	    ofstream fw1;
	    Notes1 not,nota;
	    char b='p';
	    fr1.open("notes.dat",ios::binary|ios::in|ios::out|ios::app);   //opening notes.dat
	    fw1.open("temp.dat",ios::binary);                              //opening temp.dat
	    int no,no1;        //declaration
	    clrscr();
	    pattern1();
		while(fr1.read((char*)&not,sizeof(not)))
		{
		   not.display();          //display note
		   cout<<"\n \t\t .Edit?(Y or N)\t";
		   cin>>b;
		   clrscr();
		   pattern1();
		   if(b=='y'||b=='Y')
		   {  no=not.retno();
		      nota.Add(no);             //editing
		      fw1.write((char*)&nota,sizeof(nota)); //writing to file
		      no1=1;
		   }
		   if(b=='n'||b=='N')
		   fw1.write((char*)&not,sizeof(not));   //writing to file

		}
		gotoxy(19,6);
		if(b=='p')
		cout<<"\n \t\t .No Notes added!!";
	       remove("notes.dat");
	       rename("temp.dat","notes.dat");
	       if(no1==1)
	       cout<<"\n \t\t .Note updated successfully!\n";
	       else
	       cout<<"\n \t\t .Note not updated!!\n";
	      fw1.close();                        //file close
	      nsort();                            //sort function called
	     break;

  case 4  : ifstream n1;
	    ofstream n2;
	    Notes1 not1;
	    char b2;
	    int i=1;
	    n1.open("notes.dat",ios::binary|ios::app); //opening notes.dat
	    n2.open("temp.dat",ios::binary);           //opening temp.dat
	    clrscr();
	    pattern1();
	       while(n1.read((char*)&not1,sizeof(not1)))
		{
		   not1.display();                      //display notes
		   cout<<"\n \t\t .Delete?(Y or N)\t";
		   cin>>b2;
		   clrscr();
		   pattern1();
		   if(b2=='n'||b2=='N')
		   n2.write((char*)&not1,sizeof(not1));   //writing to file
		   if(b2=='y'||b2=='Y')
		   i=0;
		 }
	       remove("notes.dat");
	       rename("temp.dat","notes.dat");
	       clrscr();
	       pattern1();
	       gotoxy(19,6);
	       if(i==0)
	       cout<<"\n \t\t .Note Deleted successfully!\n";
	       else
	       cout<<"\n \t\t .No note deleted!!\n";
	       n2.close();                //file close
	       nsort();                   //sort function is called
	       break;

  case 5  : main();                  //back to main menu

 }

 getch();
}
 }
int rsort();                      //sort function for reminders
int Reminders()                   //function for reminders
 {
  Reminders1 r;
  clrscr();
  fstream ak;
  int ch1;
 while(!0)
 {
  pattern1();
   gotoxy(19,6);
  cout<<"\t 1. VIEW \n";
   gotoxy(19,8);
  cout<<"\t 2. ADD NEW\n";
   gotoxy(19,10);
  cout<<"\t 3. EDIT\n";
   gotoxy(19,12);
  cout<<"\t 4. DELETE\n";
   gotoxy(19,14);
  cout<<"\t 5. BACK\n";
   gotoxy(19,16);
 cin>>ch1;

 switch(ch1)
 {
  case 1  :  ifstream ak1;
	    ak1.open("rem.dat",ios::binary|ios::in);  //opening file
	    int p=0;
	    while(ak1.read((char*)&r,sizeof(r)))
	    {
	    p++;
	    clrscr();pattern1();
	    r.display();             //display reminder
	    getch();
	    }
	    if(p==0)
	    {
	    gotoxy(19,6);
	    cout<<"\n \t\t .No reminders added!!";
	    }
	    getch();
	    ak1.close();                     //file close
	    break;

  case 2  : ak.open("rem.dat",ios::binary|ios::in); //opening file
	    int k=-1;
	    while(ak.read((char*)&r,sizeof(r)))     //loop to check no of reminders
	     {
	       ++k;
	     }
	     ak.close();                              //close file
	     ofstream ak2;
	     ak2.open("rem.dat",ios::binary|ios::out|ios::app);   //opening file to write
	     clrscr();
	     pattern1();
	     r.Add(++k);                                //add function called
	     ak2.write((char*)&r,sizeof(r));            //writing to file
	     ak2.close();                               //file close
	     rsort();                                  //sort function called
	     break;
  case 3  : fstream rem1;
	    ofstream rem2;
	    Reminders1 rot,rota;
	    char bo='p';
	    rem1.open("rem.dat",ios::binary|ios::in|ios::out|ios::app);//opening rem.dat
	    rem2.open("temp.dat",ios::binary);           //opening temp.dat
	    int no,no1;
		while(rem1.read((char*)&rot,sizeof(rot)))
		{
		   clrscr();
		   pattern1();
		   rot.display();                 //display reminders
		   cout<<"\n \t\t .Edit?(Y or N)\t";
		   cin>>bo;
		   clrscr();
		   pattern1();
		   if(bo=='y'||bo=='Y')
		   {
		      no=rot.retno1();
		      rota.Add(no);      //if y call function add
		      rem2.write((char*)&rota,sizeof(rota)); //writing to temp.dat
		      no1=1;
		   }
		   if(bo=='n'||bo=='N')
		   {
		   cout<<'\n';
		   rem2.write((char*)&rot,sizeof(rot)); //writing to temp.dat
		   }
		}
		clrscr();
		pattern1();
		gotoxy(19,6);
		if(bo=='p')
		cout<<"\n \t\t .No Reminders added!!";
	       remove("rem.dat");                 //remove old file
	       rename("temp.dat","rem.dat");      //rename new file
	       if(no1==1)
	       cout<<"\n \t\t .Reminders updated successfully!\n";
	       else
	       cout<<"\n \t\t .Reminders not updated!!\n";
	      rem2.close();                 //file close
	      rsort();                      //sort function called
	     break;

  case 4  : ifstream r1;
	    ofstream r2;
	    Reminders1 rot1;
	    char b3;
	    int i=1;
	    r1.open("rem.dat",ios::binary|ios::app); //opening rem.dat
	    r2.open("temp.dat",ios::binary);         //opening temp.dat
	    clrscr();
	    pattern1();
	       while(r1.read((char*)&rot1,sizeof(rot1)))
		{
		   rot1.display();          //display reminders
		   cout<<"\n \t\t .Delete?(Y or N)\t";cin>>b3;  clrscr(); pattern1();
		   if(b3=='n'||b3=='N')
		   r2.write((char*)&rot1,sizeof(rot1)); //writing to file
		   if(b3=='y'||b3=='Y')
		   i=0;
		 }
	       remove("rem.dat");              //removing old file
	       rename("temp.dat","rem.dat");   //renaming new file
	       clrscr();
	       pattern1();
	       gotoxy(19,6);
	       if(i==0)
	       cout<<"\n \t\t .Reminder Deleted successfully!\n";
	       else
	       cout<<"\n \t\t .No reminders deleted!!\n";
	       r2.close();              //file close
	       rsort();                 //sort function called
	    break;
   case 5  : main();                         //back to main menu

 }
getch();
}
 }

 int Calculator()                 //calculator function
{
   clrscr();
 double x,y;
 char ch,ch4;
 while(!0)
 {
 clrscr();
 gotoxy(25,6);                               //horizontal above
 cout<<1<<"\t"<<2<<"\t"<<3<<endl;
  gotoxy(25,8);
 cout<<4<<"\t"<<5<<"\t"<<6<<endl;            //horizontal below
  gotoxy(25,10);
 cout<<7<<"\t"<<8<<"\t"<<9<<endl;
  gotoxy(25,12);
 cout<<'+'<<"\t"<<0<<"\t"<<'-'<<endl;
  gotoxy(25,14);
 cout<<'*'<<"\t"<<'='<<"\t"<<'/'<<endl;
 char a='.';
 for(int i=18;i<47;i++)
  {
   gotoxy(i,3);
   cout<<a;
  }
 for(i=18;i<47;i++)
 {
   gotoxy(i,19);
   cout<<a;
 }
 for(i=18;i<47;i++)
 {
   gotoxy(i,16);
   cout<<'_';
  }
 for(i=3;i<20;i++)
  {
   gotoxy(18,i);
   cout<<a;
  }
 for(i=4;i<20;i++)
  {
   gotoxy(46,i);
   cout<<a;
  }

  gotoxy(25,4);
  cin>>x>>ch>>y;
  switch(ch)                     // CALCULATION!!!
  {
   case '+' : gotoxy(21,17);
	      cout<<x+y;              //sum
	      break;

   case '-' : gotoxy(21,17);
	      cout<<x-y;              //difference
	      break;

   case '*' : gotoxy(21,17);
	      cout<<x*y;              //product
	      break;


  case '/' : gotoxy(21,17);
	      cout<<x/y;              //quotient
	      break;


   }
   break;
   getch();
   }
   return 0;
}
int Converter();
void length();
void weight();
void temperature();
void currency();

int Converter()
 {
  clrscr();
  int ch1;
  pattern1();
 while(!0)
 {
 gotoxy(19,6);
  cout<<"\t  1. LENGTH\n";
 gotoxy(19,8);
  cout<<"\t  2. WEIGHT\n";
 gotoxy(19,10);
  cout<<"\t  3. CURRENCY\n";
 gotoxy(19,12);
  cout<<"\t  4. TEMPERATURE\n";
 gotoxy(19,14);
  cout<<"\t  5. BACK\n";
 gotoxy(19,18);
 cin>>ch1;
 switch(ch1)
 {
  case 1  : length();        //calling length() function
	    break;

  case 2  : weight();        //calling weight() function
	    break;

  case 3  : currency();      //calling currency() function
	    break;

  case 4  : temperature();   //calling temperature() function
	    break;

  case 5  : main();          //back to main menu
	    break;
  }
 }
}
void length()                  //function for length conversion
 {
   clrscr();
   int l1;
   while(1)
  {
   clrscr();
  pattern1();
  gotoxy(19,6);
   cout<<" 1. Kilometer to Mile\n";
  gotoxy(19,7);
   cout<<" 2. Mile to Kilometer\n";
  gotoxy(19,8);
   cout<<" 3. Meter to Yard\n";
  gotoxy(19,9);
   cout<<" 4. Yard to Meter\n";
  gotoxy(19,10);
   cout<<" 5. Mile to Yard\n";
  gotoxy(19,11);
   cout<<" 6. Yard to Mile\n";
  gotoxy(19,12);
   cout<<" 7. Meter to Inch\n";
  gotoxy(19,13);
   cout<<" 8. Inch to Meter\n";
  gotoxy(19,14);
   cout<<" 9. Back\n";
  gotoxy(19,15);
   cout<<" ENTER CHOICE\n";
  gotoxy(19,16);
  cin>>l1;
  double l;
  switch(l1)
  {
   case 1  :   gotoxy(19,17);
	      cout<<"Kilometer :  ";
	       cin>>l;
	       gotoxy(19,18);
	      cout<<"Mile      :  "<<l*0.6213 ;
	      break;

   case 2  :   gotoxy(19,17);
	      cout<<"Mile      :  ";
	       cin>>l;
	       gotoxy(19,18);
	      cout<<"Kilometer :  "<<l*1.609;
	      break;

   case 3  :   gotoxy(19,17);
	      cout<<"Meter     :  ";
	       cin>>l;
	       gotoxy(19,18);
	      cout<<"Yard      :  "<<l*1.093;
	      break;

  case 4  :    gotoxy(19,17);
	      cout<<"Yard      :  ";
	       cin>>l;
	       gotoxy(19,18);
	      cout<<"Meter     :  "<<l*0.9144;
	      break;

  case 5  :    gotoxy(19,17);
	      cout<<"Mile      :  ";
	       cin>>l;
	       gotoxy(19,18);
	      cout<<"Yard      :  "<<l*1760;
	      break;

  case 6  :    gotoxy(19,17);
	      cout<<"Yard      :  ";
	       cin>>l;
	       gotoxy(19,18);
	      cout<<"Mile      :  "<<l*0.00056;
	      break;

  case 7  :    gotoxy(19,17);
	     cout<<"Meter      :  ";
	       cin>>l;
	       gotoxy(19,18);
	     cout<<"Inch       :  "<<l*39.37;
	     break;

  case 8  :   gotoxy(19,17);
	     cout<<"Inch       :  ";
	      cin>>l;
	      gotoxy(19,18);
	     cout<<"Meter      :  "<<l*0.0254;
	     break;

  case 9  : Converter();
   }
getch();
 }
}

void weight()            //function for weight conversion
{
  clrscr();
  int w1;
  while(1)
  {
  clrscr();
  pattern1();
  gotoxy(19,6);
   cout<<" 1. Kilogram to Pound\n";
 gotoxy(19,7);
   cout<<" 2. Pound to Kilogram\n";
 gotoxy(19,8);
   cout<<" 3. Kilogram to Ounce\n";
 gotoxy(19,9);
   cout<<" 4. Ounce to Kilogram\n";
 gotoxy(19,10);
   cout<<" 5. Pound to Ounce\n";
 gotoxy(19,11);
   cout<<" 6. Ounce to Pound\n";
 gotoxy(19,12);
   cout<<"  7. BACK\n";
 gotoxy(19,13);
  cin>>w1;
  double w;
  switch(w1)
  {
   case 1  :   gotoxy(19,14);
	     cout<<"Kilogram   :  ";
	      cin>>w;
	       gotoxy(19,15);
	     cout<<"Pound      :  "<<w*2.205 ;
	      break;

   case 2  :   gotoxy(19,14);
	     cout<<"Pound      :  ";
	      cin>>w;
	       gotoxy(19,15);
	     cout<<"Kilogram   :  "<<w*0.454;
	      break;

   case 3  :   gotoxy(19,14);
	     cout<<"Kilogram   :  ";
	      cin>>w;
	       gotoxy(19,15);
	     cout<<"Ounce      :  "<<w*35.274;
	      break;

  case 4  :   gotoxy(19,14);
	     cout<<"Ounce      :  ";
	      cin>>w;
	       gotoxy(19,15);
	     cout<<"Kilogram   :  "<<w*0.0283;
	     break;

  case 5  :   gotoxy(19,14);
	     cout<<"Pound      :  ";
	      cin>>w;
	       gotoxy(19,15);
	     cout<<"Ounce      :  "<<w*16;
	     break;

  case 6  :   gotoxy(19,14);
	     cout<<"Ounce      :  ";
	      cin>>w;
	       gotoxy(19,15);
	     cout<<"Pound      :  "<<w*0.0625;
	     break;

  case 7  : Converter();
  }
 getch();
 }
}
void currency()          //function for currency conversion
{
 clrscr();
 int c1,c2;
 do
 {
  clrscr();
    pattern1();
  gotoxy(19,6);
 cout<<"\t  CONVERT\n";
  gotoxy(19,7);
 cout<<"\t  1. Rupee \n";
  gotoxy(19,8);
 cout<<"\t  2. Dollar \n";
  gotoxy(19,9);
 cout<<"\t  3. Euro \n";
  gotoxy(19,10);
 cout<<"\t  4. Yuan \n";
  gotoxy(19,11);
 cout<<"\t  5. Ruble\n";
  gotoxy(19,12);
 cout<<"\t  6. BACK\n";
  gotoxy(19,13);
 cout<<"\t  ENTER CHOICE  ";
 cin>>c1;
  gotoxy(19,15);
 double c;
 switch(c1)
 {
  case 1  :  clrscr();
	       pattern1();
		gotoxy(19,6);
	     cout<<"  1. Ruble \n";
		gotoxy(19,8);
	     cout<<"  2. Dollar \n";
		gotoxy(19,10);
	     cout<<"  3. Euro \n";
		gotoxy(19,12);
	     cout<<"  4. Yuan \n";
		gotoxy(19,14);
	     cout<<"  ENTER CHOICE   ";
	     cin>>c2;

	     switch(c2)
	     {
	      case 1 : gotoxy(19,17);
		       cout<<"Rupee      :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Ruble      :  "<<c*0.96;

		       break;

	      case 2 : gotoxy(19,17);
		       cout<<"Rupee      :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Dollar     :  "<<c*0.014;
		       break;

	      case 3 : gotoxy(19,17);
		       cout<<"Rupee      :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Euro       :  "<<c*0.012;
		       break;

	      case 4 : gotoxy(19,17);
		       cout<<"Rupee      :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Yuan       :  "<<c*0.097;
		       break;
	      }
	      break;

  case 2  :  clrscr();
	     pattern1();
	      gotoxy(19,6);
	     cout<<"  1. Ruble \n";
	      gotoxy(19,8);
	     cout<<"  2. Rupee\n";
	      gotoxy(19,10);
	     cout<<"  3. Euro \n";
	      gotoxy(19,12);
	     cout<<"  4. Yuan \n";
	      gotoxy(19,14);
	     cout<<"  ENTER CHOICE  ";
	     cin>>c2;
	     switch(c2)
	     {
	      case 1 : gotoxy(19,17);
		       cout<<"Dollar     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Ruble      :  "<<c*67.23;
		       break;

	      case 2 : gotoxy(19,17);
		       cout<<"Dollar     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Rupee      :  "<<c*69.84;
		       break;

	      case 3 : gotoxy(19,17);
		       cout<<"Dollar     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Euro       :  "<<c*0.86;
		       break;

	      case 4 : gotoxy(19,17);
		       cout<<"Dollar     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Yuan       :  "<<c*6.81;
		       break;
	      }
	      break;

  case 3  :  clrscr();
	     pattern1();
	      gotoxy(19,6);
	     cout<<"  1. Ruble \n";
	      gotoxy(19,8);
	     cout<<"  2. Rupee\n";
	      gotoxy(19,10);
	     cout<<"  3. Dollar \n";
	      gotoxy(19,12);
	     cout<<"  4. Yuan \n";
	      gotoxy(19,14);
	     cout<<"  ENTER CHOICE   ";
	     cin>>c2;
	     switch(c2)
	     {
	      case 1 : gotoxy(19,17);
		       cout<<"Euro       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Ruble      :  "<<c*78.14;
		       break;

	      case 2 : gotoxy(19,17);
		       cout<<"Euro       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Rupee      :  "<<c*81.20;
		       break;

	      case 3 : gotoxy(19,17);
		       cout<<"Euro       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Dollar     :  "<<c*1.16;
		       break;

	      case 4 : gotoxy(19,17);
		       cout<<"Euro       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Yuan       :  "<<c*7.92;
		       break;
	      }
	      break;

  case 4  :  clrscr();
	     pattern1();
	      gotoxy(19,6);
	     cout<<"  1. Ruble \n";
	      gotoxy(19,8);
	     cout<<"  2. Rupee\n";
	       gotoxy(19,10);
	     cout<<"  3. Euro \n";
	       gotoxy(19,12);
	     cout<<"  4. Dollar \n";
	       gotoxy(19,14);
	     cout<<"  ENTER CHOICE   ";
	     cin>>c2;
	     switch(c2)
	     {
	      case 1 : gotoxy(19,17);
		       cout<<"Yuan       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Ruble      :  "<<c*9.88;
		       break;

	      case 2 : gotoxy(19,17);
		       cout<<"Yuan       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Rupee      :  "<<c*10.26;
		       break;

	      case 3 : gotoxy(19,17);
		       cout<<"Yuan       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Euro       :  "<<c*0.13;
		       break;

	      case 4 : gotoxy(19,17);
		       cout<<"Yuan       :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Dollar     :  "<<c*0.15;
		       break;
	      }
	      break;

  case 5  :  clrscr();
	     pattern1();
	      gotoxy(19,6);
	     cout<<"  1. Yuan \n";
	      gotoxy(19,8);
	     cout<<"  2. Rupee\n";
	      gotoxy(19,10);
	     cout<<"  3. Euro \n";
	      gotoxy(19,12);
	     cout<<"  4. Dollar \n";
	      gotoxy(19,14);
	     cout<<"  ENTER CHOICE\n";
	      gotoxy(19,16);
	     cin>>c2;
	     switch(c2)
	     {
	      case 1 : gotoxy(19,17);
		       cout<<"Rubble     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Yuan       :  "<<c*0.1;
		       break;

	      case 2 : gotoxy(19,17);
		       cout<<"Rubble     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Rupee      :  "<<c*1.04;
		       break;

	      case 3 : gotoxy(19,17);
		       cout<<"Rubble     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Euro       :  "<<c*0.013;
		       break;

	      case 4 : gotoxy(19,17);
		       cout<<"Rubble     :  ";
		       cin>>c;
		       gotoxy(19,18);
		       cout<<"Dollar     :  "<<c*0.015;
		       break;
	      }
	      break;

    case 6  : Converter();
  }
  getch();
 }while(1);
}
void temperature()          //function for temperature conversion
 {
   clrscr();
   int t1;
   while(1)
   {
   clrscr();
   pattern1();
    gotoxy(19,6);
   cout<<" 1. Celsius to Fahrenheit\n";
    gotoxy(19,7);
   cout<<" 2. Fahrenheit to Celsius\n";
    gotoxy(19,8);
   cout<<" 3. Kelvin to Celsius\n";
    gotoxy(19,9);
   cout<<" 4. Celsius to Kelvin\n";
    gotoxy(19,10);
   cout<<" 5. Kelvin to Fahrenheit\n";
    gotoxy(19,11);
   cout<<" 6. Fahrenheit to Kelvin\n";
    gotoxy(19,12);
   cout<<" 7. BACK\n";
    gotoxy(19,13);
 cout<<" ENTER CHOICE   ";
 cin>>t1;
 double t;
 switch(t1)
 {
  case 1  : gotoxy(19,15);
	    cout<<"Celsius    :  ";
	    cin>>t;
	    gotoxy(19,16);
	    cout<<"Fahrenheit :"<<(t*9)/5 + 32;
	    break;

  case 2  : gotoxy(19,15);
	    cout<<"Fahrenheit :  ";
	    cin>>t;
	    gotoxy(19,16);
	    cout<<"Celsius    :  "<<(t-32)*5/9;
	    break;

  case 3  : gotoxy(19,15);
	    cout<<"Kelvin     :  ";
	    cin>>t;
	    gotoxy(19,16);
	    cout<<"Celsius    :  "<<t-273;
	    break;

  case 4  : gotoxy(19,15);
	    cout<<"Celsius    :  ";
	    cin>>t;
	    gotoxy(19,16);
	    cout<<"Kelvin     :  "<<t+273;
	    break;

  case 5  : gotoxy(19,15);
	    cout<<"Kelvin     :  ";
	    cin>>t;
	    gotoxy(19,16);
	    cout<<"Fahrenheit :  "<<(t-273)*9/5 + 32;
	    break;

  case 6  : gotoxy(19,15);
	    cout<<"Fahrenheit :  ";
	    cin>>t;
	    gotoxy(19,16);
	    cout<<"Kelvin     :  "<<(t-32)*5/9 + 273;
	    break;

  case 7  : Converter();
   }
 getch();
 }
}

void main()                     //main function
{
 int ch1;
 while(!0)
 { clrscr();
   pattern1();                         //border function called
  gotoxy(19,6);
 cout<<"\t  MAIN MENU\n";
  gotoxy(19,7);
 cout<<"\t  .........\n";
  gotoxy(19,8);
 cout<<"\t  1. CONTACTS\n";
  gotoxy(19,9);
 cout<<"\t  2. NOTES\n";
  gotoxy(19,10);
 cout<<"\t  3. REMINDERS\n";
  gotoxy(19,11);
 cout<<"\t  4. CALCULATOR\n";
  gotoxy(19,12);
 cout<<"\t  5. CONVERTER\n";
  gotoxy(19,13);
 cout<<"\t  6. EXIT\n";
  gotoxy(19,15);
 cout<<" \t  SELECT\t";
  gotoxy(19,16);
 cin>>ch1;

 switch(ch1)
 {
  case 1  : Contacts();          //calling contacts function
	    break;

  case 2  : Notes();             //calling notes function
	    break;

  case 3  : Reminders();         //calling reminders function
	    break;

  case 4  : Calculator();        //calling calculators function
	    break;

  case 5  : Converter();         //calling converter function
	    break;

  case 6  : char ch2;
	    gotoxy(19,17);
	    cout<<"Are you sure?(Y/N)\t";
	    cin>>ch2;
	    if(ch2=='Y'||ch2=='y')
	    exit(0);
	    }
 getch();
 }
}
/*                       OUTPUT
			 ******
		 .............................
		 .                           .
		 .                           .
		 .        MAIN MENU          .
		 .        .........          .
		 .        1. CONTACTS        .
		 .        2. NOTES           .
		 .        3. REMINDERS       .
		 .        4. CALCULATOR      .
		 .        5. CONVERTER       .
		 .        6. EXIT            .
		 .                           .
		 .        SELECT             .
		 .1                          .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .       1. SEARCH           .
		 .                           .
		 .       2. ADD NEW          .
		 .                           .
		 .       3. EDIT             .
		 .                           .
		 .       4. DELETE           .
		 .                           .
		 .       5. BACK             .
		 .                           .
		 .1                          .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .        MAIN MENU          .
		 .        .........          .
		 .        1. CONTACTS        .
		 .        2. NOTES           .
		 .        3. REMINDERS       .
		 .        4. CALCULATOR      .
		 .        5. CONVERTER       .
		 .        6. EXIT            .
		 .                           .
		 .        SELECT             .
		 .2                          .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .       1. VIEW ALL         .
		 .                           .
		 .       2. ADD NEW          .
		 .                           .
		 .       3. EDIT             .
		 .                           .
		 .       4. DELETE           .
		 .                           .
		 .       5. BACK             .
		 .                           .
		 .1                          .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .        MAIN MENU          .
		 .        .........          .
		 .        1. CONTACTS        .
		 .        2. NOTES           .
		 .        3. REMINDERS       .
		 .        4. CALCULATOR      .
		 .        5. CONVERTER       .
		 .        6. EXIT            .
		 .                           .
		 .        SELECT             .
		 .3                          .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .       1. VIEW             .
		 .                           .
		 .       2. ADD NEW          .
		 .                           .
		 .       3. EDIT             .
		 .                           .
		 .       4. DELETE           .
		 .                           .
		 .       5. BACK             .
		 .                           .
		 .1                          .
		 ............................
		 .............................
		 .                           .
		 .                           .
		 .        MAIN MENU          .
		 .        .........          .
		 .        1. CONTACTS        .
		 .        2. NOTES           .
		 .        3. REMINDERS       .
		 .        4. CALCULATOR      .
		 .        5. CONVERTER       .
		 .        6. EXIT            .
		 .                           .
		 .        SELECT             .
		 .4                          .
		 .............................
		 .............................
		 .      7*7                  .
		 .                           .
		 .      1       2       3    .
		 .                           .
		 .      4       5       6    .
		 .                           .
		 .      7       8       9    .
		 .                           .
		 .      +       0       -    .
		 .                           .
		 .      *       =       /    .
		 .                           .
		 .___________________________.
		 .    49                     .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .        MAIN MENU          .
		 .        .........          .
		 .        1. CONTACTS        .
		 .        2. NOTES           .
		 .        3. REMINDERS       .
		 .        4. CALCULATOR      .
		 .        5. CONVERTER       .
		 .        6. EXIT            .
		 .                           .
		 .        SELECT             .
		 .5                          .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .        CONVERT            .
		 .        1. Rupee           .
		 .        2. Dollar          .
		 .        3. Euro            .
		 .        4. Yuan            .
		 .        5. Ruble           .
		 .        6. BACK            .
		 .        ENTER CHOICE  1    .
		 .                           .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .  1. Ruble                 .
		 .                           .
		 .  2. Dollar                .
		 .                           .
		 .  3. Euro                  .
		 .                           .
		 .  4. Yuan                  .
		 .                           .
		 .  ENTER CHOICE   1         .
		 .                           .
		 .............................
		 .............................
		 .                           .
		 .                           .
		 .  1. Ruble                 .
		 .                           .
		 .  2. Dollar                .
		 .                           .
		 .  3. Euro                  .
		 .                           .
		 .  4. Yuan                  .
		 .                           .
		 .  ENTER CHOICE   1         .
		 .                           .
		 .                           .
		 .Rupee      :  10           .
		 .Ruble      :  9.6          .
		 .                           .
		 .............................

*/