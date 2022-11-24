#include <iostream>
#include <stdlib.h>
#include<conio.h>
using namespace std;
int count = 0;

struct Student{
	string name, id,gioitinh;

	float Diemtoan,Diemly,Diemhoa,DTB;
	int NamSinh,NgaySinh,ThangSinh,Ngaymax;

};
 
struct SV{
	Student s;
	SV *next;
};
 
typedef struct SV* sv;
sv makeNode(){
	Student s;
	
	cout << "Nhap thong tin sinh vien :\n";
	cout << "Nhap ID :"; 
	fflush(stdin);
	getline(cin,s.id);
    cout << "Nhap ten :";
    fflush(stdin);
    getline(cin, s.name);
    
    do
    {
    cout<<"Nhap ngay sinh: ";
    cin>>s.NgaySinh;	
	}
		while(s.NgaySinh<=0 || s.NgaySinh>31 && cout<<"\nNhap lai ngay sinh\n"); 
		
	do
	{
	 cout <<"Nhap thang sinh: ";
    cin>>s.ThangSinh;	
	}while(s.ThangSinh<=0 || s.ThangSinh>12 &&cout<<"\nNhap lai thang sinh\n");
   switch(s.ThangSinh){
		case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
            s.Ngaymax=31; 
        break;               
		case 2:
            if ((s.NamSinh%4==0 && s.NamSinh%100!=0) || (s.NamSinh%400==0)){
				
            if(s.NgaySinh>29){
            cout<<"Nhap lai ngay sinh: ";
			cin>>s.NgaySinh; 
	}
                    
  }
        else {
				
            if(s.NgaySinh>28){
		    cout<<"Nhap lai ngay sinh: ";
			cin>>s.NgaySinh;
	}       
  }
	    break;
        case 4:
        case 6:
        case 9:
        case 11:
            if(s.NgaySinh>30){
        cout<<"Nhap lai ngay sinh: ";
		cin>>s.NgaySinh;
};
        break;
    }
      
 
	do {
		cout<<"Nhap nam sinh: ";
	cin>>s.NamSinh;
}
    while(s.NamSinh<=1990 || s.NamSinh>2023 && cout<<"\nNhap lai nam sinh\n");
 
		do  {
			cout<<"Nhap gioi tinh y(nam) or n(nu) : ";
		cin>>s.gioitinh;
		}
	      while (s.gioitinh!="y" && s.gioitinh!= "n" && cout<<"\nNhap lai gioi tinh: \n");
 
 
        cout<<"Nhap diem toan: ";
        cin>>s.Diemtoan;
            while(s.Diemtoan<0 || s.Diemtoan >10){
         	cout<<"nhap sai roi nhap lai di: ";
         	cin>>s.Diemtoan;
        getch(); 
	}
        cout<<"Nhap diem ly: ";
        cin>>s.Diemly;
        while(s.Diemly <0 || s.Diemly >10){
         	cout<<"nhap sai roi nhap lai di: ";
         	cin>>s.Diemly;
          getch(); 
	}
        cout<<"Nhap diem hoa: ";
        cin>>s.Diemhoa;
        while(s.Diemhoa <0 || s.Diemhoa >10){
         	cout<<"nhap sai roi nhap lai di: ";
         	cin>>s.Diemhoa;
          getch();
    } 
        s.DTB = (s.Diemtoan+s.Diemly+s.Diemhoa)*1.0 / 3;
        	
    
	sv tmp = new SV();
	tmp->s = s;
	tmp->next = NULL;
	return tmp;
}
 

 bool empty(sv a){
	return a == NULL;
}
 
 int Size(sv a){
    int cnt = 0;
	while(a != NULL){
		++cnt;
		a = a->next; 
	
	}
	return cnt;
}
 

 void insertFirst(sv &a){
	sv tmp = makeNode();
	if(a == NULL){
		a = tmp;
	}
	else{
		tmp->next = a;
		a = tmp;
	}
}
 

void insertLast(sv &a){
	sv tmp = makeNode();
	if(a == NULL){
		a = tmp;
	}
	else{
		sv p = a;
		while(p->next != NULL){
			p = p->next;
		}
		p->next = tmp;
	}
}
 

 void insertMiddle(sv &a,int pos){
	int n = Size(a);
	if(pos <= 0 || pos > n + 1){
		cout << "Vi tri chen khong hop le !\n"; return;
	}
	if(pos == 1){
		insertFirst(a); return;
	}
	else if(pos == n + 1 ){
		insertLast(a); return;
	}
	sv p = a;
	for(int i = 1; i < pos - 1; i++){
		p = p->next;
	}
	sv tmp = makeNode();
	tmp->next = p->next;
	p->next = tmp;
}
 

