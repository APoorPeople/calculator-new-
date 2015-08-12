#include <stdio.h>
#include <stdlib.h>
#include <string.h>
 
int main()
{
int y;
double shu1=0;
double shu2=0;
char fuhao;
 
do
{
  printf("\n         迷你计算器\n\n");
  printf("       1.数据输入\n\n");
  printf("       2.四则运算\n\n");
  printf("       0.退    出\n\n");
  printf("   请选择（0-2）\n");
   
  scanf("%d",&y);
  getchar();
  switch(y)
  {
    case 1: 
            shu1=0;
            shu2=0;
            fuhao=0;
            printf("请输入两个数字，空格分开：");
            scanf("%lf %lf",&shu1,&shu2);
            printf("\n输入完成： %lf   %lf\n",shu1,shu2);
            getchar();
            break;
    case 2: 
            printf("\n请输入运算符号（+ - * /）:");
            scanf("%c",&fuhao);
            getchar();
             
            if(fuhao == '+')
                printf("\n加法，运算结果：%lf\n",shu1+shu2);
            if(fuhao == '-')
                printf("\n减法，运算结果：%lf\n",shu1-shu2);
            if(fuhao == '*')
                printf("\n乘法，运算结果：%lf\n",shu1*shu2);
            if(fuhao == '/')
                printf("\n除法，运算结果：%lf\n",shu1/shu2);
         
            break;
    case 0:
            printf("    谢谢使用\n");
            exit(1);
    default:
            printf("    输入错误,请重新输入\n");
  }
}
while (y>0);
}
