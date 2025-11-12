# react_tic_tac_toe

Jogo da Velha (Tic Tac Toe) feito com HTML, CSS e React (via CDN), em um único arquivo `index.html`. Ideal para apresentação acadêmica sem JSX.

## Pré-requisitos
- Navegador moderno (Chrome/Edge/Firefox).
- Opcional: Extensão Live Server (VS Code) para subir um servidor local.

## Como executar
- Opção 1: Dê duplo clique em `index.html` e abra no navegador.
- Opção 2 (recomendada): com Live Server, clique em "Go Live" na pasta do projeto.

## Funcionalidades
- Alternância de turnos X/O.
- Detecção de vencedor e de empate.
- Botão "Reiniciar".
- UI com efeito de profundidade (sombras) e imagem de fundo customizável.

## Estrutura
- `index.html`: contém o CSS, o HTML (div `#root`) e o JavaScript com `React.createElement` (sem JSX).
- React e ReactDOM carregados via CDN (`unpkg.com`).

## Personalização
- Imagem de fundo: altere a URL/arquivo no seletor `body { background-image: ... }` em `index.html`.
- Estilos: ajuste as classes `.board`, `.square`, `.reset-btn` e `.title` no `<style>` do `index.html`.

## Observação sobre Create React App
Se preferir, o mesmo código pode ser colocado dentro de um projeto gerado por `npx create-react-app react_tic_tac_toe` usando o `public/index.html`. Para esta entrega, mantivemos tudo em um único arquivo conforme alinhado ao curso.

## Licença
  
---
  
# Sumário
- [Visão geral](#visão-geral)
- [Demonstração](#demonstração)
- [Funcionalidades](#funcionalidades)
- [Tecnologias](#tecnologias)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Como executar](#como-executar)
- [Personalização](#personalização)
- [Boas práticas adotadas](#boas-práticas-adotadas)
- [Próximos passos (opcionais)](#próximos-passos-opcionais)
- [Licença](#licença-1)
  
---
  
## Visão geral
Projeto acadêmico do Jogo da Velha feito com HTML, CSS e React 18 (via CDN), em um único arquivo `index.html` e sem JSX. A UI utiliza efeitos de profundidade (box-shadow), animações sutis e imagem de fundo com overlay para garantir legibilidade.
  
## Demonstração
- Execute localmente conforme a seção [Como executar](#como-executar).
- Sugestão: inclua um screenshot do jogo rodando para documentação.
  
## Funcionalidades
- Alternância de turnos X/O.
- Detecção de vencedor (todas as 8 combinações) e de empate.
- Exibição de status (vez do jogador, vencedor ou empate).
- Botão “Reiniciar”.
- Efeito de profundidade em tabuleiro, casas e botão.
- Imagem de fundo customizável.
  
## Tecnologias
- HTML5
- CSS3 (gradientes, sombras, responsividade simples)
- React 18 e ReactDOM 18 via CDN (`unpkg.com`)
- JavaScript moderno (hooks `useState`, imutabilidade com `slice()`)
  
## Estrutura do projeto
```
.
├── index.html   # CSS, div#root e JS com React.createElement (sem JSX)
├── README.md    # Documentação
└── LICENSE      # Creative Commons (CC BY 4.0)
```
  
No `index.html`:
- `<style>` contém estilos do tabuleiro, quadrados, botão e título.
- `<div id="root"></div>` é o ponto de montagem do React.
- CDNs do React/ReactDOM (modo desenvolvimento) antes do seu `<script>`.
- `<script>` final define `Square`, `Board`, `Game` com `React.createElement`.
  
## Como executar
- Opção 1 (simples): abra `index.html` com duplo clique no navegador.
- Opção 2 (recomendada): use Live Server (VS Code):
  1. Instale a extensão “Live Server”.
  2. Clique em “Go Live” na pasta do projeto.
  3. Acesse o endereço exibido (ex.: `http://127.0.0.1:5500`).
  
> Dica: usar um servidor local evita problemas de caminho/permite recarregar facilmente.
  
## Personalização
- Imagem de fundo: altere o caminho no CSS do `body` em `index.html`:
  ```css
  body {
    background-image:
      linear-gradient(rgba(0,0,0,0.35), rgba(0,0,0,0.35)),
      url('SEU_ARQUIVO.png');
  }
  ```
- Título: ajuste o `<h1 class="title">Jogo da Velha</h1>` no componente `Game`.
- Casas do tabuleiro: altere `.square { width, height, font-size }`.
- Paleta e sombras: ajuste `.board`, `.square`, `.reset-btn`, `.title`.
  
## Boas práticas adotadas
- Sem JSX: ideal para turmas que ainda não viram JSX.
- Estado imutável (cópia com `slice()` antes da alteração).
- Lógica de vitória isolada em `calculateWinner`.
- Sem dependências extras além de React/ReactDOM.
- Estrutura mínima e clara, fácil de revisar.
  
## Próximos passos (opcionais)
- Destacar a linha vencedora (estilizar os 3 quadrados vencedores).
- Histórico de jogadas (time travel).
- Testes automatizados.
- Migrar para Create React App mantendo a mesma lógica sem JSX (ou evoluir para JSX mais tarde).
  
## Licença
Este projeto está licenciado sob **Creative Commons Attribution 4.0 International (CC BY 4.0)**.
- Texto completo: https://creativecommons.org/licenses/by/4.0/legalcode
- Você é livre para compartilhar e adaptar, desde que dê o devido crédito.