void deleteFirst(sv &a){
	if(a == NULL) return;
	a = a->next;
}
 

 void deleteLast(sv &a){
	if(a == NULL) return;
	sv truoc = NULL, sau = a;
	while(sau->next != NULL){
		truoc = sau;
		sau = sau->next;
	}
	if(truoc == NULL){
		a = NULL;
	}
	else{
		truoc->next = NULL;
	}
}
 

 void deleteMiddle(sv &a, int pos){
	if(pos <=0 || pos > Size(a)) return;
	sv truoc = NULL, sau = a;
	for(int i = 1; i < pos; i++){
		truoc = sau;
		sau = sau->next;
	}
	if(truoc == NULL){
		a = a->next;
	}
	else{
		truoc->next = sau->next;
	}
}
 
 void in(Student s){
	cout << "--------------------------------\n";
 	cout << "ID : " << s.id << endl;
 	cout << "Ho ten :" << s.name << endl;
     cout<<"Ngay/thang/nam sinh: "<<s.NgaySinh<<"/"<<s.ThangSinh<<"/"<<s.NamSinh<<endl;
     cout<<"Gioi tinh: "<<s.gioitinh<<endl; 
    cout<<"Diem toan: "<<s.Diemtoan<< "||   "<<"Diem ly: "<<s.Diemly<< "||   "<<"Diem hoa: "<<s.Diemhoa<<endl;
    cout<<"Diemtb: "<<s.DTB<<endl;
    cout<< "--------------------------------------\n";
}
 
void inds(sv a){
	cout << "Danh sach sinh vien :\n";
	while(a != NULL){
		in(a->s);
		a = a->next;
	}
	cout <<endl;
}
 
 void sapxepDTB(sv &a){
	for(sv p = a; p->next != NULL; p = p->next){
		sv max = p;
		for(sv q = p->next; q != NULL; q = q->next){
			if(q->s.DTB > max->s.DTB){
				max = q;
			}
		}
		Student tmp = p->s;
		p->s = max->s;
		max->s = tmp;
	}
}
 void sapxepid(sv &a){
	for(sv p = a; p->next != NULL; p = p->next){
		sv min = p;
		for(sv q = p->next; q != NULL; q = q->next){
			if(q->s.id < min->s.id){
				min = q;
			}
		}
		Student tmp = min->s;
		min->s = p->s;
		p->s = tmp;
	}
} 
 void sapxepdcn(sv &a){
	int max = 0;
	sv temp;
	for(sv p = a;p != NULL;p = p->next){
	    if(p->s.DTB > max){
	        max = p->s.DTB;
	        temp = p;
	    }
	}
    in(temp->s);
} 
 void sapxepdtn(sv &a){
	int min =10;
	sv temp;
	for(sv p = a;p != NULL;p = p->next){
	    if(p->s.DTB < min){
	        min = p->s.DTB;
	        temp = p;
	    }
	}
    in(temp->s);
} 


 void timkiemsv(sv &a){
   string  ma;
   cout<<"Nhap ma sinh vien can tim: ";
   fflush(stdin) ;
   getline(cin,ma); 

	for(sv p = a;p != NULL;p = p->next){
	    if(p->s.id.compare(ma)==0){
	       	in(p->s);
	}
	}

} 

 void nhanphim(){
	  do{
        cout<<"\nnhap phim bat ki de tiep tuc\n";
     }while(getch() == false  );
            
            system("cls");
}
 
 int main(){
	sv head = NULL;
	int lc;
	do{
		cout << "-----------------MENU---------------\n";
		cout << "1. Chen sinh vien vao dau danh sach\n";
		cout << "2. Chen sinh vien vao cuoi danh sach\n";
        cout << "3. Chen sinh vien vao giua danh sach\n";
		cout << "4. Xoa sinh vien o dau danh sach\n";
		cout << "5. Xoa sinh vien o cuoi danh sach\n";
		cout << "6. Xoa sinh vien  o giua\n";
		cout << "7. Hien thi danh sach sinh vien\n";
		cout << "8. Sap xep cac sinh vien diemtb cao den thap\n";
		cout << "9. Sap xep cac sinh vien theo id\n";
		cout << "10. Sinh vien diem tb cao nhat va thap nhat\n";
		cout << "11. So luong sinh vien trong danh sach\n";
		cout << "12. Tim kiem sinh vien theo ma id \n "; 
		cout << "0. Thoat !\n";
		cout << "-------------------------------------\n";
		cout << "Nhap lua chon :";
		 cin >> lc;
	
        switch(lc){
            case 1:  
			          {
			insertFirst(head);
			nhanphim(); 
                break; 
						 }   
            
            case 2:{ 
			insertLast(head);
			nhanphim();
				break;
			} 
            case 3:{
				 int pos; cout << "Nhap vi tri can chen :"; cin >> pos;
			insertMiddle(head, pos);
			nhanphim();
                   break;
			}
           
            case 4:{
			deleteFirst(head);
			nhanphim();
                    break;
			}
            
            case 5:{
			deleteLast(head);
			nhanphim();
                   break;
			}
            
            case 6:
            	{
            	 int pos;
			 cout << "Nhap vi tri can xoa:"; cin >> pos;
			deleteMiddle(head, pos);
			nhanphim();
                    break;	
				}
           
            case 7:	{
				 inds(head);
			nhanphim();
                    break;
				}
           
            case 8:{
			sapxepDTB(head);
			inds(head);
			nhanphim();
                   break;
			}
            
            case 9:{
			sapxepid(head);
			inds(head);
			nhanphim();
		}
		case 10:{
			sapxepdcn(head);
			sapxepdtn(head);
			nhanphim();
		}
		case 11:{
		    int count = Size(head);
		    cout << "Tong so luong sinh vien luc nay la: "<< count <<"\n";
		    nhanphim();
		    break;
		}
		case 12:{
		timkiemsv(head);
		nhanphim();
		 	break;
		} 
		case 0:
			{
				cout<<"thoat...";
				break;
			}
            default:
                cout << "Lua chon khong phu hop!!!!\n" ;
            }

    }while(lc!=0);
		
	return 0;
}
