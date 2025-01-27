# Bubble and Quick

Este trabalho da faculdade tem como objetivo comparar os métodos de ordenação **Bubblesort** e **Quicksort**.

### Contexto
O cenário envolve um restaurante britânico que precisa ordenar os pratos do cardápio de acordo com certos critérios.

## Desafios
O método escolhido pelo restaurante precisa ser capaz de ordenar até **300.000 pratos**. Por isso, é importante utilizar o método mais eficiente.
  
## Detalhes
- A ordenação deve ser feita com base na **prioridade** e no **tempo de preparo** de cada prato.
- Não há pratos com a mesma prioridade ou tempo de preparo, portanto, não há necessidade de lidar com empates.
- O nome de cada prato deve ter **no máximo 50 caracteres**, sem espaços.

## Relatório
- O relatório precisa comparar a eficiência dos dois métodos e explicar a escolha dos pivôs no Quicksort.

## Considerações sobre o código
### A atividade propõe que seja criada uma lista de 300.000 pratos para ser ordenada com os métodos.
Para isso, a função gerarNomePrato foi criada para combinar um adjetivo e um prato e assim, ter nomes aleatórios de pratos.

### Sobre os métodos, ambos são capazes de ordenar, porém a eficiência é diferente.
Como exemplo, ao executar o código com NUM_PRATOS 30000, o tempo de execução do QuickSort é de 0,007838 segundos e do BubbleSort é de 2,788537 segundos.
Diminuindo para 100 o NUM_PRATOS, o tempo de execução já é muito mais próximo: QuickSort - 0,000029 segundos e BubbleSort - 0,000025 segundos.
Ou seja, quanto maior a lista, maior a eficiência do Quicksort.

### Sobre a escolha dos pivôs no Quicksort
O código criado utiliza uma abordagem de pivô central para particionar o array. É a média entre os índices esquerdo e direito do array (ou da parte dele) que está sendo analisado.
O desempenho é ruim se o array já estiver ordenado, e nesse caso pode ter um desempenho similar ao BubbleSort. Como a lista não vai estar ordenada, não é um problema aparente.
Um ponto positivo é que o pivô central traz uma divisão balanceada do array.
Comparando com o pivô aleatório, o código com pivô central teve tempo de execução um pouco melhor.
