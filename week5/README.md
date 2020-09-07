Write a program that uses functions to perform the following operations on Double linked
list.:
i) Creation 
ii) Insertion 
iii) Deletion
 iv) Traversal
PROGRAM:
#include<stdio.h>
#include<stdlib.h>
struct node
{
       float data;
       struct node*prev;
       struct node*next;
};
struct node* head=NULL,*tail=NULL,*cur,*t1,*t2;
void create()
{ 
        int n;
        printf("Enter the number of nodes\n");
        scanf("%d",&n);
        for(i=0;i<=n;i++)
        {
                 cur = (struct node*)malloc(sizeof(struct node));
                 print("ENTER CURRENT NODE DATA\n");
                 scanf("%f",&(cur->data));
                 cur -> prev = NULL;
                 cur -> next = NULL;
                 if(head == NULL)
                 {
                         head = tail = cur;
                 }
                 else
                 {
                         tail -> next = cur;
                         tail -> prev = cur;
                         tail = cur;
                 }
       }
}
void insert_at_begin()
{
        cur = (struct node*)malloc(sizeof(structnode));
        printf("ENTER CURRENT NODE DATA\n");
        scanf("%d",(&cur->data));
        cur->prev = NULL;
        cur->next = head;
        head->prev = cur;
        head = cur;
}
void insert_at_pos()
{
        int pos,c =1;
        cur = (struct node*)malloc(sizeof(structnode));
        printf("Enter the cur data element:\n");
        scanf("%d",(&cur->data));
        printf("Element the pos to insert:\n");
        scanf("%d",&pos);
        next = head;
        while(c<pos)
        {
                prev = next;
                next = next->link;
                c++;
        }
        prev->link = cur;
        cur->link = next;
}
void insert_at_end()
       cur = (struct node*)malloc(sizeof(structnode));
       printf("ENTER CURRENT NODE DATA\n");
       scanf("%f",(&cur->data));
       printf("Enter the position to perform insertion:\n);
       scanf("%d",&pos);
       t1 = head;
       while(c<pos && t1 != NULL)
       {
               t2 = t1;
               t1 = t1->next;     
               c++;
       }
       t2->next = cur;
       cur->prev = t2;
       cur->next = t1;
       t1->prev = cur;
    
}
void insert_before()
{
        int value;
        cur = (struct node*)malloc(sizeof(structnode));
        printf("ENTER CURRENT NODE DATA\n");
        scanf("%f",(&cur->data));
        printf("Enter before which node we need to perform insert");
        scanf("%d",&value);
        t1 = head;
        while(t1 != NULL && t1->data != value)
        {

              t2 = t1;
              t1 = t1->next;
        }
        t2->next = cur;
        cur->prev = t2;
        cur->next = t1;
        t1->prev = cur;
}
void insert_after()
{
        float value;
        cur = (struct node*)malloc(sizeof(structnode));
        printf(""ENTER CURRENT NODE DATA\n")
        scanf("%d",(&cur->data));
        printf("Enter after which node we need to perform insertion\n");
        scanf("%d",&value);
        t1 = head;
        while(t1 != NULL && t1->data != value)
        {
               t1 = t1->next;
        }
        t2=t1->next;
        cur->next = t2;
        t2->prev=NULL;
        t1->next=cur;
        cur->prev=t1;
}
void delete_at_begin()
{
        cur = head;
        head = head->next;
        head->prev = NULL;
        cur->next = NULL;
        printf("Deleted elements is %f",cur->data);
        free(cur);
}
void delete_at_end()
{
        cur = head;
        head = head->next;
        head->next = NULL;
        cur->prev = NULL;
        printf("Deleted element is %f",cur->data);
        free(cur);
}
void delete_at_pos()
{
         int c=1,pos;
         printf("Enter the position of deletion\n");
         scanf("%d",&pos);
         t1 = head;
         while(c<pos && t1 != NULL)
         {
                 t2 = t1;
                 t2 = t1->next;
                 c++;
         }
         t2->next = t1->next;
         t1->next->prev = t2;
         printf("deleted element is at %f",t1->data);
         free(t1);
}
void delete_before_node()
{
         float value;
         printf("Enter the data to delete before\n");
         scanf("%f",&value);
         t1 = head;
         while(t1->next->data !=value && t1->next != NULL)
         {
               t2 = t1;
               t1 = t1->next;
         }
         t2->next = t1->next;
         t1->next = prev = t2;
         printf("deleted element is at %f",t1->data);
         free(t1);
}
void delete_after_node()
{
         float value;
         printf("Enter after which node we need to delete");
         scanf("%f",&value);
         t1 = head;
         while(t1 != NULL && t1->data != value)
         {
               t2 = t1->next;
         }
         t2 = t1->next;
         t1->next = t2->next;
         t2->next->prev=t1;
         printf("deleted element is at %f",t2->data);
         free(t2);
}
void display_forward()
       
        if(head == NULL)
                 printf("DLL is empty");
        else
        {
                 cur = head;
                 printf("Elements of DLL are\n");
                 while(cur!=NULL)
                 {
                         printf("%f<->",cur->data);
                         cur = cur->next;
                  }
                  printf("NULL");
        }
}
void display_reverse()
{
        if(head! == NULL)
                  printf("Elements of DLL are\n");
        else                       
        {
             cur = tail;
             printf("Elements of DLL are\n");
             while(cur != NULL);
             {
                 printf("%d->",head->data);
                 cur = cur->prev;
              }
        }
}
void searching()
        
        int flag = 0;
        float value;
        printf("Enter the value to be searched:");
        scanf("%f",&value);
        int c = 1;
        t1 = head;
        while(t1 != NULL)
        {
                if(t1->data == value)         
                {
                       flag = 1;
                       break;
                }
                t1 = t1->next;
                c++;
        }
        if(flag == 1)
        {
                 printf("Element present in the list at %d position",c);
        }           
        else
                 printf("Element not present in the list");
           
}
void sorting()
{ 
        struct node *p1,*p2,*last = NULL;
        int i,c,t;
        do
        {
        c = 0;
        p1 = head;
        while(p1 -> next != last)
        {
                if(p1->data > p1->next->data)
                {
                       t = p1->data;
                       p1->data = p1->next->data;
                       p1->next->data = t;
                 }
                 p1 = p1->next;
        }
        last = p1;
        }while(c);
       
}
int main()
{
        int ch;
        while(1)
        {
               printf("----------------------------------------\n");
               printf("program for doubled linked list\n");
               printf("1-create\n2-insert at begin\n3-insert at pos\n4-insert at end\n5-insert before pos\n");
               printf("6-insert after pos\n7-delete at begin\n8-delete at end\n9-delete at pos\n10-delete before node\n");
               printf("11-delete after node\n12-traversal\n13-reverse\n14-search\n15-sorting\n");
               printf("Enter your choice");
               scanf("%d",&ch);
               switch(ch)
               {
                       case 1: create();
                               break;
                       case 2: insert_at_begin();
                               break;
                       case 3: insert_at_pos();
                               break;
                       case 4: inser_at_end();
                               break;
                       case 5: insert_before_pos();
                               break;
                       case 6: insert_after_pos();
                               break;
                       case 7: delete_at_begin();
                               break;
                       case 8: delete_at_end();
                               break;
                       case 9: delete_at_pos();
                               break;
                       case 10: delete_before_node();
                                break;
                       case 11: delete_after_node();
                                break;
                       case 12: traversal();
                                break;
                       case 13: reverse(head);
                                break;
                       case 14: search();
                                break;
                       case 15: sorting();
                                break;
                       case 16: exit(0);
                                
                  }
                  }
                  return 0;

