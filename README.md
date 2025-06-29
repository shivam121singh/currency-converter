#include<iostream>
using namespace std ;
float converter(){
    char currency1;
    char currency2;//in which currency we have to change 
    
    float value1;
    float currencyvalue2=0;
    char startagain;
    
    cout<<"currency 1 for input\n currency 2 for output"<<endl;
    againenter:
cout<<"ENTER THE currency1 NAME  :";
cin>>currency1;
if(currency1=='d'||currency1=='r'||currency1=='p'||currency1=='e'){
cout<<"enter the value1 : ";
cin>>value1;
switch(currency1){
    case'd':
        beg:
    cout<<"enter the currency2 name:";
    cin>>currency2;
    if(currency2=='d'||currency2=='D'){
        currencyvalue2=value1*1;
    }
    else if(currency2=='e'){
        currencyvalue2=value1*0.85;
    }
    else if(currency2=='r'||currency2=='R'){
        currencyvalue2=value1*85.52;
    }
    else if (currency2=='p'||currency2=='P'){
        currencyvalue2=value1*0.72;
    }
    else {
        cout<<"wrong input ";
        goto beg;}break;
    
    

case'r':
        tt:
    cout<<"enter the currency2 name:";
    cin>>currency2;
    if(currency2=='r'||currency2=='r'){
        currencyvalue2=value1*1;
    }
    else if(currency2=='d'||currency2=='D'){
        currencyvalue2=value1*0.011;
    }
    else if(currency2=='e'||currency2=='E'){
        currencyvalue2=value1*0.0099;
    }
    else if (currency2=='p'||currency2=='P'){
        currencyvalue2=value1*0.0085;
    }
    else {
        cout<<"wrong input ";
        goto tt;
    }break;
    case'e':
        cc:
    cout<<"enter the currency2 name:";
    cin>>currency2;
    if(currency2=='d'||currency2=='D'){
        currencyvalue2=value1*1.17;
    }
    else if(currency2=='e'||currency2=='E'){
        currencyvalue2=value1*1;
    }
    else if(currency2=='r'||currency2=='R'){
        currencyvalue2=value1*100.22;
    }
    else if (currency2=='p'||currency2=='P'){
        currencyvalue2=value1*0.85;
    }
    else {
        cout<<"wrong input ";
    goto cc;
    }break;
     case'p':
        ff:
    cout<<"enter the currency2 name:";
    cin>>currency2;
    if(currency2=='d'||currency2=='D'){
        currencyvalue2=value1*1.37;
    }
    else if(currency2=='e'||currency2=='E'){
        currencyvalue2=value1*1.17;
    }
    else if(currency2=='r'||currency2=='R'){
        currencyvalue2=value1*117.36;
    }
    else if (currency2=='p'||currency2=='P'){
        currencyvalue2=value1*1;
    }
    else {
        cout<<"wrong input ";
    goto ff;
    }
    
    break;

} 
    return currencyvalue2;
    
}

else {
    cout<<"you choosed wrong currency name enter again ";
    goto againenter;
}
}
int main(){
    begin:
    char s ;
    char start;
    cout<<"*******WELCOME TO THE CURRENCY CONVERTER APP**********"<<endl;
    cout<<"       please follow the instruction as needed"<<endl;
    cout<<"you can have only these currency like dollar ruppees euro  pound "<<endl;
    cout<<"type (D or d) for the dollar "<<endl;
    cout<<"type (E or e) for euroes"<<endl;
    cout<<"type (p Or p) for pound "<<endl;
    cout<<"type (R or r)  for ruppees"<<endl;
    start:
    cout<<"ENTER S OR s FOR START "<<endl;
    cin>>start;
    if(start=='s'||start=='S'){
    float finalvalue=converter();
    cout<<"THE FINAL RESULT IS : "<<finalvalue;
    
    cout<<endl<<"do you you to start it again then press 'y' for stoping press 'n' ";
    pressagain:
    cin>>s;
    if(s=='y'||s=='Y'){
        goto begin;
    }
    else if (s=='n'||s=='N'){
        cout<<"THANKS FOR VISITING SHIVAM'S APP";}
    else {
        cout<<"wrong press press again :";
        goto pressagain;
    }
        
    }
    else {
        cout<<"you did not press s for  start please press s for start ";
        goto start ;
    }
    
    
}
