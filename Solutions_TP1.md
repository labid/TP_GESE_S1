# Solutions TP1

## EX1_TP1

```c
// Utilisation de quelques opérations avec des entiers
#include<stdio.h>
#include<stdlib.h>
int main()
{
    // Déclaration
    int A,B,C,X,Y,Z,W;
    // Préparation du traitement
    printf("donner trois entiers A,B et C\n");
    scanf("%d%d%d",&A,&B,&C);
    // Traitement
    X=A+B;
    Y=B*C;
    Z=A/C;
    W=A%(B+C);
    printf("X= %d \n",X);
    printf("Y= %d \n",Y);
    printf("Z= %d \n",Z);
    printf("W= %d \n",W);
    printf("FIN \n");
}
```

---

## EX2_TP1

```c
/* Ecrire un programme qui fait la permutation circulaire  
de quatre nombres lus au clavier. */
#include<stdlib.h>
#include<string.h>
int main()
{
    // Déclaration
    int A,B,C,D,ECH;
    // Préparation du traitement
    printf("Donner quatres entiers A,B,C et D \n");
    scanf("%d%d%d%d",&A,&B,&C,&D);
    ECH=A; A=D; D=C; C=B; B=ECH;
    printf("Apres permutation on a: \n");
    printf("A=%d et B=%d et C=%d et D=%d \n",A,B,C,D);
}
```

---

## EX3_TP1

```c
// EX4_TP2
#include <stdio.h>
#include <stdlib.h>
// Déclaration
int main()
{
    const char x=' ?', y='y', z='U';
    int X,Y,Z;
    // Traitement
    X = x;
    Y = y;
    Z = z;
    // Edition des résultats
    printf("le code ASCII du caractere %c est: %d\n",x, X);
    printf("le code ASCII du caractere %c est: %d\n",y, Y);
    printf("le code ASCII du caractere %c est: %d\n",z, Z);
    printf("FIN \n");
}
```

---

*Algorithmique et programmation 1*  
Prof. G. Mangoub
