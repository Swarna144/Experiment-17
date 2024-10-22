# Experiment-17
Aim:
To study and implement Linked Lists.

Theory:
Singly linked list is a linear collection of data structures which consists of a sequence of elements where each element (also called a node) has two fields: one for storing the information and another which contains the address of the next element in the list. In almost all of the arrays data components are stored together in the memory whilst in a singly linked list, the data components are not kept together in the memory; every component is stored dynamically by pointing to the next one.

Components of Singly Linked Lists:
→ Node:
Each node contains data or the actual information or value of the node and next which is a pointer or reference to the next node in the list. If it’s the last node, this pointer is null or None.
→ Head:
The first node of the linked list. If the list is empty, the head is null.

Characteristics of Singly Linked Lists:
→ Dynamic Size.
→ Efficient insertions/ deletions of elements.
→ No reverse traversals.

CODE:-
```
#include<iostream>
using namespace std;

class Link {
    public:
    int data;
    Link* next;

    Link(int num){
        data=num;
        next=NULL;
    }
};
void insert_head(Link* &head, int data){
    Link* new_node=new Link(data);
    new_node->next = head;
    head = new_node;
}
void disp(Link* head){
    Link* temp = head;
    while(temp!=NULL){
        cout<<temp->data<<"->";
        temp = temp->next;
    }
    cout<<"NULL"<<endl;
}

int main(){
    Link* head = NULL;
    insert_head(head, 30);
    disp(head);
    insert_head(head, 32);
    disp(head);
    insert_head(head, 35);
    disp(head);
    //l1.disp();
}
```

OUTPUT:-

![Ex 17 JPG](https://github.com/user-attachments/assets/0b997bfb-fdbf-4062-b6d5-d662067830f8)
