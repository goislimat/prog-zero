# Anotações da aula

## introdução

O objetivo do curso é ensinar vocês a pensarem como programadores. As técnicas aqui apresentadas não terão nada de extremamente avançadas, mas ensinarão vocês a ótica de resolvedor de problemas que um programador possui.

O conteúdo será passado da maneira mais breve o possível, mas como ninguém aprende a nadar vendo vídeo de gente nadando, ninguém aprende a programar estudando apenas teoria. Então o curso é muita mão na massa e bem focado em vocês. Vai ter exercícios, sim. Vão haver exercícios simples. Vão haver exercícios que vão demandar entendimento do problema antes de começarem a "codar". E eu espero que vocês trabalhem em grupo sempre que necessário.

### terminologias fundamentais

**Qual o papel do computador?**
O computador é a máquina que tem a capacidade de realizar cálculos extremamente complexos, mas ele é incapaz de operar se não houverem instruções informando-o o que deve ser feito.

**O que é algoritmo?**
Algoritmo é o como resolver um problema. É a ideia, o passo-a-passo, a receita que você tem para que um problema passe ao estado de resolvido.

**O que é código?**
Código é a maneira que você tem para passar para o computador o algoritmo que você bolou para resolver um determinado problema.

**O que é compilador?**
Compilador é o carinha que pega aquilo que você escreveu em uma linguagem legível para seres humanos e converte em linguagem de computador. Ele transforma:
_Acesso_ em _01000001 01100011 01100101 01110011 01110011 01101111_

### estrutura básica

Todo programa em C começa a partir da seguinte estrutura básica:

```c
/*
  Isso é um comentário.
  Todo código colocado dentro desse bloco não é executado pelo compilador.
  Dessa maneira, você pode escrever várias linhas de comentário no seu código
  que podem te ajudar como anotações para futuras revisões.
*/

// Isso também é um comentário, mas ele comenta apenas uma linha

// Inclui funções que permitem trabalhar com a entrada e saída de dados. Geralmente, teclado e monitor.
#include<stdio.h>

// TODAS as execuções de programas em C começam a partir dessa função
int main() {
  // TODO: seu código vem aqui

  // Quando o programa encerrar sua execução, ele vai retornar o valor 0. Isso é apenas um padrão geral.
  return 0;
}
```

Retirando os comentários:

```c
#include<stdio.h>

int main() {
  // TODO: seu código vem aqui

  return 0;
}
```

### variáveis

Imagine que você quer programar uma calculadora que some dois números quaisquer, essa calculadora deve ser capaz de somar _1 + 1_, mas também _5 + 86_ ou _24 + 69_, ... Como não dá para predizer quais serão os valores que serão somados, dizemos que esses valores são _variáveis_.

Variáveis em C são de tipagem forte. Isso quer dizer que para cada variável que você cria, você deve saber de antemão que tipo de valor você quer inserir naquela variável. Os tipos de variáveis existentes em C são: **char**, **int** e **float** (principais). Mas também temos **double**, **void**, **unsigned char**, **long int**, **unsigned int**, **unsigned long int**, **short int**, **unsigned short int**.

Para o nosso exemplo da calculadora poderíamos fazer:

```c
int a;
int b;
```

### operações com valores

Linguagens de programação nos permitem operar valores matematicamente como uma de suas operações mais básicas. Em C temos: **+**, **-**, **\***, **/** e **%**. Exemplos:

```c
6 + 2; // 8
6 - 2; // 4
6 * 2; // 12
6 / 2; // 3
6 % 2; // 0
```

### entrada e saída de dados

Algumas seções atrás, vimos a inclusão de uma biblioteca com o `include<stdio.h>` que permite operar em cima da entrada e saída do computador. As funções fornecidas por essa biblioteca são: **printf** (para mostrar dados, ou seja. saída) e **scanf** (para coletar dados, ou seja, entrada).

Operações com printf:

```c
printf("Olá mundo!"); // Mostra 'Olá mundo!' na tela
printf("Tenho 20 anos"); // Mostra 'Tenho 20 anos' na tela
printf("Tenho %d anos", 20); // Mostra 'Tenho 20 anos' na tela
```

Operações com scanf:

```c
int i;

/*
  Quando o programa chega nesse ponto do código, ele espera que o usuário insira um número,
  e esse número é guardado na memória dentro da variável i.
  Nesse caso, o & (e comercial) é muito importante, pois ele diz ao C que é para guardar esse
  valor na memória.
*/
scanf("%d", &i);
```

A lista de codificação para que você consiga ler e apresentar variáveis na tela é:

- **%d** para inteiros
- **%f** para floats
- **%c** para chars

### exemplo de um programa completo em C

```c
#include<stdio.h>

int main() {
  float salario;
  int percentualEconomia;
  float valorEconomizar;

  printf("Salário: ");
  scanf("%f", &salario);

  printf("\nPercentual a salvar por mês (sem %): ");
  scanf("%i", &percentualEconomia);

  valorEconomizar = salario * percentualEconomia / 100;

  printf("\nValor a ser economizado: R$ %.2f", valorEconomizar);

  return 0;
}
```

O que esse programa faz?
