# Resumão massa

### Estrutura básica

```c
#include <stdio.h>

int main() {
  // código aqui

  return 0;
}
```

### Tipos de variáveis

```c
// char para armazenar caracteres únicos
char sim_ou_nao;
char primeira_letra;

// int para armazenar valores inteiros (sem fração)
int idade;
int gols;

// float para armazenar valores fracionados
float peso;
float distancia;
```

### Leitura de dados

```c
// Toda leitura é feita com scanf

// Toda leitura de caracteres é feita com %c (de char)
// É importante lembrar que toda vez que estivermos fazendo um scanf devemos usar o &
// para que consigamos colocar o valor no espaço de memória dedicado à essa variável
scanf("%c", &primeira_letra);

// Toda leitura de inteiros é feita com %d (de digit)
scanf("%d", &gols);

// Toda leitura de valores fracionados é feita com %f (de float)
scanf("%f", &distancia);

```

### Impressão de dados

```c
// Printfs mostram mensagem na tela (qualquer que seja ela)
// Essas mensagens podem ou não, conter variáveis

// Para imprimir caracteres, use %c e lembre-se de falar qual variável quer imprimir
printf("A primeira letra do meu nome é: %c", primeira_letra);

// Para imprimir inteiros, use %d e lembre-se de falar qual variável quer imprimir
printf("A minha idade é: %d", idade);

// Para imprimir números fracionados, use %f e lembre-se de falar qual variável quer imprimir
// Floats tem um tratamento especial
// Normalmente um float tem 6 casas depois da vírgula, caso queira limitar a quantidade de casas
// mostradas,
printf("A distância da minha casa para o trabalho é: %.3f", distancia);

// Imprimindo várias variáveis em um único trecho de printf
// Você coloca todo o texto que quer imprimir na tela e referencia todos os locais que tiverem variáveis
// Para esse exemplo podemos fazer o seguinte, escrevemos a frase "Letra T ===> Idade: 28 ====> Distância: 1.563 m"
// Jogamos isso no printf
// printf("Letra T ===> Idade: 28 ====> Distância: 1.563 m")
// substituímos variável a variável
// printf("Letra %c ===> Idade: 28 ====> Distância: 1.563 m", primeira_letra);
// printf("Letra %c ===> Idade: %d ====> Distância: 1.563 m", primeira_letra, idade);
// printf("Letra %c ===> Idade: %d ====> Distância: %.3f m", primeira_letra, idade, distancia);
printf("Letra %c ===> Idade: %d ====> Distância: %.3f m", primeira_letra, idade, distancia);
```

### Operações matemáticas

```c
9 + 5; // 14
9 - 5; // 4
9 * 5; // 45
9 / 5; // 1.8
9 % 5; // 4
```
