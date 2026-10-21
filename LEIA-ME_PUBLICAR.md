# Nanda Porto Beauty: como colocar no ar (prévia para a cliente)

Esta pasta é o site completo em HTML puro. Não precisa de instalação nem de build.

## 1) Subir no GitHub
1. Crie um repositório novo (pode ser privado), por exemplo `nanda-porto-site`.
2. Envie **o conteúdo desta pasta** (index.html, style.css, script.js, pastas img, fonts, links, etc.) para a raiz do repositório.

## 2) Publicar no Cloudflare Pages (gratuito, permite uso comercial)
1. Entre em dash.cloudflare.com, vá em *Workers & Pages*, clique em *Create* e escolha *Pages* e *Connect to Git*.
2. Escolha o repositório. Em *Framework preset* deixe **None**. *Build command*: vazio. *Build output directory*: `/` (ou deixe em branco).
3. Clique em *Save and Deploy*. Você recebe um endereço do tipo `nome-do-projeto.pages.dev`.
4. Mande esse endereço para a cliente. Cada alteração enviada ao GitHub publica sozinha.

(Os nomes dos botões do Cloudflare podem mudar um pouco. O caminho é sempre: Pages, conectar o Git, sem build.)

## 3) Enquanto for prévia
O site está marcado como **noindex** (o Google não lista). Isso está em 4 lugares:
- `<meta name="robots" content="noindex, nofollow">` em `index.html` e em `links/index.html`
- `robots.txt`
- bloco `X-Robots-Tag` em `_headers`

## 4) No lançamento (domínio da cliente)
1. Apague os 4 itens de noindex acima.
2. Antes de mexer no domínio, veja o que ele já usa hoje (e-mail, outro site). Só então conecte em *Custom domains* no Cloudflare Pages.
3. Troque os textos entre colchetes (nomes/notas dos produtos), as fotos "Adicionar foto aqui", e o link da Shopee e do Facebook.
4. **Fonte Brittany:** o arquivo veio como "uso pessoal". Para site de cliente em produção, compre a licença comercial.
