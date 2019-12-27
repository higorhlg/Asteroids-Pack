# Dicas para scripts

<h3> Acessar variável de outro script </h3>

Para acessar uma variável de outro script, crie uma variável para servir de referência ao script em que se encontra a variável desejada, o tipo dessa variável deve ser o nome do script alvo. Além disso, se certifique de que a variável desejada esteja definida como <b> pública </b> para que possa ser realizado o acesso externo.

Exemplo:
Suponhamos que existem 2 scripts: Script1 e Script2. 

No Script1 você deseja acessar uma variável <b> x </b> que está presente no script 2:

```
.
.
.

public class Script2: MonoBehaviour{
  public int <b> x </b>;
.
.
.
```

Para realizar esse acesso, deve-se criar uma variável no Script1 do tipo <b>Script2</b>:

```
.
.
.

public class Script1: MonoBehaviour{
  //SerializeField para atribuir o valor do script pelo editor da unity (uma outra alternativa é explicada na próxima dica)
  [SerializeField] 
  Script2 script;
.
.
.
```

Com o valor atribuído corretamente a variável "script" (pelo inspector no objeto que está rodando o Script1), temos acesso as variáveis e também aos métodos/funções <b>públicas</b> presentes no Script2, podendo acessar esses atributos através de um .(ponto) ao final da palavra "script", exemplo:

```
public class Script1: MonoBehaviour{
  [SerializeField] //SerializeField para atribuir o valor do script pelo editor da unity
  Script2 script;
  
  void Start(){
    script.x = 100; // Atribui valor 100 a variável "x" do Script2 associado com a variável "script"
  }
.
.
.
```


<h3> Encontrar objeto na cena através da tag </h3>
Em algumas situações pode ser necessário a busca de um objeto da cena por algum motivo, como por exemplo pegar um componente desse objeto.

Para encontrar um objeto na cena através de sua tag usamos o comando a seguir:

`GameObject.FindWithTag("tagdesejada")`

Com isso temos uma referência ao <b> primeiro </b> ojeto encontrado em cena com a tag desejada, poderíamos agora pegar algum de seus componenentes como o Rigidbody2D utilizando o `.GetComponent<ComponenteDesjado>()`:


`GameObject.FindWithTag("tagdesejada").GetComponent<Rigidbody2D>()`

Poderíamos ao invés do rigidbody, pegar um script presente no objeto por exemplo:

`GameObject.FindWithTag("tagdesejada").GetComponent<NomeDoScriptDesejado>()`

Utilizando o exemplo anterior em que desejamos no "Script1" acessar uma variável "x" existente no "Script2", poderíamos fazer da seguinte forma no Script1:

```
public class Script1: MonoBehaviour{
  Script2 script;
  
  void Start(){
    //Encontrar o objeto com a tag desejada e pegar o seu componente do tipo "Script2":
    script = GameObject.FindWithTag("tagdesejada").GetComponent<Script2>(); 
    script.x = 100; // Atribui valor 100 a variável "x" do Script2 associado com a variável "script"
  }
.
.
.


<h3> Gerar valor aleatório </h3>

Podemos utilizar a função `Random.Range(minValor, maxValor)` para gerar um valor entre `minValor` e `maxValor`.
Exemplo:

`Random.Range(0,100) // Gera um número aleatório entre 0 e 100` 
