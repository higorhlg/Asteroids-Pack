# Atividade 1

Implemente as seguintes funcionalidades para o jogador:
<ul>
  <li> Rotação (direita e esquerda) com as teclas A e D</li>
  <li> Movimento (Impulsionar a nave para frente) com a tecla W </li>
  <li> Atirar com a tecla ESPAÇO ou CLIQUE ESQUERDO </li>
</ul>

<h2> Dicas: </h2>
<h3> 1º - Impulso para frente </h3> 
Para o efeito de impulso no espaço use o método <b>AddForce</b> presente nos componentes do tipo Rigidbody2D, informações e exemplos disponíveis <a href="https://docs.unity3d.com/ScriptReference/Rigidbody2D.AddForce.html">aqui</a>. 

<h4> Comentário sobre os exemplos da documentação: </h4>

No lugar de gameObject.AddComponent use apenas <b>GetComponent\<TipoDoComponente\>()</b> para pegar o componente Rigibody2D que já deverá estar presente no objeto do Player em cena.

O comando AddForce pode ser usado de duas formas: passando apenas a força que se deseja adicionar ao corpo, ou passando a força e o tipo de força a se aplicar, para esse momento usaremos apenas a primeira forma, um exemplo de como deve ser utilizado:

<b> corpo.AddForce(new Vector2(0,forca)) </b>

OBS: No lugar de new Vector2, podemos usar um Vector2 (conjunto de coordenadas 2D(x,y) já existente, um exemplo é o:

<b> transform.up </b>,

que representa a direção para cima do transform.

O valor de transform.up é um conjunto de coordenadas (Vector) que represente a direção pra cima do objeto, seu valor varia de acordo com a rotação do player, devido a mudança da direção cima do objeto com a sua rotação, caso o objeto não esteja rotacionado, o seu valor é (0,1). 

Ao usar o transform.up para direcionar a força aplicada ao objeto, esse valor pode ser multiplicado por um valor para controle da intensidade da força aplicada no objeto como por exemplo:

<b> corpo.AddForce(transform.up * forca) </b>

<h3> 2º - Atirar </h3>
Para poder atirar, crie a munição (laser) a ser disparado como objeto em cena, com o objeto pronto arraste-o para a pasta Prefabs para transformá-lo em um prefab (um prefab é um modelo pronto de um objeto que pode ser usado para criar tal objeto em cena). 

<b>O prefab da munição deverá ter um script que faça apenas com que a mesma se movimente para frente a cada quadro do jogo (Update).</b>

Com o prefab pronto, o script do player, ao detectar um CLIQUE ESQUERDO ou a tecla ESPAÇO deverá fazer a instanciação (criação) do objeto a partir do prefab criado, para isso deverá ser feito o uso do método Instantiate, informações e exemplos disponíveis <a href="https://docs.unity3d.com/ScriptReference/Object.Instantiate.html">aqui</a>. 

<h4> Observações sobre o Instantiate </h4>
O método Instantiate possui várias formas de utilização, a que devemos utilizar no momento é:

<b> Instantiate(prefab, posicao_para_instanciação, rotação_para_instanciação) </b>,

onde o prefab é uma variável do tipo GameObject que possui um prefab como valor (facilmente atribuído pelo editor), e
posição e rotação para instanciação são respectivamente a posição e a rotação que o prefab terá ao ser criado em cena.

<h3> ATIVIDADE EXTRA </h3>

Tente fazer com que a nave ao se movimentar (impulso para frente), reproduza uma animação com fogo saindo de sua traseira (turbina).
