#import "C:\Program Files\Common Files\System\ADO\msado15.dll" \
no namespace rename("EOF", "EndOfFile")
#include<iostream.h>
#include<stdio.h>
#include<conio.h>
void states();
void terr();
void reli();
void lang();
int ch,ch1;
void main()
{
CoInitialize(NULL);
char e='y';
int i;
while(e=='y')
{
cout<<"\n\n\n\n\n\n\n\n\n\n   ------------------------------------------------------------------------\n\n";
cout<<"\t\t\t\ Indian DEMOGRAPHY\n\n";
cout<<"   -------------------------------------------------------------------------\n\n";
cout<<"\n\n\n\n";
cout<<"\t\t\t1. STATES OF INDIA";
cout<<"\n\n\t\t\t2. UNION TERRITORIES OF INDIA";
cout<<"\n\n\t\t\t3. RELIGIONS OF INDIA";
cout<<"\n\n\t\t\t4. LANGUAGES OF INDIA";
cout<<"\n\n\t\t\t5. EXIT";
cout<<"\n\n\n\t\t\t ENTER YOUR CHOICE :";
cin>>ch;
switch(ch)
{
case 1:
states();
break;
case 2:
terr();
break;
case 3:
reli();
break;
case 4:
lang();
break;
case 5:
goto e;
break;
}
try
{
_RecordsetPtr pRst("ADODB.Recordset");
_bstr_t strCnn("DRIVER={Microsoft Access     Driver(*.mdb)};UID=admin;DBQ=pro1.mdb");
switch(ch)
{
case 1:
{
if(ch==29)
goto e;
else {
pRst->Open("SELECT * FROM states1 ;", strCnn, adOpenStatic, adLockReadOnly, adCmdText);
for(i=1;i<=28,!pRst->EndOfFile;i++)
{
if(i==ch1)
{
cout<<"\n\n\n\n\t\tName of the state    :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("statenames")->GetValue()<<"\t";
cout<<"\n\n\t\tTotal population     :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("tpop")->GetValue()<<"\t";
cout<<"\n\n\t\tMale population      :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("mpop")->GetValue()<<"\t";
cout<<"\n\n\t\tFemale population    :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("fpop")->GetValue()<<"\t";
cout<<"\n\n\t\tGender ratio         :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("sratio")->GetValue()<<"\t";
cout<<"\n\n\t\tTotal literacy rate  :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("tlit")->GetValue()<<"\t";
cout<<"\n\n\t\tMale literacy rate   :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("mlit")->GetValue()<<"\t";
cout<<"\n\n\t\tFemale literacy rate :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("flit")->GetValue();
}
else
{
pRst->MoveNext();
}
}
pRst->MoveFirst();
pRst->Close();
}
}
break;
case 2:
{
if(ch==8)
 goto e;
else {
pRst->Open("SELECT * FROM terr1 ;", strCnn, adOpenStatic, adLockReadOnly, adCmdText);
for(i=1;i<=7,!pRst->EndOfFile;i++)
{
if(i==ch1)
{
cout<<"\n\n\n\n\t\tName of the state    :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("terrname")->GetValue()<<"\t";
cout<<"\n\n\t\tTotal population     :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("tpop")->GetValue()<<"\t";
cout<<"\n\n\t\tMale population      :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("mpop")->GetValue()<<"\t";
cout<<"\n\n\t\tFemale population    :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("fpop")->GetValue()<<"\t";
cout<<"\n\n\t\tGender ratio         :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("sratio")->GetValue()<<"\t";
cout<<"\n\n\t\tTotal literacy rate  :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("tlit")->GetValue()<<"\t";
cout<<"\n\n\t\tMale literacy rate   :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("mlit")->GetValue()<<"\t";
cout<<"\n\n\t\tFemale literacy rate :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("flit")->GetValue();
}
else
{
pRst->MoveNext();
}                 
}
pRst->MoveFirst();
pRst->Close();
}
}
break;
case 3:
{
if(ch==8)
goto e;
else {
 pRst->Open("SELECT * FROM reli1 ;", strCnn, adOpenStatic, adLockReadOnly, adCmdText);
for(i=1;i<=7,!pRst->EndOfFile;i++)
{
if(i==ch1)
{
cout<<"\n\n\n\n\t\tName of the religion :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("rname")->GetValue();
cout<<"\n\n\t\tTotal population     :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("tpop")->GetValue();
cout<<"\n\n\t\tGender ratio         :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("sratio")->GetValue();
cout<<"\n\n\t\tChild gender ratio   :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("csratio")->GetValue();
cout<<"\n\n\t\tTotal literacy rate  :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("tlit")->GetValue();
}
else
{
pRst->MoveNext();
} 
}
pRst->MoveFirst();
pRst->Close();
}
}
break;
case 4:
{
if(ch==38)
goto e;
else {
pRst->Open("SELECT * FROM lang1 ;", strCnn, adOpenStatic, adLockReadOnly, adCmdText);
for(i=1;i<=37,!pRst->EndOfFile;i++)
{
if(i==ch1)
{
cout<<"\n\n\n\n\t\tName of the language         :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("lname")->GetValue();
cout<<"\n\n\t\tpopulation in India         :";
cout<<(_bstr_t) pRst->GetFields()->GetItem("ipop")->GetValue();
cout<<"\n\n\t\tpopulation other countries:";
cout<<(_bstr_t) pRst->GetFields()->GetItem("opop")->GetValue();
}
else
{
pRst->MoveNext();
}  
}
pRst->MoveFirst();
pRst->Close();
}
}
}
}
catch (_com_error &e)
{
cout<<(char*) e.Description();
}
e:
cout<<"\n\n\n";
cout<<"\t\t do you want to continue(y/n):";
cin>>e;
}
}
void states()
{
 cout<<"\n\n\n\n\n\n\n\t---------------------------------------------------------\n";
 cout<<"\n\t|\t\t\t STATES OF INDIA\t\t\t|\n";
 cout<<"\t---------------------------------------------------------\n\n";
 cout<<"\n\n\t|\t1.  andhra pradesh	15. maharastra\t\t|";
 cout<<"\n\n\t|\t2.  arunachal pradesh	16. megalaya\t\t|";
 cout<<"\n\n\t|\t3.  Assam		 17. mizoram\t\t|";
 cout<<"\n\n\t|\t4.  Bihar		 18. nagaland\t\t|";
 cout<<"\n\n\t|\t5.  goa  		 19. orrisa\t\t|";
 cout<<"\n\n\t|\t6.  gujarat		 20. punjab\t\t|";
 cout<<"\n\n\t|\t7.  haryana		 21. Rajasthan\t\t|";
 cout<<"\n\n\t|\t8.  himachal pradesh	 22. sikkim\t\t|";
 cout<<"\n\n\t|\t9.  jammu & Kashmir 23. tamil nadu\t\t|";
 cout<<"\n\n\t|\t10. jarkhand		24. tripura\t\t|";
 cout<<"\n\n\t|\t11. karnataka		25. Uttar pradesh\t|";
 cout<<"\n\n\t|\t12. kerala		26. uttranchal\t\t|";
 cout<<"\n\n\t|\t13. Madhya pradesh	27. west bengal\t\t|";
 cout<<"\n\n\t|\t14. Manipur 		28. chatisgar\t\t|";
 cout<<"\n\n\t|\t\t\t\t29. EXIT\t\t|";
 cout<<"\n\n\t---------------------------------------------------------\n\n";
 cout<<"\n\n\t\t  enter your choice: ";
 cin>>ch1;
 }
