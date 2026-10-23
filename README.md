# Salas

Salas simples para compartilhar a tela direto entre navegadores (WebRTC, sem servidor próprio).
Visual inspirado no vidro líquido do iOS.

## Recursos
- Compartilhar a tela (computador), câmera e microfone
- Chat da sala e reações com emojis
- Convite por link (no celular abre o menu de compartilhar)
- Silenciar o áudio de cada tela recebida e ver em tela cheia
- Layout para celular, com tela que não apaga enquanto você está na sala

## Como usar
1. Abra o site, digite seu nome e um código de sala (ou clique em **Criar sala nova**).
2. Toque no código no topo para copiar o link e envie para quem vai entrar.
3. Clique em **Compartilhar tela**. Toque numa tela recebida para ver em tela cheia.

## Publicar no GitHub Pages
1. Crie um repositório público no GitHub.
2. Envie `index.html` e este `README.md` para a branch `main`.
3. Em **Settings → Pages**, escolha *Deploy from a branch*, branch `main`, pasta `/ (root)`.
4. Em cerca de um minuto o site fica em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

## Como funciona
- Usa a biblioteca [Trystero](https://github.com/dmotz/trystero) para as pessoas se encontrarem pelo código da sala (via relays públicos) e então trocarem vídeo diretamente.
- É uma malha P2P: cada pessoa se conecta a todas as outras. Funciona bem para grupos pequenos (até uns 6).
- Exige HTTPS (o GitHub Pages já fornece) e navegador de computador para compartilhar a tela.

## Celular
Navegadores de celular (Android e iPhone) não permitem compartilhar a tela pelo site. No celular dá para assistir às telas dos outros, usar chat, reações e microfone, e compartilhar a câmera.

## Limitações
- Sem servidor TURN, algumas redes muito restritas (corporativas, NAT rígido) não conseguem conectar.
- O código da sala é a única proteção: use códigos difíceis de adivinhar.
- A versão do Trystero está fixada em `index.html`; atualize ali se quiser uma mais nova.
