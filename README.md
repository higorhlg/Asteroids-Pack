# Asteroids-Pack
<p> Repositório criado para facilitar o acesso a recursos(assets) e informações para a atividade a ser realizada com a turma de Introdução ao desenvolvimento de jogos digitais. Os assets aqui disponíveis serão utilizados para a criação de um jogo similar ao clássico Asteroids. </p>

<p align="center">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/en/1/13/Asteroi1.png" />
</p>

<h1> Sobre o jogo </h1>

O objetivo é pontuar destruindo asteróides e naves inimigas enquanto se mantém vivo, obtendo pontos para cada asteróide destruido de acordo com o seu tamanho. Quando um asteróide é destruído, existe uma chance de aparecer uma das possíveis naves inimigas, que fornecem mais pontos do que asteróides ao serem destruídas. E quando todos os asteróides são destruídos, se inicia um novo level com mais asteróides.

# Menu Principal

Ao começar o jogo deve ser exibido um menu principal com as opções de começar o jogo e sair do mesmo. O menu deverá conter:
<ul>
  <li> Imagem de fundo </li>
  <li> "Asteroids" como título do menu </li>
  <li> Botão para começar o jogo </li>
  <li> Botão para ver ranking de pontuações </li>
  <li> Botão para sair do jogo </li>
</ul>


Devem ser utilizadas as imagens, botões e fontes disponíveis dentro da pasta de assets disponibilizadas.

Um exemplo de como poderia ficar o seu menu principal: 
<p align="center">
    <img src="https://i.ibb.co/BCttKhY/Screen-Shot-2019-10-21-at-13-18-31.png" />
</p>


# Interface do Usuário em jogo (UI)

A cena em que se passa o jogo deverá conter como elementos da interface do usuário:
<ul>
  <li> Indicação de pontuação atual </li>
  <li> Indicação da quantidade de vidas do player </li>
  <li> Botão de pause </li>
</ul>

Um exemplo de como poderia ficar a sua interface do usuário durante o jogo: 
<p align="center">
    <img src="https://i.ibb.co/yWPpPGC/Screen-Shot-2019-10-21-at-13-35-08.png" />
</p>


# Mecânicas do jogador (nave)
O jogador começa com 3 vidas e controla uma nave capaz de rotacionar, atirar e se movimentar para frente com o impulso da turbina da nave, a nave eventualmente para de se movimentar quando não está sendo impulsionada.
O jogador pode sair com a nave dos limites da tela e sair no lado oposto da tela.
Sendo assim o jogador deverá ser capaz de:
<ul>
  <li> Rotacionar para esquerda e direita</li>
  <li> Atirar </li>
  <li> Impulsionar para frente </li>
  <li> Sair da tela e reaparecer no lado oposto de onde saiu (Screen Wrap)</li>
</ul>

Ao impulsionar para frente, deverá ser reproduzida uma animação com a turbina da nave soltando fogo (disponível na pasta de assets disponibilizada).

# Estados do Jogo 
O jogo deverá ter estados, sendo eles:
<ul>
    <li> WAITGAME (Esperando) </li>
    <li> STARTGAME (Começando) </li>
    <li> INGAME (Em jogo) </li>
    <li> PAUSED (Pausado) </li>
    <li> GAMEOVER (Fim de Jogo) </li>
    <li> RESTART </li>
</ul>

Alguns estados deverão ter telas específicas,

<h2> Estado de Pausa (PAUSED) </h2>

Para o estado PAUSED, o jogo deverá ser congelado e deverá existir na interface do usuário (UI) alguma forma de resumir o jogo.

<h2> Estado de Game Over </h2>

Para esse estado GAMEOVER, é obrigatório existir uma tela que:
<ul>
    <li> Indique a quantidade total de pontos do jogador </li>
    <li> Possua um botão para recomeçar o jogo </li>
    <li> Possua um botão para voltar ao menu do jogo </li>
</ul
