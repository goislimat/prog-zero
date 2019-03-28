# #1

```c
#include<stdio.h>

int main() {
  char letra;
  int idade;
  float altura;

  printf("Primeira letra do seu nome: ");
  scanf("%c", &letra);

  printf("Idade: ");
  scanf("%d", &idade);

  printf("Altura: ");
  scanf("%f", &altura);

  printf("%c -> %d anos -> %.2f m", letra, idade, altura);

  return 0;
}
```

# #2

```c
#include<stdio.h>

int main() {
  int tempo;

  printf("Tempo em anos: ");
  scanf("%d", &tempo);

  printf("%d anos equivale a %d dias.", tempo, tempo * 365);

  return 0;
}
```

# #3

```c
#include<stdio.h>

int main() {
  float vm;

  printf("Velocidade média em km/h: ");
  scanf("%f", &vm);

  printf("%.2f km/h equivalem a %.2f m/s.", vm, vm/3.6);

  return 0;
}

```

# #4

```c
#include<stdio.h>

int main() {
  // peso = massa * gravidade => massa = peso / gravidade

  float peso = 80;
  float gravidadeTerra = 9.8;
  float massa = peso / gravidadeTerra;

  float gravidadeLua = 1.62;
  float gravidadeMarte = 3.71;

  printf("Um corpo de %.2f kg na terra pesa %.2f na lua\n", peso, massa * gravidadeLua);
  printf("Um corpo de %.2f kg na terra pesa %.2f em marte", peso, massa * gravidadeMarte);

  return 0;
}
```

# #5

```c
#include<stdio.h>

int main() {
  // peso = massa * gravidade => massa = peso / gravidade

  float peso;
  float gravidadeTerra = 9.8;

  float gravidadeLua = 1.62;
  float gravidadeMarte = 3.71;

  printf("Entre com o peso do corpo na lua: ");
  scanf("%f", &peso);

  float massa = peso / gravidadeLua;

  printf("Um corpo de %.2f kg na lua pesa %.2f na terra\n", peso, massa * gravidadeTerra);
  printf("Um corpo de %.2f kg na lua pesa %.2f em marte", peso, massa * gravidadeMarte);

  return 0;
}
```

# #6

```c
#include<stdio.h>

int main() {
  // fc = m * (v * v) / r

  float massa;
  float velocidade;
  float raio;

  printf("Massa (em kg): ");
  scanf("%f", &massa);
  printf("Velocidade (em m/s): ");
  scanf("%f", &velocidade);
  printf("Raio (em m): ");
  scanf("%f", &raio);

  printf("A força centrípeta é %.2f N", massa * (velocidade * velocidade) / raio);

  return 0;
}
```
