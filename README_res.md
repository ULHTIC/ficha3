**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**

# Resolução da Ficha de Exercícios - 3

1. Implemente um programa que escreve no ecrã a frase "O primeiro programa nunca se esquece!".

   *Resolução:*

   ```c
   void ex1 (void) {
       printf("\n\t******** Exercicio 1 ********\n");
       printf("O primeiro programa nunca se esquece!\n");
   }
   ```

2. O que faz o seguinte programa?

   ```c
   #include <stdio.h>
   
   int main(void)
   {
   	int x;
   	scanf( "%d", &x );
   	printf("%d\n", 2*x );
   	return 0;
   }
   ```

*Resolução: Lê um valor inteiro do teclado e imprime o valor multiplicado por 2.* 


3. Leia uma temperatura em graus Fahrenheit e apresente-a convertida em graus Celsius. A fórmula de conversão é: C = 5.0 ∗ (F − 32.0)/9.0, sendo C é a temperatura em graus Celsius e F a temperatura em graus Fahrenheit. 

   *Resolução:*

   ```c
   void ex3(void) {
   	float celsius,fahrenheit;
   	printf("\n\t******** Exercicio 3 ********\n");
   	printf("Insira a temperatura (graus Fahrenheit):\n");
   	scanf("%f", &fahrenheit);
   	celsius = 5.0 * (fahrenheit - 32.0)/9.0;
   	printf("A temperatura em Graus Celsius é de %f\n", celsius);
   }
   ```

2. Leia o valor do raio de um círculo. Calcule e imprima a área do círculo correspondente. A área do círculo é π ∗ raio² , considere π = 3.141592 (constante). 

   *Resolução:*

   ```c
   void ex4(void) {
   	const float Pi = 3.14F;
   	float raio, area;
   	printf("\n\t******** Exercicio 4 ********\n");
   	printf("Inira o raio de um círculo:\n");
   	scanf("%f", &raio);
   	area = Pi * (raio*raio);
   	printf("O valor da área do circulo é de %f\n", area);
   }
   ```

3. Faça um programa que peça ao utilizador 2 valores inteiros e coloque o primeiro valor numa variável chamada de A e o segundo valor noutra variável chamada de B. Em seguida, o seu programa deverá trocar o conteúdo destas variáveis e imprimir no ecrã o que cada variável contém.
   *Resolução:*

   ```c
   void ex5(void) {
   	int a, b, aux;
   	printf("\n\t******** Exercicio 5 ********\n");
   	printf("Insira um valor para a variável 'A':\n");
   	scanf("%d", &a);
   	printf("Insira um valor para a variável 'B':\n");
   	scanf("%d", &b);
   	printf("O valor inserido para a variável 'A' foi %d\n", a);
   	printf("O valor inserido para a variável 'B' foi %d\n", b);	
   
   	aux = a;
   	a = b;
   	b = aux;
   	puts("Depois da troca:");
   	printf("variável 'A': %d\n", a);
   	printf("variável 'B': %d\n", b);
   }
   ```
   
4. Faça um programa que peça ao utilizador 4 valores inteiros. Coloque estes valores nas variáveis a, b, c, d e imprima no ecrã o resultado da seguinte expressão:(a + b + c) x d
   *Resolução:*

   ```c
   void ex6(void) {
   	int a, b, c, d;
   	printf("\n\t******** Exercicio 6 ********\n");    
   	printf("Insira quatro numeros separados por virgula(',')\n");
   	scanf("%d,%d,%d,%d",&a,&b,&c,&d);
   	printf("o resultado da operação (a + b + c) * d) é: %d\n",(a + b + c) * d);
   }
   ```
   
5. Faça um programa que peça ao utilizador 4 notas de um aluno e imprima no ecrã a média desse aluno. 
   *Resolução:*

   ```c
   void ex7(void) {
   	float nota1, nota2, nota3, nota4, media;
       printf("\n\t******** Exercicio 7 ********\n");    
   	printf("Insira o valor da primeira nota:\n");
   	scanf("%f", &nota1);
   	printf("Insira o valor da segunda nota:\n");
   	scanf("%f", &nota2);
   	printf("Insira o valor da terceira nota:\n");
   	scanf("%f", &nota3);
   	printf("Insira o valor da quarta nota:\n");
	scanf("%f", &nota4);
   	media = (nota1+nota2+nota3+nota4)/4;
   	printf("O valor da média das notas é: %f\n", media);
   }
   ```
   
