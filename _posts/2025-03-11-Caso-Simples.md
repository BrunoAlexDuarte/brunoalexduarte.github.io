---

title: "Começar com Caso Simplificado"
date : 2025-03-11 00:00:00 +0000
categories: [Darwin]
tags: [Darwin]

---

## Começar com Caso Simplificado

Foi decidido que se iria simplificar o problema inicialmente e se iriam adicionando funcionalidades mais complexas à medida que as anteriores ficassem completas.
Com isso, a primeira tarefa seria a seguinte: usando uma câmara exterior ao Darwin-OP, obtém informação do mesmo, e envia o mesmo para a posição onde estará o objeto.

Para isso, foi necessário criar um programa de visão que detetasse a posição de ambos e calculasse os movimentos que o Darwin teria que fazer. 
Esses movimentos incluem rotação e translação.
Foram criadas funções que recebem um comando (Ir para a frente, rodar para a direita ou esquerda, e parar) e que chamam a framework Walking associada ao Darwin para que o mesmo possa fazer esses movimentos de forma segura, sem danificar a estrutura do mesmo. Inspiração para isso veio do exemplo que vem instalado no Darwin onde o mesmo tem que seguir uma bola.

Após ter uma maneira de controlar o Darwin a partir do meu computador de forma simples, criei o programa para detetar o alvo e o Darwin-OP, bem como os movimentos que o mesmo deveria executar.
Nesta fase o alvo é uma bola vermelha que se encontrará no chão, e o Darwin terá colado na cabeça uma fita adesiva de cor amarela e de cor verde para conseguir detetar a posição e a orientação do mesmo.

Com ambos esses dados será possível saber como devemos rodar ou fazer andar o Darwin-OP para que ele chegue perto do objeto usando uma câmara externa. No entanto a cor verde não é a mais indicada pois reflete demasiado a luz, e em algumas situações fica impossível de detetar, por isso será necessário testar cores mais resilientes à mudança de posição e orientação do robô.

## Usando câmara interna

Depois do primeiro caso estar feito, foi usado um método baseado no código de exemplo fornecido pela ROBOTIS onde o Darwin persegue uma bola para chutar a mesma. Este exemplo foi adaptado para em vez de procurar a bola no chão a procurar ligeiramente acima do mesmo, e para quando a encontrar e se deslocar até à mesma, quando estiver perto, levantar os braços em vez de a chutar.

Para esse efeito foi necessário atualizar um parâmetro que verifica se a inclinação da cabeça está adequada, bem como se a posição do píxel central na imagem é menor que um certo valor.
Após isso, o robô chega ao suporte, mas colide ligeiramente com o mesmo, demonstrando que necessita de um pouco mais de calibração.

