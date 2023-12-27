#include <stdio.h>
#include <stdlib.h>
// Programa que pide un número al usuario y le devuelve los números que son múltiplos de 3 y 5, en el intervalo entre cero y el número dado usando pilas 
// This program gives us the multiples of 3 and 5 between 0 and a number gived by the user
// all comments in this program are written in spanish, so sorry if you dont speak spanish, if you need use translator, i hope this code could help you for your homework or something similar

struct pila1 // creamos una pila para guardar los números múltiplos del 3
{
	int numero;
	struct pila1*sig;
};
struct pila1 *head1=NULL; // creamos un apuntador que indique el último elemento agregado a la pila

struct pila2 // creamos una pila para guardar los números múltiplos del 5
{
	int numero;
	struct pila2 *sig;
};
struct pila2 *head2=NULL; // creamos un apuntador que indique el último elemento agregado a la pila

void push1(int num) // creamos una función para agregar números a la pila de números múltiplos del 3
{
	struct pila1 *nuevo; // creamos un apuntador tipo struct pila1 para agregar un nuevo número a la pila
	nuevo=(pila1*)malloc(sizeof(pila1)); // reservamos espacio en la memoria para agregar un nuevo número a la pila
	(*nuevo).numero=num; // guardamos el número en la pila
	(*nuevo).sig=head1; // enlazamos cada nodo con el siguiente
	head1=nuevo; // hacemos que el apuntador head1 apunte al último elemento agregado
}

void push2(int num) // creamos una función para agregar números a la pila de números múltiplos del 5 (es practicamente igual a push1)
{
	struct pila2 *nuevo;
	nuevo=(pila2*)malloc(sizeof(pila2));
	(*nuevo).numero=num;
	(*nuevo).sig=head2;
	head2=nuevo;
}

void imprimir1() //funcion para imprimir números múltiplos del 3
{
	struct pila1 *aux; // creamos un apuntador auxiliar
	aux=head1; //hacemos que el apuntador auxiliar que creamos apunte a head1
	do //creamos un ciclo do while para imprimir todos los números de la pila que guarda los números múltiplos del 3
	{
		printf ("%d\t",(*aux).numero);// imprimimos el número dentro del nodo al cual apuntamos
		aux=(*aux).sig; //pasamos al siguiente número en la pila 
	}
	while (aux!=NULL); // el ciclo acaba cuando aux apunte a NULL
	
}

void imprimir2() //funcion para imprimir números múltiplos del 5 (es practicamente a la funcion para imprimir los números múltiplos del 3)
{
	struct pila2 *aux;
	aux=head2;
	do
	{
		printf ("%d\t",(*aux).numero);
		aux=(*aux).sig;
	}
	while (aux!=NULL);
	
}

void solution(int number)// función para guardar los números múltiplos de 3 y 5
{
	int b; // agregamos un contador para los números múltiplos de 3
	int c; // agregamos un contador para los números múltiplos de 3
	int i; // agregamos un contadort para el ciclo for
	b=0;
	c=0;
	for (i=1;i<number+1; i++)
	{
    	if(i%3==0) // evaluamos si el resto entre el número que estamos pasando y 3 es igual a cero
    	{
    		push1(i); //llamamos a la funcion push1 para agregar al número a la pila de los múltiplos de 3
    		b++;
    	}
    	if(i%5==0) // evaluamos si el resto entre el número que estamos pasando y 5 es igual a cero
    	{
    		push2(i); //llamamos a la funcion push2 para agregar al número a la pila de los múltiplos de 5
    		c++;
    	}
	}
	printf ("\n hay %d números que son múltiplos de 3 en el intervalo [0,  %d] y son los siguientes: \n",b,number);
	imprimir1();
  printf ("\n hay %d números que son múltiplos de 5 en el intervalo [0,  %d] y son los siguientes: \n",c,number);
	imprimir2();
	
}

int main () // función principal
{
	int a;
	printf ("ingrese un número mayor a cero \n");
	scanf ("%d",&a);
	if (a<=0)
	{
		printf ("\n ingrese un número válido");
	}
	else 
	{
		solution(a);		
	}
}
