# learning
## APCS 
```c
#include <stdio.h>
int AND(int a, int b);
int OR(int a, int b);
int XOR(int a, int b);
int main() {
    int a, b, c, t;
    
    while(scanf("%d %d %d", &a, &b, &c)!=EOF)
    {
        t=0;
        if(AND(a, b)==c)
        {
            printf("AND\n");
            t++;
        }
            
        if(OR(a, b)==c)
        {
            printf("OR\n");
            t++;
        }
        if(XOR(a, b)==c)
        {
            printf("XOR\n");
            t++;
        }
        if(t==0) printf("IMPOSSIBLE");
        
    }

    return 0;
}

int AND(int a, int b)
{
    if(a!=0 && b!=0) return 1;
    else return 0;
}
int OR(int a, int b)
{
    if(a==0 && b==0) return 0;
    else return 1;
}
int XOR(int a, int b)
{
    if(a==0 && b==0) return 0;
    else if(a!=0 && b!=0) return 0;
    else return 1;
}
