# MarketBilling
#include<stdio.h>
#include<math.h>
float func(int x)
{
    return (x*x)-(4*x)+4;;
}
int bisect(int p,int q)
{
    int a,b,c;
    c=(a+b)/2;
    float r=func(a)*func(b);
    if(r<0)
        b=c;
    else
        a=c;

}
int interval(int a,int b)
{
    int res=func(a)*func(b);
    if(res>0)
        return res;
    else if(res<0)
        bisect(a,b);
}
int main()
{
    int n,i,a,b,pro;
    printf("Enter the no of iterations:-");
    scanf("%d",&n);
    do
    {
        printf("\nEnter the intervals:-");
        scanf("%d%d",&a,&b);
        pro=interval(a,b);
    }while(pro>0);

return 0;
}
