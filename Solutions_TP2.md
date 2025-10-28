# Solutions TP2

## EX1_TP2 (avec S.A.S.R)
```c
// corrigé EX1_TP2 avec S.A.S.R 
#include<stdio.h> 
#include<stdlib.h> 
int main() 
{ 
    //declaration 
    float X,Y; 
    //preparation du traitement 
    printf("donner deux reels quelconques X et Y\n"); 
    scanf("%f%f",&X,&Y); 
    //traitement 
    if(X==Y) 
        printf(" X et Y sont Egaux \n"); 
    if(X!=Y) 
        printf("X et Y sont differents \n"); 
} 
```

## EX1_TP2 (avec S.A.complète)
```c
// corrigé EX1_TP2 avec S.A.complète 
#include<stdio.h> 
#include<stdlib.h> 
int main() 
{ 
    //declaration 
    float X,Y; 
    //preparation du traitement 
    printf("donner deux reels quelconques X et Y\n"); 
    scanf("%f%f",&X,&Y); 
    //traitement 
    if(X==Y) 
        printf(" X et Y sont Egaux \n"); 
    else 
        printf("X et Y sont differents \n"); 
} 
```

## EX1_TP2 (avec combinaison de condition)
```c
// corrigé EX1_TP2 avec combinaison de condition 
#include<stdio.h> 
#include<stdlib.h> 
int main() 
{ 
    //declaration 
    float X,Y; 
    //preparation du traitement 
    printf("donner deux reels quelconques X et Y\n"); 
    scanf("%f%f",&X,&Y); 
    //traitement 
    if((X>Y)||(X<Y)) 
        printf("X et Y sont differents \n"); 
    if(X==Y) 
        printf(" X et Y sont Egaux \n"); 
} 
```

## EX2_TP2_3 (Version avec switch)
```c
// Corrigé EX2_TP2_3    
#include<stdio.h> 
#include<stdlib.h> 
#include<math.h> 
int main() 
{ 
    //declaration 
    int I,N; 
    //preparation du traitement 
    printf("donner N \n"); 
    scanf("%d",&N); 
    //traitement 
    switch(N) 
    { 
        case 1: 
        { 
            printf(" Noir \n"); 
            break; 
        } 
        case 2: 
        {  
            printf(" Bleu \n"); 
            break; 
        } 
        case 3: 
        {  
            printf(" Vert\n"); 
            break; 
        } 
        case 4: 
        { 
            printf(" Jaune \n"); 
            break; 
        } 
        case 5: 
        {  
            printf(" Rouge \n"); 
            break; 
        } 
        case 6: 
        {  
            printf(" Blanc\n"); 
            break; 
        } 
        default: 
        {  
            printf(" Couleur non predefinie\n"); 
            break; 
        } 
    } 
    printf("FIN \n"); 
} 
```

## EX2_TP2_4 (Version avec variables booléennes)
```c
/*corrigé EX2_TP2_4   */ 
#include<stdio.h> 
#include<stdlib.h> 
#include<stdbool.h> 
int main() 
{ 
    //declaration 
    int N; 
    bool C1,C2,C3,C4,C5,C6,C7; 
    //preparation du traitement 
    printf("donner N \n"); 
    scanf("%d",&N); 
    //traitement 
    C1=(N==1); 
    C2=(N==2); 
    C3=(N==3); 
    C4=(N==4); 
    C5=(N==5); 
    C6=(N==6); 
    if(C1) printf(" Noir \n"); else 
    if(C2) printf(" Bleu \n"); else 
    if(C3) printf(" Vert\n"); else 
    if(C4) printf(" Jaune \n"); else 
    if(C5) printf(" Rouge \n"); else 
    if(C6) printf(" Blanc\n"); else 
           printf(" Couleur non predefinie\n"); 
    printf("FIN \n");
}
```

---

*Algorithmique et programmation 1*  
Prof. G. Mangoub