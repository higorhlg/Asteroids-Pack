# Atividade 2

Defina em um script os estados do jogo:

<ul>
    <li> INGAME (Em jogo) </li>
    <li> PAUSED (Pausado) </li>
    <li> GAMEOVER (Fim de Jogo) </li>
</ul>

<h3> Estado de jogo (INGAME) </h3>

Para o estado INGAME o jogo deverá ter o tempo fluindo naturalmente (Time.timeScale = 1). 

<h3> Estado de Pausa (PAUSED) </h3>

Para o estado PAUSED, o jogo deverá ser congelado (Time.timeScale = 0) e deverá existir na interface do usuário (UI) alguma forma de resumir o jogo (voltar para o estado INGAME).

<h3> Estado de Game Over </h3>

Para esse estado GAMEOVER, além do tempo ser congelado, é obrigatório exibir uma tela que:
<ul>
    <li> Indique a quantidade total de pontos do jogador </li>
    <li> Possua um botão para recomeçar o jogo </li>
    <li> Possua um botão para voltar ao menu do jogo </li>
</ul>

<h2> Dicas </h2>

Para definir estados é sugerida a utilização de <b>enum</b>:

Enumerações ou <b>enum</b>, são utilizados para que possamos definir um novo tipo de dado que podem assumir apenas os valores que forem definidos em sua criação.
Um exemplo:

enum DIAS {
  DOMINGO,
  SEGUNDA,
  TERCA,
  QUARTA,
  QUINTA,
  SEXTA,
  SABADO,
}

Com essa sintaxe eu defino um novo <b> tipo </b> de variável, chamado de DIAS, e os valores que as variáveis desse tipo podem guardar são exclusivamente: DOMINGO,SEGUNDA,TERCA,...,SÁBADO.


<h4> Posso então criar a seguinte variável: </h4>

DIAS diaAtual;

<h4> E fazer a seguinte atribuição de valor </h4>

diaAtual = DIAS.DOMINGO;  

OBS: NOTE QUE PARA ACESSAR UM VALOR DO TIPO "DIAS" EU DEVO USAR A SINTAXE "DIAS.VALORDESEJADO"

<h4> E fazer as seguintes verificações: </h4>

if(diaAtual == DIAS.DOMINGO){ <br>
  //Faça alguma coisa <br>
}<br>
else if (diaAtual == DIAS.SEGUNDA){<br>
  //Faça outra coisa<br>
}<br>
...<br>
else if (diaAtual == DIAS.SABADO){<br>
  //Faça alguma coisa<br>
}<br>
