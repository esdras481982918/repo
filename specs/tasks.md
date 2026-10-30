# Plano de implementação: Chuva de Bugs

> Como usar: rode `/4-implementar N` para cada tarefa, teste no navegador e faça commit.

- [ ] 1. Estruturar a tela e o loop principal
  - montar a estrutura HTML, o canvas e o texto inicial; criar o estado base e o `CONFIG`; iniciar o loop principal com `requestAnimationFrame`.
  - **Arquivos:** `index.html`, `style.css`, `src/config.js`, `src/main.js`
  - **Como verificar:** abrir a página no navegador → a tela central aparece com o nome do jogo e a instrução "pressione Espaço para começar"; o loop continua rodando sem travar a página.
  - _Requisitos: 1.1, 1.2, 1.3, 5.1_

- [ ] 2. Implementar movimento e vida inicial
  - mover o dev com as teclas de seta e A/D; impedir saída dos limites da tela; manter o dev parado quando não houver movimentação; inicializar o HUD com 3 vidas.
  - **Arquivos:** `src/main.js`, `src/game.js`, `src/render.js`
  - **Como verificar:** pressionar as teclas de movimento no navegador → o dev se desloca para os lados e não sai da área; ao iniciar a partida, o HUD mostra 3 vidas e pontuação zerada.
  - _Requisitos: 2.1, 2.2, 2.3, 2.4, 5.3_

- [ ] 3. Gerar itens, cair e colidir
  - gerar cafés e bugs do topo em posições aleatórias; aplicar gravidade e aumento de dificuldade com o tempo; remover itens que saem da tela; detectar colisões com o dev e aplicar pontuação ou dano.
  - **Arquivos:** `src/game.js`, `src/render.js`, `src/config.js`
  - **Como verificar:** aguardar alguns segundos → os itens aparecem e caem em velocidade crescente; coletar café → pontuação aumenta em 1; colidir com bug → vida diminui em 1; itens que chegam ao chão desaparecem sem efeito.
  - _Requisitos: 3.1, 3.2, 3.3, 3.4, 4.1, 4.2, 4.3, 4.4, 5.2, 5.4_

- [ ] 4. Finalizar partida, recorde e revisão
  - encerrar a partida ao zerar vidas; exibir tela de fim com pontuação final e recorde; salvar o melhor valor em armazenamento local; reiniciar a partida quando o jogador pressionar Espaço.
  - **Arquivos:** `src/game.js`, `src/render.js`, `src/main.js`
  - **Como verificar:** perder todas as vidas → aparece a tela de fim com a pontuação e o recorde; recarregar a página → o recorde permanece; apertar Espaço na tela final → a partida começa do zero.
  - _Requisitos: 6.1, 6.2, 6.3, 6.4_

## Correções

