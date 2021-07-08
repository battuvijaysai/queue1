#include<stdio.h>
#include<stdlib.h>
struct queue
{
    int rear,front,size;
    int a[5];
};
struct queue q;
void insert();
void delete();
void display();
int main()
{
    int choice;
    int queue_array[10];
    q.rear=-1;
    q.front=0;
    q.size=4;
    while(1)
    {
        printf("1.insert element to queue:\n");
        printf("2.delete element from queue:\n");
        printf("3.display all element from queue:\n");
        printf("4.quit\n");
        printf("enter your choice:");
        scanf("%d",&choice);
        void insert()
        {
            int add_item;
            if(q.rear=q.size-1)
            {
                printf("queue overflow");
            }
            else if(q.front==-1)
            {
                q.front=0;
                printf("insert the element in queue:");
                scanf("%d",&add_item);
                q.rear=q.rear+1;
                queue_array[q.rear]=add_item;
            }
        }
        void delete()
        {
            if(q.front==-1)
            {
                printf("que under flow\n");
                return;
            }
            else
            {
                printf("element deleted from queue is%d\n",q.front);
                q.front=q.front+1;
            }
        }
        void display()
        {
            int i;
            if(q.front==-1)
            {
                printf("queue is empty\n");
            }
            else
            {
                printf("queue is:\n");
                for(i=q.front;i<q.rear;i++)
                {
                    printf("%d",queue_array[i]);
                    printf("\n");
                }
            }
        }
        switch(choice)
        {
            case 1:insert();
            break;
            case 2:delete();
            break;
            case 3: display();
            break;
            default:exit(0);
        }
     }
}


