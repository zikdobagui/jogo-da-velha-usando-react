# react_tic_tac_toe — Versão JSX

Esta é uma variação do projeto utilizando JSX diretamente no navegador, via Babel Standalone, para fins de estudo e comparação com a versão sem JSX.

## Arquivo principal
- `index_jsx.html`: contém os estilos, o `div#root`, as CDNs de React/ReactDOM, a CDN do Babel e o script com JSX.

## Como executar
- Abra o arquivo `index_jsx.html` no navegador (duplo clique) ou use o Live Server no VS Code.
- Requisitos:
  - Conexão com a internet (para baixar React/ReactDOM/Babel das CDNs `unpkg.com`).
  - Navegador moderno.

## Tecnologias
- React 18 e ReactDOM 18 (UMD) via CDN
- Babel Standalone (para transpilar JSX no browser)
- HTML e CSS iguais à versão sem JSX

## Estrutura (arquivo único)
```
index_jsx.html
├─ <style> ... CSS (board, square, reset-btn, title) ...
├─ <div id="root"></div>
├─ <script src="react.development.js"> (CDN)
├─ <script src="react-dom.development.js"> (CDN)
├─ <script src="babel.min.js"> (CDN)
└─ <script type="text/babel"> ... App em JSX ...
```

## Componentes (JSX)
- `Square`: renderiza um botão com o valor da casa e o `onClick`.
- `Board`: monta a grade 3x3 usando `map` (linhas e colunas) e usa `Square`.
- `Game`: controla o estado, calcula vencedor/empate, renderiza status, tabuleiro e botão "Reiniciar".

## Lógica (idêntica à versão sem JSX)
- `useState` mantém `squares` (array de 9 posições) e `xIsNext` (vez do jogador).
- `calculateWinner` checa todas as linhas/colunas/diagonais.
- `handleSquareClick` alterna entre 'X' e 'O', respeitando casas preenchidas e vitória.
- `handleReset` zera o tabuleiro.

## Observações importantes
- Babel no navegador é apenas para estudo/demonstração. Em produção, recomenda-se um build (ex.: Create React App, Vite, Next.js) que transpila JSX e otimiza o bundle.
- Ambos os modos (com e sem JSX) geram a mesma estrutura de elementos React; JSX é apenas uma forma mais concisa e legível de escrever `React.createElement`.

## Personalização
- A UI e o CSS são os mesmos da versão sem JSX. Edite o `<style>` no topo do `index_jsx.html`.
- A imagem de fundo aponta para o arquivo local já usado no projeto. Se renomear o arquivo, ajuste a URL no CSS do `body`.

## Licença
- A mesma licença do projeto principal se aplica a esta variação: **CC BY 4.0**.
