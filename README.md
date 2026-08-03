# Residencial Mirantti — Landing Page

Landing page de alta conversão para o **Residencial Mirantti** (Blendi Empreendimentos · Londrina/PR).

Site estático, sem build step. Hospedado na Vercel.

## 🚀 Stack

- HTML5 + CSS3 (variáveis, grid, flex)
- JavaScript vanilla (sem dependências)
- Fontes Google: Playfair Display + Inter
- WhatsApp como canal de conversão principal (`wa.me/554196486014`)

## 📁 Estrutura

```
.
├── index.html              ← página única (entrypoint)
├── assets/                 ← tudo o que o HTML referencia
│   ├── logo-blendi.png
│   ├── logo-miranti.png
│   ├── logo-miranti-transparente.png
│   ├── minha-casa-mimha-vida.png
│   ├── identidade-visual.png
│   ├── familia-hero-1.jpg
│   ├── familia-hero-2.jpg
│   ├── familia-hero-3.jpg
│   └── criativos/          ← fotos do book oficial
├── _materiais/             ← NÃO vai pro deploy (materiais de apoio)
│   ├── MIRANTTI_Book_Final.pdf
│   ├── Mirantti_Copy_Anuncios.md
│   ├── Mirantti_Copy_Hub.html
│   ├── VIDEOS/
│   └── _originais_familia/
├── vercel.json             ← config de headers + cache
├── package.json            ← metadata + scripts de dev
├── .gitignore
└── README.md
```

## 💻 Rodar localmente

```bash
# opção 1 — direto
abrir index.html no navegador

# opção 2 — servidor local (recomendado)
npm start          # usa npx serve
# ou
python -m http.server 8000
```

Acesse: <http://localhost:8000> ou <http://localhost:3000>

## 📲 Como funciona o WhatsApp

Cada botão CTA abre `https://wa.me/554196486014?text=...` com uma **mensagem pronta** dizendo de onde o lead veio e qual seção clicou. Os códigos de origem estão em `index.html`, no objeto `MESSAGES`:

| Origem (`data-wa`) | Seção                  |
|--------------------|------------------------|
| `nav`              | Cabeçalho              |
| `hero_principal`   | Hero (botão principal) |
| `sobre`            | Sobre                  |
| `galeria_condominio` | Galeria "O Condomínio" |
| `lazer`            | Lazer Completo         |
| `plantas`          | Plantas                |
| `apartamento`      | Apartamento (cômodos)  |
| `localizacao`      | Localização            |
| `cta_final`        | CTA final              |
| `footer`           | Rodapé                 |
| `flutuante`        | Botão flutuante        |

## 🚢 Deploy na Vercel

### Opção 1 — via CLI

```bash
npm i -g vercel
vercel                 # primeiro deploy (preview)
vercel --prod          # promoção para produção
```

### Opção 2 — via GitHub

1. Suba este repositório para o GitHub (sem a pasta `_materiais`)
2. Em <https://vercel.com/new>, importe o repo
3. **Não precisa mexer em nada** — a Vercel detecta automaticamente que é um site estático
4. Cada `git push` na branch `main` dispara deploy automático

## ✏️ Atualizar conteúdo

- **Cores**: edite as variáveis CSS em `:root` no topo de `index.html`
- **Textos**: procure por `<h2>` e `<p class="lead">`
- **Fotos**: troque os arquivos em `assets/criativos/` mantendo o mesmo nome
- **WhatsApp**: edite a constante `PHONE` e o objeto `MESSAGES` no JS

## 📞 Contato

Blendi Empreendimentos · Londrina/PR
WhatsApp: +55 41 9648-6014
