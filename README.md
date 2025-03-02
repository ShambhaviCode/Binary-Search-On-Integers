#include<stdio.h>
#include<stdlib.h>
int main(void)
{
int iaArr[100],iNum,i,iMid,iLow,iHigh,iFound,iKey;
printf("\nEnter the number of elements\n");
scanf("%d",&iNum);
printf("\nEnter the elements in ascending order\n");
for(i=0;i<=iHigh;i++)
scanf("%d",&iaArr[i]);
printf("\nEnter the key elemet\n");
scanf("%d",&iKey);
iFound=0;
iLow=0;
iHigh=iNum-1;
while(iLow<=iHigh)
{
iMid=(iLow+iHigh)/2;
if(iKey==iaArr[iMid])
{
iFound=1;
break;
}
else if(iKey<iaArr[iMid])
{
iHigh=iMid-1;
}
else
{
iLow=iMid+1;
}
}
if(iFound)
printf("\nKey element %d found at %d \n",iKey,iMid+1);
else
printf("\nKey element not found \n");
return 0;
}