8. Considere um programa com as seguintes variáveis e respetivas inicializações:

    `unsigned char c = 3.14;` 
    `unsigned short int i = 3.14; `
    `unsigned int j = ‘B’; `
    `float f = ‘C’; `

    Usando o debugger (sem recorrer a printf()) verifique:

    - Qual é o valor efetivo f?

    - Qual o valor das variáveis quando se soma o valor 2 a cada uma delas?

    *Resolução:*

    ```c
    void ex8 (void) {
    	unsigned char c = 3.14;
    	unsigned short int i = 3.14;
    	unsigned int j = 'B';
    	float f = 'C';
    	printf("\n\t******** Exercicio 8 ********\n");
    	/* Usar o Debug e em "Debugging windows" abrir "Watches"*/
    	c = c + 2;
    	i = i + 2;
    	j = j + 2;
    	f = f + 2;
    }
    ```

9. Faça um programa que, a partir da leitura  das medidas dos lados de um retângulo (comprimento e largura), lidos do teclado, calcule e imprima a área e o perímetro do retângulo.
   *Resolução:*

   ```c
   void ex9(void){
   	int comp,larg;
   	printf("\n\t******** Exercicio 9 ********\n");    
   	printf("Insira o comprimento do retângulo:\n");
   	scanf("%d", &comp);
   	printf("Insira a largura do retângulo:\n");
   	scanf("%d", &larg);
   	printf("A área do retângulo é: %d\n", comp*larg);
   	printf("O perímetro é: %d\n", 2*(comp + larg));
   }
   ```

10. Faça um programa que leia pelo teclado um valor, em euros, converta e imprima o mesmo num valor     em dólares. Considere que €1 seja equivalente a US$ 1,23.
   *Resolução:*

   ```c
   void ex10(void){
   	float euros, dolares;
   	printf("\n\t******** Exercicio 10 ********\n");    
   	printf("Insira o valor em euros:\n");
   	scanf("%f", &euros);
   	dolares = euros*1.23;
       // imprimir com duas casas decimais (2 caracteres depois da virgula)
   	printf("O valor em dolares é: %.2f", dolares);
   }
   ```

11. A condição física de uma pessoa pode ser medida com base no cálculo do Índice de Massa Corporal     (IMC). O mesmo é calculado dividindo-se o peso desta pessoa em kg pelo quadrado da sua altura em m. Escreva um programa que leia o peso em kilograma e a altura de uma pessoa em metros, calcule e mostre o IMC. 

    *Se as entradas fossem 70.0kg para o peso e 1.80m para altura então a saída esperada seria aproximadamente 21.60.*
    *Resolução:*

    ```c
    void ex11(void){
    	float peso, altura, imc;
    	puts("\n\t******** Exercicio 11 ********");    
    	puts("Insira o seu peso (Kg):");
    	scanf("%f", &peso);
    	puts("Insira a sua altura (m):");
    	scanf("%f", &altura);
    	imc = peso/(altura*altura);
    	printf("O Índice de Massa Corporal (IMC) é de %.2f\n", imc);
    }
    ```

12. Escreva um programa que lê um certo número de segundos e dá o correspondente aos Dias, Horas, Minutos e Segundos.

     *Exemplo: 228184 segundos correspondem a 2 Dias e 15 Horas 23 Minutos e 4 Segundos.*

     *Resolução:*

   ```c
void ex12(void){
	int inputSeconds, inputSecondsCopy;
	int days, hours, minutes, seconds;
	puts("\n\t******** Exercicio 12 ********");
	puts("Insira o numero de segundos");
	scanf("%d", &inputSeconds);
	inputSecondsCopy = inputSeconds;

	// dividir pelo numero de segundos de 1 dia
	// um dia tem 24h e cada hora tem 60*60 segundos
	days = inputSeconds / (24 * 3600);

	// Calculo do resto da divisao anterior para saber quantos segundos sobram
	inputSeconds = inputSeconds % (24 * 3600);
	// Conversao dos segundos que sobrarm para horas
	hours = inputSeconds / 3600; 

	// Calculo do resto da divisao anterior para saber quantos segundos sobram
	inputSeconds %= 3600;
	// Conversao dos segundos que sobrarm para minutos
	minutes = inputSeconds / 60 ; 

	// Calculo do resto da divisao anterior para saber quantos segundos sobram
	inputSeconds %= 60; 
	seconds = inputSeconds; 

	printf("%d segundos correspondem a %d Dias e %d Horas %d Minutos e %d Segundos.\n", 		inputSecondsCopy, days, hours, minutes, seconds);
}
   ```

