# Dicas para scripts

<h3> Encontrar objeto na cena através da tag </h3>
Em algumas situações pode ser necessário a busca de um objeto da cena por algum motivo, como por exemplo pegar um componente desse objeto.

Para encontrar um objeto na cena através de sua tag usamos o comando a seguir:

`GameObject.FindWithTag("tagdesejada")`

Com isso temos uma referência ao <b> primeiro </b> ojeto encontrado em cena com a tag desejada, poderíamos agora pegar algum de seus componenentes como o Rigidbody2D utilizando o `.GetComponent<ComponenteDesjado>()`:


`GameObject.FindWithTag("tagdesejada").GetComponent<Rigidbody2D>()`

Poderíamos ao invés do rigidbody, pegar um script presente no objeto por exemplo:

`GameObject.FindWithTag("tagdesejada").GetComponent<NomeDoScriptDesejado>()`


<h3> Gerar valor aleatório </h3>

Podemos utilizar a função `Random.Range(minValor, maxValor)` para gerar um valor entre `minValor` e `maxValor`.
Exemplo:

`Random.Range(0,100) // Gera um número aleatório entre 0 e 100` 
