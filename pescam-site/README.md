# PesCam — Site Oficial

Site SEO do app PesCam. HTML puro, hospedado no GitHub Pages.

## Estrutura de Arquivos

```
/
├── index.html                    ← Home (palavra-chave: câmera para pesca)
├── style.css                     ← CSS global compartilhado
├── main.js                       ← JS compartilhado (nav, FAQ, contador)
├── icon.png                      ← Ícone do app (copiar do Android Studio)
├── sitemap.xml                   ← Sitemap para Google
├── robots.txt                    ← Instruções para robôs do Google
├── CNAME                         ← Domínio personalizado pescam.com.br
├── .nojekyll                     ← Desabilita Jekyll (usar HTML puro)
├── como-gravar-pescaria/
│   └── index.html                ← Pilar SEO #1
├── camera-para-pesca/
│   └── index.html                ← Pilar SEO #2
├── como-nao-perder-fisgada/
│   └── index.html                ← Pilar SEO #3
├── pesca-no-caiaque/
│   └── index.html                ← Segmento caiaqueiro
├── app/
│   └── index.html                ← Página de download (conversão)
└── politica-de-privacidade/
    └── index.html                ← Política (já existia)
```

## Como Fazer o Deploy

### 1. Copie todos os arquivos para o repositório pescamapp/pescamapp.github.io
- Substitua o index.html atual (era só a política)
- Adicione todos os outros arquivos e pastas

### 2. Copie o ícone do app
- Pegue o arquivo `ic_launcher.png` do Android Studio
- Renomeie para `icon.png`
- Coloque na raiz do repositório

### 3. Configure o domínio no Registro.br
- Acesse registro.br → pescam.com.br → DNS
- Adicione os registros CNAME abaixo:

```
CNAME  www     pescamapp.github.io
A      @       185.199.108.153
A      @       185.199.109.153
A      @       185.199.110.153
A      @       185.199.111.153
```

### 4. Configure no GitHub Pages
- Repositório → Settings → Pages
- Source: Deploy from a branch → main → / (root)
- Custom domain: pescam.com.br
- ☑ Enforce HTTPS

### 5. Quando o app for aprovado na Play Store
- Atualize o link do botão em `app/index.html`
- Atualize o link "Baixar Grátis" em todos os outros arquivos
- Busque por `https://play.google.com/store/apps/details?id=com.pescam.app` e confirme que está correto

### 6. Cadastre no Google Search Console
- Acesse search.google.com/search-console
- Adicione propriedade: pescam.com.br
- Verifique via DNS (adicionar TXT no Registro.br)
- Envie o sitemap: pescam.com.br/sitemap.xml

## Manutenção

Para editar qualquer página, edite o arquivo `index.html` da pasta correspondente.
O CSS é compartilhado em `style.css` — qualquer mudança de visual aplica em todo o site.

Contato: admin@pescam.com.br
