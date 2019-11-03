# list
#include<stdio.h>
#define success_value 99999
#define null_value -99999

struct listNode
{
    int item;
    struct listNode *next;
};
struct listNode *list;
void initialize()
{
    list = 0;
}
void insertItem(int value)
{
    struct listNode *newNode;
    newNode=(struct listNode*)malloc(sizeof(struct listNode));
    newNode->item = value;
    newNode->next = list;
    list = newNode;

}
void print()
{
  struct listNode *temp;
   temp = list;
   while(temp!=0)
   {
       printf("%d ",temp->item);
       temp = temp->next;
   }
}
int main()
{
    int input;
    initialize();
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    print();
}