void terr()
{
cout<<"\n\n\n\n\n\n\n\n\n";
cout<<"\t\t---------------------------------\n";
cout<<"\n\t\t|\t UNION TERRITORIES\t|\n\n";
cout<<"\t\t---------------------------------\n";
cout<<"\n\n\t\t|\t1. Andaman & nicrobar\t|";
cout<<"\n\n\t\t|\t2. chandigarh\t\t|";
cout<<"\n\n\t\t|\t3. dadra & nagarhaveli  |";
cout<<"\n\n\t\t|\t4. daman & diu\t\t|";
cout<<"\n\n\t\t|\t5. Delhi\t\t|";
cout<<"\n\n\t\t|\t6. lakshadweep\t\t|";
cout<<"\n\n\t\t|\t7. pondicherry\t\t|";
cout<<"\n\n\t\t|\t8. EXIT      \t\t|";
cout<<"\n\n\t\t---------------------------------\n";
cout<<"\n\n\t\t\t  enter your choice:  ";
cin>>ch1;
}
void reli()
{
  cout<<"\n\n\n\n\n\n\n\n\n\n\n\n";
 cout<<"\t\t-----------------------------------------\n";
 cout<<"\n\t\t|\t  RELIGIONS IN INDIA    \t|\n";
 cout<<"\n\t\t-----------------------------------------\n\n";
 cout<<"\t\t|\t\t1. Hindus\t\t|\n\n";
 cout<<"\t\t|\t\t2. Muslims\t\t|\n\n";
 cout<<"\t\t|\t\t3. Christians\t\t|\n\n";
 cout<<"\t\t|\t\t4. Sikhs\t\t|\n\n";
 cout<<"\t\t|\t\t5. Buddhists\t\t|\n\n";
 cout<<"\t\t|\t\t6. Jains\t\t|\n\n";
 cout<<"\t\t|\t\t7. Others\t\t|\n\n";
 cout<<"\t\t|\t\t8. EXIT \t\t|\n\n";
 cout<<"\n\t\t-----------------------------------------\n\n";
 cout<<"\t\t\t Enter your choice: ";
 cin>>ch1;
}
void lang()
{
cout<<"\n\n\n\n";
cout<<"\t-----------------------------------------------------------------\n";
cout<<"\n\t|\t\t   LANGUAGES IN INDIA \t\t\t\t|\n";
cout<<"\n\t----------------------------------------------------------------\n\n";
cout<<"\t|\t\t01. Assamese		20. Goanese\t\t|\n\n";
cout<<"\t|\t\t02. Awadi    		21. Kurux\t\t|\n\n";
cout<<"\t|\t\t03. Bagri	                        22. Maithili\t\t|\n\n";
cout<<"\t|\t\t04. Bengali	 	23. Malayalam\t\t|\n\n";
cout<<"\t|\t\t05. Bhili 	                        24. Marathi\t\t|\n\n";
cout<<"\t|\t\t06. Bhojpuri 	            25. Marwari\t\t|\n\n";
cout<<"\t|\t\t07. Chatisgar                  26. Meithei\t\t|\n\n";
cout<<"\t|\t\t08. Deccan		27. Mundari\t\t|\n\n";
cout<<"\t|\t\t09. Dogri-Kangri            28. Nepali\t\t|\n\n";
cout<<"\t|\t\t10. Garhwali 		29. Oriya\t\t|\n\n";
cout<<"\t|\t\t11. Gujarati		30. Punjabi\t\t|\n\n";
cout<<"\t|\t\t12. Haryana		31. Sadri\t\t|\n\n";
cout<<"\t|\t\t13. Hindi 		32. Santhali\t\t|\n\n";
cout<<"\t|\t\t14. Ho			33. Sindhi\t\t|\n\n";
cout<<"\t|\t\t15. Kanauji		34. Tamil\t\t|\n\n";
cout<<"\t|\t\t16. Kannada		35. Telugu\t\t|\n\n";
cout<<"\t|\t\t17. Kashmiri		36. Tulu\t\t|\n\n";
cout<<"\t|\t\t18. Khandesi		37. Urdu\t\t|\n\n";
cout<<"\t|\t\t19. Konkani               38. EXIT\t\t|\n\n";
cout<<"\t-----------------------------------------------------------------\n";
cout<<"\n\t\t enter your choice: ";
cin>>ch1;
}
