# Empreenda Ideias

Site de **empreendaideias.com.br**, hospedado no GitHub Pages.

| Endereço | Arquivo |
|---|---|
| empreendaideias.com.br/bio | `bio/index.html` (página de links: Mentoria, YouTube, WhatsApp) |
| empreendaideias.com.br | `index.html` (por enquanto redireciona para `/bio/`) |

## Editar a página de links

Tudo fica em `bio/index.html`:

- **Links dos banners:** atributos `href` de cada `<a class="banner ...">`.
- **Vídeo do story (avatar):** `VIDEO_ID` no `<script>` no final do arquivo (código do YouTube Shorts).
- **Foto:** substitua `bio/jeff.jpg` (quadrada, ~800×800).

Cada alteração enviada para a branch `main` vai ao ar sozinha em 1–2 minutos.

## Configuração do GitHub Pages (uma vez)

1. **Settings → Pages:** em *Build and deployment*, escolha *Deploy from a branch*, branch `main`, pasta `/ (root)`.
2. Em *Custom domain*, confirme `empreendaideias.com.br` (vem do arquivo `CNAME`).
3. No painel onde o domínio foi registrado (Registro.br ou outro), configure o DNS:

   | Tipo | Nome | Valor |
   |---|---|---|
   | A | `@` (raiz) | `185.199.108.153` |
   | A | `@` | `185.199.109.153` |
   | A | `@` | `185.199.110.153` |
   | A | `@` | `185.199.111.153` |
   | CNAME | `www` | `jefftribuzz.github.io` |

   Apague outros registros A/AAAA da raiz que apontem para a hospedagem antiga.
4. Quando o DNS propagar (de minutos a algumas horas), volte em **Settings → Pages** e marque **Enforce HTTPS**.
