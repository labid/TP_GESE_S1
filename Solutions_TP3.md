# Solutions TP3

## EX1_TP3 (Calcul des Combinaisons)
```c
#include <stdio.h>

int main()
{
    //declaration 
    int I,N,P,NMP; 
    float FACTN,FACTP,FACTNMP,CNP; 
     
    //preparation du traitement 
    printf("donner un entier N>0\n"); 
    scanf("%d",&N); 
    printf("donner un entier P>0 et <N\n"); 
    scanf("%d",&P); 
    
    //traitement 
    FACTN=1;FACTP=1;FACTNMP=1;  //initialisation 
    
    //calcul de N! 
    for(I=2;I<=N;I++) 
        FACTN=FACTN*I; 
    printf("FACTN=%f \n", FACTN); 
    
    //calcul de P!      
    for(I=2;I<=P;I++) 
        FACTP=FACTP*I; 
    printf("FACTP=%f \n", FACTP); 
    
    //calcul de (N-P)! 
    NMP=N-P;      
    for(I=2;I<=NMP;I++) 
        FACTNMP=FACTNMP*I; 
    printf("FACTNMP=%f \n", FACTNMP); 
    
    //calcul de CNP 
    CNP=FACTN/((FACTP)*(FACTNMP));   
    printf("CNP=%f \n", CNP);    
    printf("FIN \n");
    
    return 0;
}
```


*Algorithmique et programmation 1*  
## EX2_TP3 (Combinaisons avec contrôle de saisie)
```c
#include <stdio.h>

int main()
{
    //declaration 
    int I,N,P,NMP; 
    float FACTN,FACTP,FACTNMP,CNP; 
    
    //preparation du traitement 
    printf("donner un entier N>0\n"); 
    scanf("%d",&N); 
    printf("donner un entier P>0 et <N\n"); 
    scanf("%d",&P); 
    
    while((N<=0)||(P<=0)||(N<P)) 
    {
        printf("donner un entier N>0\n"); 
        scanf("%d",&N); 
        printf("donner un entier P>0 et <N\n"); 
        scanf("%d",&P); 
    }
    //traitement 
    FACTN=1;I=1;  //initialisation 
    //calcul de N! 
    while(I<N) 
    { 
        I=I+1; 
        FACTN=FACTN*I; 
    } 
    printf("FACTN=%f \n", FACTN); 
    //calcul de P!   
    FACTP=1;I=1;   //initialisation 
    while(I<P) 
    {  
        I=I+1; 
        FACTP=FACTP*I; 
    } 
    printf("FACTP=%f \n", FACTP); 
    //calcul de (N-P)! 
    NMP=N-P;    
    FACTNMP=1;I=1;  //initialisation 
    while(I<NMP) 
    {
        I=I+1; 
        FACTNMP=FACTNMP*I; 
    } 
    printf("FACTNMP=%f \n", FACTNMP); 
    //calcul de CNP 
    CNP=FACTN/((FACTP)*(FACTNMP));
        printf("CNP=%f \n", CNP);
        printf("FIN \n");
        return 0;
}
```
Prof. G. Mangoub
## EX3_TP3 (Combinaisons avec do...while)
```c
#include <stdio.h>

int main()
{
    //declaration 
    int I,N,P,NMP; 
    float FACTN,FACTP,FACTNMP,CNP; 
    
    //preparation du traitement 
    do 
    { 
        printf("donner un entier N>0\n"); 
        scanf("%d",&N); 
        printf("donner un entier P>0 et <N\n"); 
        scanf("%d",&P); 
    } 
    while((N<=0)||(P<=0)||(N<P)); 
    //traitement 
    FACTN=1;I=1;  //initialisation 
    //calcul de N! 
    do 
    { 
        I=I+1; 
        FACTN=FACTN*I; 
    } 
    while(I<N); 
    printf("FACTN=%f \n", FACTN); 
    //calcul de P!   
    FACTP=1;I=1;   //initialisation 
    do 
    {  
        I=I+1; 
        FACTP=FACTP*I; 
    } 
    while(I<P); 
    printf("FACTP=%f \n", FACTP); 
    //calcul de (N-P)! 
    NMP=N-P;    
    FACTNMP=1;I=1;  //initialisation 
    do 
    {
        I=I+1; 
        FACTNMP=FACTNMP*I; 
    } 
    while(I<NMP); 
    printf("FACTNMP=%f \n", FACTNMP); 
    //calcul de CNP 
    CNP=FACTN/((FACTP)*(FACTNMP));   
    printf("CNP=%f \n", CNP);    
    printf("FIN \n"); 
    return 0;
}
```