11. A importância de €780.000,00 será dividida entre três vencedores de um concurso. Sendo que da quantia total:

    - O primeiro vencedor receberá 46%

    - O segundo receberá 32%

    - O terceiro receberá o restante

    Calcule e imprima a quantia ganha por cada um dos vencedores.

   *Resolução:*

   ```c
#define FIRST_FACTOR 0.46
#define SECOND_FACTOR 0.32
#define THIRD_FACTOR (1-(FIRST_FACTOR + SECOND_FACTOR))
void ex13 (void){
	const float premio = 780000.00;
	float primeiro_premio = premio * FIRST_FACTOR;
	float segundo_premio = premio * SECOND_FACTOR;
	float terceiro_premio = premio * THIRD_FACTOR;
	puts("\n\t******** Exercicio 13 ********");
	printf("O valor do primeiro prémio é de %.2f euros.\n", primeiro_premio);
	printf("O valor do segundo prémio é de %.2f euros.\n", segundo_premio);
	printf("O valor do terceiro prémio é de %.2f euros.\n", terceiro_premio);
}
   ```
   
   

13. Faça um programa que leia um número inteiro e o imprima.

   *Resolução:*

   ```C
   void ex1 (void){
   	int num = 0;
   	printf("\n\t******** Exercicio 1 ********\n");	
   	printf("Insira um numero inteiro:\n");
   	scanf("%d",&num);
   	printf("O numero inteiro introduzido foi o: %d\n",num);
   }
   ```

   

14. Faça um programa que leia um número real e o imprima.

   *Resolução:*

   ```C
   void ex2 (void){
   	float num;
   	printf("\n\t******** Exercicio 2 ********\n");
   	printf("Insira um numero real:\n");
   	scanf("%f",&num);
   	printf("O numero real introduzido foi o: %f\n",num);
   }
   ```

   

15. Peça ao utilizador para digitar três valores inteiros e imprima a soma deles.

   *Resolução:*

   ```C
   void ex3 (void){
   	int n1,n2,n3;
   	printf("\n\t******** Exercicio 3 ********\n");	
   	printf("Insira tres valores inteiros:\n");
   	scanf("%d %d %d",&n1,&n2,&n3);
   	printf("O valor da soma: %d", n1+n2+n3);
   }
   ```

   

16. Leia um número real e imprima o resultado do quadrado desse número.

   *Resolução:*

   ```C
   void ex4 (void){
   	float num;
   	printf("\n\t******** Exercicio 4 ********\n");
   	printf("Insira um numero real:\n");
   	scanf("%f",&num);
   	printf("O quadrado de %f: %f",num,num*num);
   }
   ```

   

17. Crie um programa capaz de ler um caractere e imprimir o seu valor em decimal e hexadecimal.

   *Resolução:*

   ```C
   void ex5 (void){
   	char c;
   	printf("\n\t******** Exercicio 5 ********\n");	
   	printf("Insira um caractere:\n");
   	scanf(" %c",&c);
   	printf("O caractere '%c' tem como valor decimal %d e hexadecimal %x\n",c,c,c);
   }
   ```

   

18. Preencha a seguinte tabela com o resultado esperado (0 ou 1) depois de aplicar o “operador lógico” aos dois valores indicados.

| Valor 1 | Operador | Valor 2 | Resultado |
| ------- | -------- | ------- | --------- |
| 1       | &&       | 0       |           |
| 10      | &&       | 1       |           |
| 0       | &&       | 0       |           |
| 1       | \|\|     | 10      |           |
| 10      | \|\|     | 0       |           |
| 0       | \|\|     | 0       |           |

*Resolução:*

```C
void ex6 (void){
	printf("\n\t******** Exercicio 6 ********\n");
	printf("1 && 0 = %d\n", 1 && 0);
	printf("10 && 1 = %d\n", 10 && 1);
	printf("0 && 0 = %d\n", 0 && 0);
	printf("1 || 10 = %d\n", 1 || 10);
	printf("10 || 0 = %d\n", 10 || 0);
	printf("0 || 0 = %d\n", 0 || 0);
}
```

