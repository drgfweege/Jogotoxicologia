# Circuito Lento — Jogo de Toxicologia (Depressores do SNC)

PWA educativa: jogo de tabuleiro sobre drogas depressoras do sistema nervoso central.

## Estrutura
```
index.html        # o jogo (com manifest + service worker registrados)
manifest.json     # Web App Manifest
sw.js             # Service worker (cache offline)
icons/            # ícones 192, 512 e 512-maskable
```

## Deploy no Cloudflare Pages via GitHub (mesmo fluxo do DengueCare)

### 1. Subir ao GitHub
```bash
cd circuito-lento
git init
git add .
git commit -m "Circuito Lento - PWA jogo depressores SNC"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/circuito-lento.git
git push -u origin main
```

### 2. Conectar no Cloudflare Pages
1. Dashboard Cloudflare → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. Selecione o repositório `circuito-lento`
3. Configurações de build:
   - **Framework preset:** None
   - **Build command:** (deixe vazio)
   - **Build output directory:** `/` (raiz)
4. **Save and Deploy**

Pronto: ficará em `circuito-lento.pages.dev`.

## Empacotar para Google Play (PWABuilder)
1. Acesse https://www.pwabuilder.com
2. Cole a URL `https://circuito-lento.pages.dev`
3. Aba **Android** → **Generate Package** → baixe o `.aab`
4. Suba no Google Play Console (mesma conta de dev, taxa única já paga)

## Instalação direta (sem loja, Android e iOS)
Abrir a URL no navegador → "Adicionar à tela inicial". Funciona offline.
