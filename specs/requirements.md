# Requisitos: Chuva de Bugs

## Introdução
Este projeto é um jogo de navegador em que o jogador controla um dev para coletar cafés e evitar bugs que caem do céu. Ele foi pensado para ser simples, rápido de jogar e fácil de entender em poucos segundos.

## Glossário
- **Dev**: personagem controlado pelo jogador, posicionado na parte inferior da tela.
- **Café**: item que vale 1 ponto quando coletado.
- **Bug**: item que causa perda de 1 vida ao encostar no dev.
- **Tela de jogo**: estado visual em que a partida está ativa e o jogador vê pontuação e vidas.
- **Recorde**: maior pontuação salva no navegador para a sessão do usuário.

## Requisitos

### Requisito 1: Tela inicial e início de partida
**História de usuário:** Como jogador, quero começar uma partida com um único comando, para iniciar rapidamente a experiência.

**Critérios de aceitação**
- **1.1** QUANDO a página for carregada, O SISTEMA DEVE exibir a tela de início com o nome do jogo e a instrução "pressione Espaço para começar".
- **1.2** QUANDO o jogador pressionar a tecla Espaço na tela de início, O SISTEMA DEVE iniciar a partida e trocar para a tela de jogo.
- **1.3** ENQUANTO a partida estiver iniciada, O SISTEMA DEVE ocultar a tela de início e mostrar somente as informações da partida em andamento.

### Requisito 2: Movimento do dev
**História de usuário:** Como jogador, quero mover meu dev para os lados, para capturar itens e evitar obstáculos.

**Critérios de aceitação**
- **2.1** QUANDO o jogador pressionar a tecla esquerda ou a tecla A, O SISTEMA DEVE mover o dev para a esquerda.
- **2.2** QUANDO o jogador pressionar a tecla direita ou a tecla D, O SISTEMA DEVE mover o dev para a direita.
- **2.3** ENQUANTO nenhuma tecla de movimento estiver pressionada, O SISTEMA DEVE manter o dev parado na posição atual.
- **2.4** ENQUANTO o dev estiver na área jogável, O SISTEMA DEVE impedir que ele saia dos limites da tela.

### Requisito 3: Geração e queda dos itens
**História de usuário:** Como jogador, quero ver itens caindo em posições aleatórias, para manter o jogo desafiador e dinâmico.

**Critérios de aceitação**
- **3.1** QUANDO a partida iniciar, O SISTEMA DEVE gerar itens do topo da tela em posições aleatórias ao longo da área jogável.
- **3.2** QUANDO um item for gerado, O SISTEMA DEVE fazê-lo cair verticalmente em direção ao chão da tela.
- **3.3** QUANDO um item alcançar a parte inferior da tela, O SISTEMA DEVE removê-lo da partida sem adicionar pontuação nem vida.
- **3.4** ENQUANTO a partida estiver ativa, O SISTEMA DEVE aumentar a frequência e a velocidade de queda dos itens com o passar do tempo.

### Requisito 4: Coleta de cafés e contato com bugs
**História de usuário:** Como jogador, quero pegar cafés e evitar bugs, para ganhar pontos sem perder vidas.

**Critérios de aceitação**
- **4.1** QUANDO o dev colidir com um item do tipo café, O SISTEMA DEVE aumentar a pontuação em 1 ponto e remover o item da tela.
- **4.2** QUANDO o dev colidir com um item do tipo bug, O SISTEMA DEVE remover o item da tela e reduzir a vida em 1 unidade.
- **4.3** QUANDO o jogador perder uma vida, O SISTEMA DEVE atualizar a informação visual de vidas na tela.
- **4.4** SE o jogador colidir com um item que já foi removido, ENTÃO O SISTEMA DEVE ignorar esse contato sem alterar pontuação ou vidas.

### Requisito 5: Estado do jogo, pontuação e vidas
**História de usuário:** Como jogador, quero ver meu progresso em tempo real, para saber se estou indo bem e quando preciso reagir.

**Critérios de aceitação**
- **5.1** QUANDO a partida estiver ativa, O SISTEMA DEVE mostrar a pontuação atual e as vidas restantes no topo da tela.
- **5.2** QUANDO a pontuação mudar, O SISTEMA DEVE atualizar a exibição imediatamente na tela.
- **5.3** QUANDO o jogador começar, O SISTEMA DEVE atribuir 3 vidas iniciais.
- **5.4** SE a quantidade de vidas chegar a zero, ENTÃO O SISTEMA DEVE encerrar a partida e apresentar a tela de fim de jogo.

### Requisito 6: Fim de jogo e recorde
**História de usuário:** Como jogador, quero ver o resultado final e tentar superar meu melhor desempenho, para continuar jogando e melhorando.

**Critérios de aceitação**
- **6.1** QUANDO a partida terminar por falta de vidas, O SISTEMA DEVE exibir a tela de fim de jogo com a pontuação final.
- **6.2** QUANDO a tela de fim de jogo aparecer, O SISTEMA DEVE exibir o recorde salvo no navegador.
- **6.3** QUANDO o usuário pressionar a tecla Espaço na tela de fim de jogo, O SISTEMA DEVE reiniciar a partida do zero.
- **6.4** ENQUANTO o navegador estiver aberto, O SISTEMA DEVE manter o recorde salvo mesmo após o fechamento e reabertura da página.

## Fora do escopo
- Som, música e efeitos de áudio.
- Multiplayer ou partidas em rede.
- Login, autenticação e perfil de usuário.
- Ranking online ou compartilhamento de pontuação.
- Níveis, fases ou modos de dificuldade diferentes.

## Suposições
- A partida reinicia a partir do estado inicial quando o jogador pressiona Espaço na tela de fim de jogo.
- O recorde é salvo no navegador com armazenamento local do próprio site, sem servidor externo.
- Os itens são limitados a dois tipos: café para pontuar e bug para perder vida.
