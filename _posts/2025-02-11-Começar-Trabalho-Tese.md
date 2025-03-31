---

title: "Começar Trabalho Tese"
date : 2025-02-11 00:00:00 +0000
categories: [Darwin]
tags: [Darwin]

---

## Começar Trabalho de Tese

Seguindo o plano de trabalhos, o primeiro trabalho a fazer será detetar objetos para transportar.
Reconhecendo já as capacidades das câmaras, podemos passar diretamente para detetar objetos.

O Darwin-OP já possui num dos seus tutoriais um programa que nos permite detetar um objeto de uma cor à nossa escolha usando métodos clássicos de filtração de cores, permite-nos também saber as coordenadas do centróide desse mesmo objeto.
Usando isso, é possível fazer o mesmo seguir objetos dessa mesma cor tanto a andar como somente com a cabeça, o que também já nos é dispobilizado nos tutoriais.

Incluindo isso tudo, e sabendo as posições de todas as juntas do robô, será possível ter uma previsão da distância do objeto ao robô se assumirmos uma altura predeterminada para o objeto, como por exemplo o chão. Usando imagens sucessivas onde o robô movimente ligeiramente a cabeça mas consiga mantêr o objeto no seu ângulo de visão irá permitir determinar a posição do mesmo.

Usando isso, faltará criar os controlos para o robô conseguir pegar no objeto.

No entanto, para poder eventualmente aumentar a complexidade dos objetos ou ambientes nos quais o robô poderá funcionar, um simples filtro de cores não será suficiente. Para isso, e devido à capacidade computacional limitada do Darwin-OP, será necessário que as imagens sejam processadas num computador externo que depois enviará os comandos ao robô, assim ganhamos flexibilidade para as imagens também poderem vir de câmaras externas ao robô.