19. Indique qual o resultado das seguintes expressões. Assuma que todas as variáveis são inteiras:

- X = 5 && 6; 
- X = 5 && 0; 
- X = 5 > 2; 
- X = 5==6; 
- X = !5; 
- X = !0; 
- X = 5­3­2 || 1; 
- X = 5­6 || 1; 
- X = 5­7 || 0; 
- X = 0*3 || 5*0; 
- X = 0 || !0; 
- X = 50 >> 2; 
- X = 100 << 3

   *Resolução:*

   ```C
   void ex7 (void){
   	int X;
   	printf("\n\t******** Exercicio 7 ********\n");	
   	X = 5 && 6;
   	printf("5 && 6 = %d\n",X);
   	X = 5 && 0;
   	printf("5 && 0 = %d\n",X);
   	X = 5 > 2;
   	printf("5 > 2 = %d\n",X);
   	X = 5==6;
   	printf("5==6 = %d\n",X);
   	X = !5;
   	printf("!5 = %d\n",X);
   	X = !0;
   	printf("!0 = %d\n",X);
   	X = 532 || 1;
   	printf("532 || 1 = %d\n",X);
   	X = 56 || 1;
   	printf("56 || 1 = %d\n",X);
   	X = 57 || 0;
   	printf("57 || 0 = %d\n",X);
   	X = 0*3 || 5*0;
   	printf("0*3 || 5*0 = %d\n",X);
   	X = 0 || !0;
   	printf("0 || !0 = %d\n",X);
   	X = 50 >> 2;
   	printf("50 >> 2 = %d\n",X);
   	X = 100 << 3;
   	printf("100 << 3 = %d\n",X);
   }
   ```

20. Implemente uma função que recebe o número de quilómetros que percorreu e o número de litros de combustível que o automóvel consumiu e retorne o número de litros que este consome em média em 100 quilómetros. Use constantes para representar os vários fatores de conversão.

   *Exemplo de uma sessão de uso do programa (à frente do símbolo ‘>’ aparece o input do utilizador):*

   ```bash
   Qual o número de quilómetros que percorreu?
   > 100
   Qual o número de litros que consumiu?
   > 10
   Consumo aos 100 Km = 10
   ```
   
   *Resolução:*
   
   ```C
   float consumo (float km, float lts){
   	const int aos = 100;
   	return lts*aos/km;
   }
   void ex8 (void){
   	float km,lts;
   	printf("\n\t******** Exercicio 8 ********\n");	
   	printf("Qual o numero de quilometros que percorreu?\n");
   	scanf("%f",&km);
   	printf("Qual o numero de litros que consumiu?\n");
   	scanf("%f",&lts);
   	printf("Consumo aos 100 Km = %f\n", consumo(km,lts));
   }
   ```

21. Implemente uma função que recebe um horário, através da Hora, dos Minutos e dos Segundos, e com estes dados calcule e retorne o tempo total em segundos.

   *Exemplo de uma sessão de uso do programa:*

   ```bash
   Qual a hora?
   > 10
   Qual o minuto?
   > 20
   Qual o segundo?
   > 35
   Total de segundos = 37235
   ```

   *Resolução:*

   ```C
   int calculaSegundos(int horas,int minutos, int segundos){
   	return horas*60*60+minutos*60+segundos;
   }
   void ex9 (void){
   	int horas,minutos,segundos;
   	printf("\n\t******** Exercicio 9 ********\n");	
   	printf("Qual a hora?\n");
   	scanf("%d",&horas);
   	printf("Qual o minuto?\n");
   	scanf("%d",&minutos);
   	printf("Qual o segundo?\n");
   	scanf("%d",&segundos);
   	printf("Total de segundos = %d",calculaSegundos(horas,minutos,segundos));
   }
   ```

   

22. Implemente um programa que peça ao utilizador para introduzir dois números inteiros (a e b) e, de seguida, apresente no ecrã o resultado das seguintes operações aritméticas:

   - a+b

   - a-b (assim com b-a)

   - a*b

   - a/b (assim como b/a)
   
     

   *Notas:* 

