#include<stdio.h>
int main()
{
    int i=0;
    char ch[100];
    printf("Enter your password:");
    for(;;)
    {
        ch[i]=_getch();
        if(ch[i]=='\r')
        break;
        else if(ch[i]=='\b')
        {
            if(i!=0)
            {
             i=i-1;
             printf("\b \b");
            }
        }
        else
        {
        printf("%c",ch[i]);
        i++;
        }
    }
    ch[i]=NULL;
    printf("\n%s",ch);
    return 0;
}
