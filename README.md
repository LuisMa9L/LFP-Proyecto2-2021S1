# [LFP]Proyecto 2 - Archivos de Entrada

Universidad de San Carlos de Guatemala  
Facultad de Ingeniería  
Escuela de Ciencias y Sistemas  
Lenguajes Formales y de Programación  
Primer Semestre 2021

Nota: El simbolos `$` representa a `ε` (Producción vacía)

### [gramaticas1.glc](gramticas1.glc)
```
Grm1
S,A,B,C;a,b,z,$;S
S->A
A->a A a
A->B
B->b B b
B->C
C->z C
C->$
*
Gramatica2
A,B,C,D;0,1;A
A->1 B
A->0 C
B->1 A
B->0 D
C->1 D
C->0
D->1 C
C->0 A
D->0 B
*
```


### [gramaticas2.glc](gramticas2.glc)
```
parparentesis
A,B;(,),0,1;A
A->B
B->( ( B ) )
B->1
B->0
*
abb
A,B,C;a,b;A
A->B
B->a C
C->a C b b
C->b b
*
sumarnumeros
A,B,N,NP,NUMERO,D;sumar,(,),:,0,1,2,3,4,5,6,7,8,9,$;A
A->B
B->sumar ( N )
N->NUMERO NP
NP->: NUMERO NP
NP->$
NUMERO->D NUMERO
NUMERO->$
D->0
D->1
D->2
D->3
D->4
D->5
D->6
D->7
D->8
D->9
*
```
