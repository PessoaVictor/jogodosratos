# Ratos do Bueiro

Jogo 3D de fuga pelos esgotos, feito para o navegador. Você controla um ratinho que precisa encontrar a família perdida pelos túneis, escapar dos humanos com lanternas e chinelos e levar todo mundo até o cano de saída antes da enchente.

> **Status:** em fase de testes. Equilíbrio de dificuldade e visual ainda estão sendo ajustados.

## Como jogar

| Ação | Teclado | Celular |
| --- | --- | --- |
| Mover | Setas ou WASD | Deslizar na tela ou direcional |
| Pular | Espaço | Botão **Pular** |
| Pausar | P ou Esc | Botão de pausa |

- **Reúna a família:** encoste nos ratinhos perdidos e eles seguem você em fila. No escuro, os olhinhos brilham.
- **Mais ratos, mais moedas:** cada moeda vale 1 + o número de ratos que estão com você.
- **Fuja da lanterna:** se a luz pegar você, o humano corre atrás.
- **Cuidado com a chinelada:** de perto, o humano bate com o chinelo. Saia do círculo vermelho ou pule.
- **Pule obstáculos:** muretas, canos caídos e buracos só passam pulando.
- **Cola-rato:** deixa você lento por pouco mais de um segundo. Dá para pular por cima.
- **Capa de herói:** aparece de vez em quando e deixa você voar por 6 segundos sem ser pego.
- **Bueiros:** as grades com luz da rua levam você para outro ponto do esgoto.

Ao terminar cada fase aparece um **código de 5 letras**. Digite esse código na tela inicial para voltar direto àquela fase. Cada fase tem sempre o mesmo labirinto.

Entre as fases, a **Oficina do Bueiro** vende melhorias: velocidade, visão no escuro, mais tempo antes da enchente e vidas extras.

## Rodando localmente

É um único arquivo HTML, sem etapa de build. Abra `index.html` no navegador.

Para evitar restrições de alguns navegadores com arquivos locais, você também pode servir a pasta:

```bash
python3 -m http.server 8000
# depois abra http://localhost:8000
```

## Publicando no GitHub Pages

1. No repositório, abra **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)` e salve.
4. Em alguns minutos o jogo fica disponível em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

## Tecnologia

- [Three.js](https://threejs.org/) r128 para a cena 3D, carregado via CDN.
- Texturas de tijolo, concreto e água geradas em tempo real com Canvas, sem arquivos de imagem.
- Sons sintetizados com Web Audio API.
- Progresso e recorde salvos no `localStorage` do navegador.
