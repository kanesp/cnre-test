# cnre-test
cnre test
#include<conio.h>
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
void fun(char *ss)
{
	int i;
	for(i=0;ss[i]!='\0';i++)
	{
		  if(i%2==1&&ss[i]>='a'&&ss[i]<='z')
			  ss[i]-=32;
	}
			
  
}
void main()
{
  FILE *wf;
  char tt[81],s[81]="abc4Efg";
  system("CLS");
  printf("\nPlease enter an string within 80 characters:\n");
  gets(tt);
  printf("\n\nAfter changing, the string\n  %s",tt);
  fun(tt);
  printf("\nbecomes\n %s\n",tt);
/******************************/
  wf=fopen("out.dat","w");
  fun(s);
  fprintf (wf,"%s",s);
  fclose(wf);
/*****************************/
}
