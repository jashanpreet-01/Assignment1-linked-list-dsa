                            /* ASSIGNMENT 1(linked list)
                                Name: Jashanpreet Singh
                                 SID: 21104121
                                 Branch: Electrical Engineering */


#include <iostream>                   
using namespace std;                  

//CREATING NODE CLASSS
class Node{
    public:
    string name;
    int age;
    Node*next;  
    Node*prev;  
    //calling constructor
    Node(string name,int age){
        this->name=name;
        this->age=age;
        next=NULL;  
        prev=NULL;  
    }
};

// TO INSERT DATA AT END OF LINKED LIST
void append(Node* &head,string name,int age){  
    Node*temp=head;
    Node*new_node=new Node(name,age);
    //Inserting node in empty list
    if(temp==NULL){
        head=new_node;
    }
    //Either, in non empty list
    else{
        while(temp->next!=NULL){temp=temp->next;}
        temp->next=new_node;
        new_node->prev=temp;
    }
}

//FUNCTION TO INSERT DATA AT START OF LINKED LIST
void insert_at_head(Node*&head,string name,int age){
     Node*new_node=new Node(name,age);
     new_node->next=head;
    head->prev=new_node;
    head=new_node;
}

//FUNCTION TO DIPLAY DATA FROM START OF LINKED LIST
void display_from_start(Node*head){
    Node*temp=head;
    while(temp!=NULL){cout<<"[Name:"<<temp->name<<" Age:"<<temp->age<<"]"<<"<=>";temp=temp->next;}
    cout<<endl;
}

//FUNCTION TO DISPLAY DATA FROM END OF LINKED LIST
void display_from_end(Node*head){
    Node*temp=head;
    while(temp->next!=NULL){temp=temp->next;}
    while(temp!=NULL){cout<<"[Name:"<<temp->name<<" Age:"<<temp->age<<"]"<<"<=>";temp=temp->prev;}
    cout<<endl;
}

//FUNCTION TO DELETE ANY INDEX(0,n-1) EXCLUDING LAST ELEMENT 
void delete_ind(Node*&head,int i){
    if(i==0){
        Node*temp=head;
        head=temp->next;
        head->prev=NULL;
        delete temp;
    }
    else{
        Node*temp=head;
        for(int j=0;j<i;j++){temp=temp->next;}
        temp->prev->next=temp->next;
        temp->next->prev=temp->prev;
        delete temp;
    }
}

//FUNCTION TO DELETE LAST ELEMENT
void pop(Node*&head){
    Node*temp=head;
    while(temp->next!=NULL){temp=temp->next;}
    temp->prev->next=NULL;
    delete temp;
}

int main(){
     Node*head=NULL;
	int no_of_family_mem;
 	cout<<"Enter Number Of Family Members:";cin>>no_of_family_mem;
 	for(int i=1;i<=no_of_family_mem;i++){
		string name;
		int age;
		cout<<"Enter Family Member "<<i<<" Name:";cin.ignore();getline(cin,name);
		cout<<"Enter Family Member "<<i<<" Age:";cin>>age;
 		append(head,name,age);
	}
    cout<<endl; 
     cout<<"Doubly Linked list with my family members as elements is shown below:"<<endl;
    cout<<endl;
    display_from_start(head);
}
 

/*BONUS QUESTION
Q.Try to find a way to link the family members' doubly-linked list based on their relationship.
Ans.We can link the family members doubly-linked list  by sorting the doubly linked list according
to age in decending order.By doing so we will get a doubly linked list in which older generation 
people will be close to head in double linked list and new generation people will be close to tail
 in doubly linked list.



Name: Jashanpreet singh
SID: 21104121*/


