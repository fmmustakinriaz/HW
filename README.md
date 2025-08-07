#include<stdio.h>

void deleteValue(int a[],int b)
{
   int n;
   printf("\nEnter search value :");
   scanf("%d",&n);
   //Search value
   int c= valueSearch(a,b,n);
   printf("\nSearch value index :%d\n",c);
   for(int i=c;i<b-1;i++)
   {
     a[i]=a[i+1];


   }
   //deletion array
   for(int i=0;i<b-1;i++)
   {

      printf("\n modify value %d ",a[i]);
   }
}
int valueSearch(int a[],int b,int n)
{

    int cnt=0;
    printf("Search a value:");
    for(int i=0;i<b;i++)
    {

        if(n==a[i])
        {

            cnt=i;
            break;
        }
    }
    return cnt;
}
void frequency(int a[],int b)
{

    int cnt[100]={0};
    for(int i=0;i<b;i++)
    {
        cnt[a[i]]++;
    }
    printf(" count frequency:\n");
      int g=sizeof(cnt)/sizeof(cnt[0]);
    for(int i=0;i<g;i++)
    {


    if(cnt[i]>0)
    {
        printf("\n%d frequency :%d\n",i,cnt[i]);
    }

    }
}
void insert(int a[],int b)
{

    a[b+1];
    int j;
    printf("\nAdd a index element : ");
    scanf("%d",&j);

    for(int i=0;i<b-1;i++)
    {

        a[b-i]=a[b-i-1];
    }

     a[2]=j;
    printf("\nAfter add value:");
    for(int i=0;i<b+1;i++)
    {

        printf("%d ",a[i]);
    }
    printf("\n");
}
int main()
{
    //array declaration

    int k[5];
    //arrays value assigning
    printf("Enter array element :");
    for(int i=0;i<5;i++)
    {

        //arrays value access
        scanf("%d",&k[i]);

    }
    int v;

    printf("1.deletion & search a value :\n");
    printf("2.frequency count:\n");
    printf("3.insert a value:\n");
    printf("\nChoice operation :");
    scanf("%d",&v);
    if(v==1)
    {
       deleteValue(k,5);
    }
    else if(v==2)
    {

        frequency(k,5);
    }
    else if(v==3)
    {

        insert(k,5);
    }
    else
        printf("\nChoice not  found:");


}
