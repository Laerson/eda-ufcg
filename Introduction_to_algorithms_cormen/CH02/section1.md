1 - Using Figure 2.2 as a model, illustrate the operation of INSERTION-SORT on the array A = [31, 41, 59, 26, 41, 58].
  [adicionar a imagem da resposta]

2 - Rewrite the INSERTION-SORT procedure to sort into nonincreasing instead of nondecreasing order.
  Duas possibilidades de implementação:
    a) trocar a condição da linha 5 para "while *i* > 0 and A[*i*] < *key* (jogar os menores na frente)
    b) varrer a array de trás pra frente.

  Em pseudocódigo:
    a)
    ***for*** *j* <- 2 ***to*** *length*[A]
      ***do*** *key* <- A[*j*]
        *i* <- *j* - 1
        ***while*** *i* > 0 and A[*i*] < *key*
          ***do*** A[*i* + 1] <- A[*i*]
            *i* <- *i* - 1
          A[*i* + 1] <- *key*

    b)

3 - Consider the searching problem:

* **Input**: A sequence of n numbers A = [a1, a2, . . . , an] and a value v.
* **Output**: An index i such that v = A[i] or the special value NIL if v does not appear in A.


Write pseudocode for **linear search**, which scans through the sequence, looking for v. Using a loop invariant, prove that your algorithm is correct. Make sure that your loop invariant fulfills the three necessary properties.

  ***for*** *i* <- 1 ***to*** *length*[A]
    ***do if*** *v* = A[i]
      ***return*** *i*
    ***return*** *NIL*

  **Loop Invariant** : Para todo 0 < *j* < *i*, nenhum A[*j*] é igual a *v*.
  **Inicialização** : Quando *i = 1*, não existe nenhum A[*j*], logo o **Loop invariant** é verdadeiro.
  **Manutenção** : Se A[*i*] != *v*, na próxima iteração, o **Loop invariant** vai continuar verdadeiro.
  **finalização** : Se em alguma iteração A[*i*] = *v*, o loop termina, mantendo a propriedade verdadeira(e retornando o indice do elemento que não respeita a propriedade). Quando *i* = *length[A]* + 1, a gente sabe que A[1...*length*[A]] não tem nenhum elemento que seja igual a *v*, logo é retornado *NIL*.

4 - Consider the problem of adding two n-bit binary integers, stored in two n-element arrays A and B. The sum of the two integers should be stored in binary form in an (n + 1)-element array C. State the problem formally and write pseudocode for adding the two integers.


  n <- length[A]
  C = array[n + 1]
  carry <- 0
  for i <- 1 to n
    do C[i] <- (carry + A[i] + B[i])%2
      carry <- (carry + A[i] + B[i])/2
  C[n + 1] <- carry
  return C
