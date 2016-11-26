1 - Dê um exemplo de um aplicativo que requer conteúdo algorítmico no nível do aplicativo e discuta a função dos algoritmos envolvidos. (Give an example of an application that requires algorithmic content at the application level, and discuss the function of the algorithms involved.)

  -Akinator é aplicação web que diz o que estava em nossa mente simplesmente fazendo perguntas. Usa árvores de decisão para chegar à conclusão.
  [Mais exemplos]

2 - Suponha que estamos comparando implementações de "insertion sort" e "merge sort" na mesma máquina. Para entradas de tamanho n, "insertion sort" é executado em 8n² passos, enquanto "merge sort" executa em (64n lg n) passos. Para que valores de n, "insertion sort" é mais rápido que "merge sort"? (Suppose we are comparing implementations of insertion sort and merge sort on the same machine. For inputs of size n, insertion sort runs in 8n² steps, while merge sort runs in (64n lg n) steps. For which values of n does insertion sort beat merge sort?)

  A resposta desse problema é a inequação 8n² < 64n*lg(n) (onde n é um inteiro positivo e lg é o logaritmo na base 2).
    8n² < 64n * lg(n)
    (1/(8n)) * 8n² < (1/(8n)) * 64n * lg(n)
    n < 8 * lg(n)
    n/8 < lg(n)
    2 ^ (n/8) < n

  A partir desse ponto, não podemos resolver a equação explicitamente, só com ajuda de métodos numéricos. Com uma calculadora, ou aplicativo que desenhe gráficos (wolfram alpha), podemos ver que os valores de N que são solução para o problema estão no intervalo : 2 <= n <= 43.

3 - (What is the smallest value of n such that an algorithm whose running time is 100n² runs faster than an algorithm whose running time is (2^n) on the same machine?)

  A resposta é o menor valor inteiro que é solução da equação 100n² < 2^n.
  Como na questão anterior, essa equação não pode ser resolvida algebricamente, então temos que encontrar valores por métodos numéricos. (onde a resposta pra esse caso vai ser n = 15).
