# Atividade3

<h3> Faça com que o player não seja capaz de se movimentar, rotacionar ou atirar durante os estados PAUSE e GAMEOVER. </h3>

Para esse objetivo, faça uma condicional em todo código que só deve ser executado durante o estado INGAME. Exemplo:

```
if (estadoAtual == INGAME) {

  // Código a ser executado quando o estado for "INGAME", exemplo: Rotação do Player.
  
  .
  .
  . 
  
}
```

<h3> Crie os seguintes prefabs: </h3>

<ul>
    <li> Meteoro (Grande) </li>
    <li> Meteoro (Medio) </li>
    <li> Meteoro (Pequeno) </li>
</ul>

Para os meteoros, implemente os seguintes comportamentos:

<ul>
    <li> Os meteoros se movimentam pelo espaço </li>
    <li> Ao colidir com o player ou com o laser do player, o meteoro é destruído </li>
    <li> Ao ser destruído pelo player, o meteoro deve acrescentar pontos no placar do jogador</li>
</ul>

O player ao colidir com um meteoro deve ser destruído e reaparecer no meio da tela caso possua vidas extras.

<h2> Dicas </h2>

<h3> Acessar variável de outro script </h3>

Para acessar uma variável de outro script, crie uma variável para servir de referência ao script em que se encontra a variável desejada, o tipo dessa variável deve ser o nome do script alvo. Além disso, se certifique de que a variável desejada esteja definida como <b> pública </b> para que possa ser realizado o acesso externo.

Exemplo:
Suponhamos que existem 2 scripts: Script1 e Script2.

Script1 deseja acessar uma variável <b> x </b> que está definida da seguinte forma no script 2:

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

Para realizar esse acesso, deve-se criar uma variável no Script1 do tipo Script2:

```
.
.
.

public class Script1: MonoBehaviour{
  [SerializeField] //SerializeField para atribuir o valor do script pelo editor da unity
  Script2 script;
.
.
.
```

Com o valor atribuído corretamente a variável "script", temos acesso as variáveis e também aos métodos/funções públicas presentes no Script2, podendo acessar esses atributos através de um .(ponto) ao final da palavra "script", exemplo:

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

<h3> Valor Aleatório </h3>
Utilize a função <b>Random.Range(valorMínimo, valorMáximo)</b> para gerar um valor aleatório dentro da faixa especificada.

Exemplo:

```
Random.Range(0,100) gera um valor aleatório entre 0 e 100
```

Sugere-se a utilização de valores aleatórios para as direções x e y na movimentação do meteoro.




