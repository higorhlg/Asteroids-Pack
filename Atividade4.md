# Atividade3

<h3>Spawn de Meteoros</h3>
Faça com que ao começar o jogo sejam criados uma certa quantidade de meteoros em posições aleatórias da cena.

<h2> Dicas </h2>

Crie um script responsável pelo spawn de objetos, um exemplo de nome seria "ControladorSpawn" ou "SpawnController" em inglês. Nesse script deverá ser feito toda a lógica de spawn de meteoro.

1 - Utilize valores aleatórios para as posições x e y. Exemplo:

`float x  = Random.Range(-limiteX, limiteX); //limiteX é o valor limite para a posição no eixo X para criação do meteoro.`

2 - Com os valores de x e y, crie um novo Vector3 com essas posições. Exemplo:

`Vector3 pos = new Vector3(x, y, 0);`

3 - Instancie o prefab do meteoro com a posição definida e com a rotação original do prefab:

`Instantiate(meteoroPrefab, pos, meteoroPrefab.transform.rotation);`

4 - Utilize um laço de repetição (for, while...) para criar a quantidade definida de meteoros. Exemplo:
int contador = 0;

```
for(contador = 0; i < quantidadeDeMeteoros; i++){
  //lógica de spawn
}
```

