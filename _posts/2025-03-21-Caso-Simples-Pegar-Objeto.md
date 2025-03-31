---

title: "Acabar o caso simplificado e pegar no objeto individualmente"
date : 2025-03-31 00:00:00 +0000
categories: [Darwin]
tags: [Darwin]

---

## Finalizar caso simplificado

Após experimentação, desistiu-se da ideia de usar verde e amarelo na cabeça do Darwin para usar um triângulo isósceles com os lados iguais de tamanho superior à base para ser possível detetar mais facilmente a orientação e posição do Darwin. Este método é melhor pois não esgotamos as cores alvo que podemos querer utilizar para os objetos ou outros robôs. 

Problemas desta medida vem com as variações da liminusidate do ambiente, que podem afetar ligeiramente as partes do triângulo mais distintas e com isso detetar ângulos não tão precisos. Para mitigar essa situação foi feito com que se o ângulo medido for muito diferente do medido anteriormente, é ignorado, e repete isso até 3 vezes, à terceira vez assume que o ângulo inicial é que estava errado e corrige. Com este método o Darwin consegue inclinar-se na direção da bola com mais precisão.

No entanto problemas ocorreram ao calcular a distância entre a bola e o Darwin. Devido à possível variação do centróide do Darwin enquanto o mesmo caminha, o sistema poderia calcular uma distância muito superior à que aconteceria caso o mesmo estivesse parado. Com isso, creio que a melhor abordagem será usar a câmara externa para colocar o robô na direção do objeto, mas depois usar a câmara interna do mesmo para ele se aproximar do mesmo.

## Pegar no objeto

Já foram criados movimentos para o Darwin poder pegar nos objetos alvo (por enquanto barras de metal), no entanto há problemas devido à estabilidae do mesmo, que de vez em quando perde o balanço ao levantar os braços mesmo que devagar. Para resolver este problema poderá ser útil calcular o centro de massa do mesmo de modo a conseguir ter uma melhor estimativa de como deveremos ajustar a posição do robô para ele pegar no objeto em segurança. 

No entanto a abordagem que vem como exemplo do robô não tem dado resultados muito conclusivos (dá sempre o mesmo centro de massa independemente da posição), pelo que poderá ter de ser feito o cálculo do mesmo "à mão".

Alternativamente poderemos também ajustar a forma do Darwin andar de modo a acabar numa posição mais estável, usando o Walk Tuner que vem instalado no robô.

