Music Player Pro
Player e buscador de músicas em HTML, CSS e JavaScript puro (vanilla), consumindo a API pública do iTunes.
Stack

HTML5 — estrutura semântica simples (input de busca, grids de resultados e favoritos)
CSS3 — sem frameworks, só CSS puro
JavaScript (ES6+) — sem bibliotecas, fetch nativo

Funcionalidades

Busca em tempo real na API do iTunes (itunes.apple.com/search), com debounce de 600ms no input para evitar excesso de requisições
Cards com flip 3D (transform: rotateY, perspective, backface-visibility) — frente mostra a capa do álbum, verso mostra player de áudio e botão de favoritar
Player de áudio único ativo por vez — ao tocar uma prévia, os event listeners de play/pause pausam automaticamente os demais áudios da grid
Sistema de favoritos persistente via localStorage, com serialização em JSON e sincronização entre a grid de busca e a seção de favoritos
Design responsivo com CSS Grid (auto-fill, minmax) e breakpoint para mobile
Efeitos visuais: fundo com blur/glassmorphism (backdrop-filter), animação de entrada dos cards (@keyframes fadeIn), sombras e transições suaves

Detalhes técnicos

async/await + try/catch para as chamadas à API
Manipulação de DOM via template strings (geração dinâmica dos cards)
Delegação de eventos (play/pause capturados na fase de capture, true no addEventListener) para funcionar com áudios criados dinamicamente
