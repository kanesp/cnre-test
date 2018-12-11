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
89programming exercise43
#include <stdio.h>
void  fun( char *a )
{
	char *t=a;
	int i,j=0,m=0,n=0;
	while(t)
	{
		t++;
	m++;}
	while(*t=='*')
	{ t--;
	n++;}
	for(i=0;i<m-n;i++)
		a[j++]=t[i];
	a[j]='\0';


}

void main()
{  char  s[81];void NONO ();
   printf("Enter a string:\n");gets(s);
   fun( s );
   printf("The string after deleted:\n");puts(s);
   NONO();
}
void NONO ()
{/* ±¾º¯ÊýÓÃÓÚ´ò¿ªÎÄ¼þ£¬ÊäÈëÊý¾Ý£¬µ÷ÓÃº¯Êý£¬Êä³öÊý¾Ý£¬¹Ø±ÕÎÄ¼þ¡£ */
  FILE *in, *out ;
  int i ; char s[81] ;
  in = fopen("in.dat","r") ;
  out = fopen("out.dat","w") ;
  for(i = 0 ; i < 10 ; i++) {
    fscanf(in, "%s", s) ;
    fun(s) ;
    fprintf(out, "%s\n", s) ;    
  }
  fclose(in) ;
  fclose(out) ;
}
