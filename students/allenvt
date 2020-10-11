
#include<stdio.h>uuu
void main()
{
 int n,i,j,TEMP,TEMP1,TEMP2,TEMP3,TEMP4;
 float WTSUM=0,TATSUM=0;
 int ct[10],tat[10],wt[10],a[20][20];
 printf("enter the no of  process\n");
 scanf("%d",&n);
 for(i=1;i<=n;i++)
 {
  printf("Enter the arrival time of p%d:\t",i);
  scanf("%d",&a[i][1]);
  printf("Enter burst time of p%d: \t",i);
  scanf("%d",&a[i][2]);
  printf("Enter the priority :\t");
  scanf("%d",&a[i][3]);
  a[i][0]=i;
  printf("\n");
 }
 ct[0]=0;
    if(a[1][2]>=a[n][1])
    {
        ct[1]=a[1][2]+a[1][1];
        tat[1]=ct[1]-a[1][1];
        wt[1]=tat[1]-a[i][2];
        wt[1]=0;
  WTSUM=wt[1];
  TATSUM=tat[1];
        for(i=2;i<=n;i++)
        {
            for(j=i+1;j<=n;j++)
            {
                if(a[j][3]<a[i][3])
                {
                    TEMP4=a[i][3];
                    a[i][3]=a[j][3];
                    a[j][3]=TEMP4;
                    TEMP1=a[i][2];
                    a[i][2]=a[j][2];
                    a[j][2]=TEMP1;
                    TEMP2=a[i][1];
                    a[i][1]=a[j][1];
                    a[j][1]=TEMP2;
                    TEMP3=a[i][0];
                    a[i][0]=a[j][0];
                    a[j][0]=TEMP3;
                }
            }
                if(ct[i-1]<a[i][1])
                {
                    TEMP=a[i][1]-ct[i-1];
                    ct[i]=ct[i-1]+a[i][2]+TEMP;
                    TEMP1=a[i][2];
                }
                else
                {
                    ct[i]=ct[i-1]+a[i][2];
                }
                tat[i]=ct[i]-a[i][1];
                wt[i]=tat[i]-a[i][2];
                WTSUM=WTSUM+wt[i]+wt[1];
                TATSUM=TATSUM+tat[i]+tat[1];
       }
   }
            if(a[n][1]=0)
            {
            ct[0]=0;
            for(i=1;i<=n;i++)
                {
                    for(j=i+1;j<=n;j++)
                    {
                        if(a[j][3]<a[i][3])
                        {
                            TEMP4=a[i][3];
                            a[i][3]=a[j][3];
                            a[j][3]=TEMP4;
                          TEMP1=a[i][2];
                          a[i][2]=a[j][2];
                          a[j][2]=TEMP1;
                        TEMP2=a[i][1];
                        a[i][1]=a[j][1];
                        a[j][1]=TEMP2;
                        TEMP3=a[i][0];
                    a[i][0]=a[j][0];
                    a[j][0]=TEMP3;
                        }
                    }
                if(ct[i-1]<a[i][1])
                {

                    TEMP=a[i][1]-ct[i-1];
                    ct[i]=ct[i-1]+a[i][2]+TEMP;
                    TEMP1=a[i][2];
                }
                else
                {
                    ct[i]=ct[i-1]+a[i][2];
                }
            tat[i]=ct[i]-a[i][1];
            wt[i]=tat[i]-a[i][2];
            WTSUM=WTSUM+wt[i];
           TATSUM=TATSUM+tat[i];
        }
    }
 printf("\n\n\n");
 printf("\tPROCESS\tBT\tAT\tPT\tTAT\tWT\n");
 for(i=1;i<=n;i++)
 {
 printf("\tP%d\t%d\t%d\t%d  \t%d\t%d\n\n",a[i][0],a[i][2],a[i][1],a[i][3],tat[i],wt[i]);
 }
 printf("Average_waiting_time = %f\n",WTSUM/n);
 printf("Average_turn_around_time= %f\n",TATSUM/n);
 printf("\n\n");
 printf("Gantt chart\n");
 for(i=1;i<=n;i++)
 {
  printf("\tP%d\t",a[i][0]);

 }
 printf("\n");
 for(i=1;i<=n;i++)
 {
 printf("\t%d\t",ct[i]);
 }
}
