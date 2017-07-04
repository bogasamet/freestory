# freestory
#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
  typedef struct node{
  	char data ;
   node *next;
  }ptr;
    node *p=NULL;
    node *q=NULL;
    node *son=NULL; 
	node *son1=NULL;
	
    node *ekle(char *data1,char *data2,node *ilk,node *ilk1){
   if(*data1==NULL && *data2==NULL){
   	return ilk;
   } 
   else if(*data1!=NULL && *data2==NULL){ 
   node *temp; 
       temp=new ptr();
       temp->data=*data1;
       son->next=temp;
       temp->next=NULL;
       son=temp;
       ekle(data1+1,data2,ilk,ilk1);
   	
   }
   else if(*data1==NULL && *data2!=NULL){
   	node *temp; 
   	 temp=new ptr();
       temp->data=*data2;
       son1->next=temp;
       temp->next=NULL;
       son1=temp;
       ekle(data1,data2+1,ilk,ilk1);
   }
   else{

   	 if(ilk==NULL){
   		ilk=new ptr();
   		ilk->data=*data1;
   		ilk->next=NULL;
   		son=ilk;
   		p=ilk;
	   }
	   else{
	   	node *temp; 
	   	temp=new ptr();
	   	temp->data=*data1;
	   	temp->next=NULL;
	   	son->next=temp;
	   	son=temp;
	   }
	   
	if(ilk1==NULL){
		
   		ilk1=new ptr();
   		ilk1->data=*data2;
   		ilk1->next=NULL;
   		son1=ilk1;
   		q=ilk1;
	   }
	   else{
	   	node *temp; 
	   	temp=new ptr();
	   	temp->data=*data2;
	   	temp->next=NULL;
	   	son1->next=temp;
	   	son1=temp;
	   }
	ekle(data1+1,data2+1,ilk,ilk1);
   }
   	
   }
  
   int main(){
   	char dizi[20],dizi1[20];
   	char *a,*b;
   	printf("gir");scanf("%s",&dizi);
   	printf("gir");scanf("%s",&dizi1);
   	a=&dizi[0];
   	b=&dizi1[0];
     ekle(a,b,p,q);
  
   }
