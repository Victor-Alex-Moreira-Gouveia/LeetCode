# Conhecimentos gerais

Aqui vai está o conhecimento básico para conseguir entender e fazer atividade de LeetCode.

**Pré-requisitos:**
- Entender a lógica de programação.
- Saber linguagem de programação python ou C.
- Ter paciência.
- Dedicação.
- Vontade de aprender.

**OBS:** Caso não consiga entender o conteúdo recomendo que tente obter informações de outras fontes, mas eu vou deixar nos titulos o nome de cada tema para facilitar a pesquisa.
___
## Big O notation

É uma anotação que serve para medir a eficiencia de um algoritmo pelo tempo ou espaço. É uma forma padronizada que permite avaliar de forma mais rápida e simples o quão bom é o código criado.

<img src="./BigOGrafico.png">

**Legenda:**
    - O > Tempo
    - n > Quantidade de entrada de dados

#### Exemplo prático O(1)
<br>

**Python**
```python
nome = "Victor Alex"
letra = nome[0] # Vai armazenar a primeira letra que nesse caso é 'V'
print(letra) # nesse caso o algoritmo é O(1)
```

<br>

**C**
```c
#include <stdio.h>

int main(){
    char nome[] = "Victor Alex";
    char letra = nome[0];
    printf("%c", letra);
    return 0;
}
```

<br>

#### Exemplo prático em python O(n)
<br>

**Python**
```python
numeros = [0, 15, 38, 84, 35]
for i in numeros: # O(n)
    print(i) # O(1)
```

<br>

**C**
```c
#include <stdio.h>
int main(){
    int numero[4] = {0, 15, 38, 84, 35};
    for (int i = 0; i < 5; i++){ // O(n)
        printf("%d° elemento: %d", i, numero[i]); // O(1)
    }
    return 0;
}
```

<br>

#### Exemplo prático em python O(log n)
<br>

**Python**
```python
def busca_binaria(lista, alvo):
    esquerda = 0
    direita = len(lista) - 1

    while esquerda <= direita:
        meio = (esquerda + direita) // 2
        if lista[meio] == alvo:
            return meio
        elif lista[meio] < alvo:
            esquerda = meio + 1
        else:
            direita = meio - 1
    return -1

# Exemplo de uso:
numeros = [2, 3, 5, 7, 11, 13, 17]
resultado = busca_binaria(numeros, 7)  # Nesse caso, o algoritmo é O(log n)
print(resultado)  # Retorna o índice do número 7 na lista, que é 3
```

<br>

**C**
> Descupe não tenho conhecimento o sufuciente para converter isso mas estou estudado e me esforçando para melhorar

<br>

#### Exemplo prático em python O(n²)
<br>

**Python**
```python
def encontrar_pares(lista):
    for i in range(len(lista)):  # O(n)
        for j in range(len(lista)):  # O(n)
            print(f"Par: ({lista[i]}, {lista[j]})")  # O(1)

# Exemplo de uso:
numeros = [1, 2, 3]
encontrar_pares(numeros)
```

<br>

**C**
> Descupe não tenho conhecimento o sufuciente para converter isso mas estou estudado e me esforçando para melhorar.

<br>
___

## Tipos de estrutura de dados
**Descrição:** São diferentes formas de se organizar os dados, e caso a forma de organização for correta isso pode proporcionar um bom desempenho. Lembrando que cada forma de organização foi feita para um cenario em especifico então escolha com cuidado se não pode ocasionar em uma grande dor de cabeça.

- Array => Conjunto de dados armazenado em formato de vetor ou matrix.
<br>
- Pilha => Dado organidado de forma que o primeiro dado que entrou e o ultimo a sair.
<br>
- Fila => Semelhante ao formato de atendimento o primeiro a entrar e o primeiro a sair.
<br>
- Árvore binaria e árvore binaria de busca => Usado para organizar dados não lineares.
<br>
- HashMap => Estrutura que guarda dado em formato chave e valor.