- Deve ter em conta que o operador de divisão, quando aplicado a dois números inteiros, descarta a parte fracionária do resultado. Neste exercício, se o utilizador introduzir o valor 1 para o primeiro número e o valor 2 para o segundo número, o programa deve apresentar o valor 0.5 como resultado de a / b.

- 
  Deve ter em atenção situações de erro possíveis. Por exemplo, quando o utilizador introduzir 50 para o primeiro número e o valor 0 para o segundo número, não deve ser executada a operação a/b .

- Deve ter em atenção situações de erro possíveis. Por exemplo, quando o utilizador introduzir o valor 50 para o primeiro número e o valor 0 para o segundo número, não deve ser executada a operação a/b (pois seria 50/0.

  *Resolução:*

  ```C
  void ex10 (void){
  	int a,b;
	printf("\n\t******** Exercicio 10 ********\n");	
  	printf("insira dois numeros inteiros separados por espaco ' '\n");
  	scanf("%d %d", &a, &b);
  	printf("a+b = %d\n",a+b);
  	printf("a-b = %d\n",a-b);
  	printf("b-a = %d\n",b-a);
  	printf("a*b = %d\n",a*b);
  	if(b){
  		printf("a/b = %f\n",(float)a/b);
  	}
  	if(a){
  		printf("b/a = %f\n",(float)b/a);
  	}
  }
  ```
  

 

23. Considere o seguinte programa em C:

    ```C
    # include <stdio.h>
    int main (void)
    {
    	char alpha = (char) 0xF0;
    	unsigned int clr = 0xBF3F3FF0 ;
    	unsigned char beta;
    	unsigned char gr = (clr >> 16) & (0x000000FF);
    	beta = alpha >> 4;
    	return 0;
    }
    ```

    - Calcule, manualmente e sem compilar o código, o valor das variáveis `alpha`, `beta`, `clr` e `gr`.
    - A variável beta é um número negativo ou positivo?
    - Compile o código e verifique se o resultado foi o esperado. Caso não seja, identifique o erro e volte a fazer a primeira alínea.

  *Resolução:*
  
   Para calcular o valor de gr podemos converter para binário, ou podemos trabalhar directamente em hexadecimal já que a primeira operação é um *shift right* de 16 bits ou seja 24 dígitos hexadecimais.
   `clr >> 16 = 0x0000BF3F` 
  Em binário entram 16 zeros à esquerda (porque o número é sem sinal), e os 16 bits mais à direita perdem-se.
  Em seguida aplica-se a operação AND bit-a-bit:
   ```
       0x0000BF3F
    &  0x000000FF
   -----------------
       0x0000003F
   ``` 
   Logo, `gr = 0x0000003F`

   O calculo do `alpha` embora pareça mais simples tem um pormenor importate. `alpha` é do tipo `char` e portanto é um número com sinal (está em notação complemento para 2). Esse número pode ser positivo ou negativo dependendo do bit mais significativo. Se o número mais significativo (mais à esquerda) for `1`, o número é negativo. Se for `0`, o número é positivo. Portanto, neste caso `alpha` contém um número negativo porque `alpha = '1111 0000' b`. Quando um número é negativo, um shift para a direita introduz um `1` à esquerda em vez de `0`. E portanto `alpha >> 4 = '1111 1111' b = 0xFF = -1`.
   Note que se o número fosse positivo ou sem sinal (`unsigned`) entrariam zeros à esquerda. Note também que uma deslocação para a direita é uma divisão por 2. Se o número é negativo e for dividido por 2, tem de continuar a ser negativo. Se entrassem zeros, o número passaria a positivo e portanto estaria errado.
   
   
   
*Função main que chama todas as funções definidas:*

   ```c
#include <stdio.h>

void ex1 (void);
void ex2 (void);
void ex3 (void);
void ex4 (void);
void ex5 (void);
void ex6 (void);
void ex7 (void);
void ex8 (void);
void ex9 (void);
void ex10 (void);
void ex11 (void);
void ex12 (void);
void ex13 (void);
void ex14 (void);

int main (void)
{
	ex1();
	ex2();
	ex3();
	ex4();
	ex5();
	ex6();
	ex7();
	ex8();
	ex9();
	ex10();
	ex11();
	ex12();
	ex13();
	ex14();
	return 0;
}

