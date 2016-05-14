# calculator
primer calculadora con c++


#include<stdio.h>
#include<Windows.h>
#include<math.h>

int suma(int digito1, int digito2);
int resta(int digito1, int digito2);
int multiplicar(int digito1, int digito2);
int dividir(int digito1, int digito2);
double raiz(double digito1);
double exponente(double digito1, double digito2);
int vector(int vec1);


//float suyma(float,float);


int main()
{
	int dig1, dig2, vec1;
	double dig3, dig4, resultado;
	int opc;
	do
	{
		printf("Elige:\n1.-Funcion suma.\n2.-Funcion resta.\n3.-Funcion multiplicar.\n4.-Funcion dividir.\n5.-Funcion raiz cuadrada.\n6.-exponente a la 'n'.\n");
		printf("7.-Funcion vector que se llena y se despliega.\n8.-Salir.\n");
		scanf("%d", &opc);
		switch(opc)
		{
		case 1:
			system("cls");
			printf("Esta opcion realiza la suma de dos digitos.\n");
			printf("Dame el primer digito: ");
			scanf("%d", &dig1);
			printf("Dame el segundo digito: ");
			scanf("%d", &dig2);
			printf("El resultado es: %d", suma(dig1,dig2));
			getchar();
			getchar();
			system("cls");
			break;

		case 2:
			system("cls");
			printf("Esta opcion realiza la resta de dos digitos.\n");
			printf("Dame el primer digito: ");
			scanf("%d", &dig1);
			printf("Dame el segundo digito: ");
			scanf("%d", &dig2);
			printf("El resultado es: %d", resta(dig1,dig2));
			getchar();
			getchar();
			system("cls");

			break;

		case 3:
			system("cls");
			printf("Esta opcion realiza la multiplicacion de dos digitos.\n");
			printf("Dame el primer digito: ");
			scanf("%d", &dig1);
			printf("Dame el segundo digito: ");
			scanf("%d", &dig2);
			printf("El resultado es: %d", multiplicar(dig1,dig2));
			getchar();
			getchar();
			system("cls");

			break;

			case 4:
			system("cls");
			printf("Esta opcion realiza la division de dos digitos.\n");
			printf("Dame el primer digito: ");
			scanf("%d", &dig1);
			printf("Dame el segundo digito: ");
			scanf("%d", &dig2);
			printf("El resultado es: %d", dividir(dig1,dig2));
			getchar();
			getchar();
			system("cls");

			break;

			case 5:
			system("cls");
			printf("Esta opcion realiza la raiz cuadrada.\n");
			printf("Dame el numero para raiz:\n");
			scanf("%lf", &dig3);
			printf("El resultado es: %lf", raiz(dig3));
			getchar();
			getchar();
			system("cls");
			break;

			case 6:
			system("cls");
			printf("Esta opcion realiza la x^n.\n");
			printf("Dame el numero a exponenciar:\n");
			scanf("%lf", &dig3);
			printf("Dame el numero de exponente:\n");
			scanf("%lf", &dig4);
			printf("El resultado es: %lf", exponente(dig3,dig4));
			getchar();
			getchar();
			system("cls");
			break;

			case 7:
			system("cls");
			printf("Esta opcion realiza pedir el tamaño de vector, llenarlo y desplegarlo.\n");
			printf("Dame el tamano de el vector:\n");
			scanf("%d", &vec1);
			system("cls");
			vector(vec1);
			getchar();
			getchar();
			system("cls");
			break;

		}

	getchar();
	}while(opc != 8);



}


int suma(int digito1, int digito2)
{
	return(digito1+digito2);
}


int resta(int digito1, int digito2)
{
	return(digito1-digito2);
}

int multiplicar(int digito1, int digito2)
{
	return(digito1*digito2);
}

int dividir(int digito1, int digito2)
{
	
	return(digito1/digito2);

}

double raiz(double digito1) 
{
	double resultado;
	sqrt(digito1);
	resultado = sqrt(digito1);
	return(resultado);

}


double exponente(double digito1, double digito2)
{
	double resultado1;
	pow(digito1,digito2);
	resultado1= pow(digito1,digito2);
	return(resultado1);

}

int vector(int vec1)
{
	int i, vec[50];
	for(i=0; i<vec1; i++)
	{
		printf("Teclea digito en %d:", i);
		scanf("%d", &vec[i]);
	}
	system("cls");
	printf("Tus numeros son:\n");
	for(i=0; i<vec1; i++)
	{
		printf("\nEn la casilla %d: %d",i, vec[i]);
	}
	
	
}
	
