# Defensas Copabo — PWA

App offline de inspeção de defensas (Copabo Infra).  
Funciona no **iPhone** e **Android** como aplicativo instalado na tela inicial.

## Arquivos desta pasta

```
pwa-copabo/
├── index.html              ← app
├── manifest.webmanifest    ← configuração PWA
├── sw.js                   ← cache offline
├── icons/                  ← ícones do app
└── README.md
```

---

## Passo a passo — publicar com GitHub Desktop (sem erro)

### 1) Conta e programa
1. Crie conta em [https://github.com](https://github.com) (se ainda não tiver).
2. Instale o **GitHub Desktop**: [https://desktop.github.com](https://desktop.github.com)
3. Abra o GitHub Desktop e faça login com a conta do GitHub.

### 2) Criar o repositório
1. No GitHub Desktop: **File → New Repository…**
2. Preencha:
   - **Name:** `defensas-copabo` (ou outro nome sem espaços)
   - **Local path:** escolha uma pasta no computador
   - Marque **Initialize this repository with a README** (pode deixar desmarcado se preferir)
3. Clique em **Create Repository**.

### 3) Colocar os arquivos do app
1. Abra a pasta do repositório que o GitHub Desktop criou (botão **Show in Explorer** / **Show in Finder**).
2. **Apague** o que tiver dentro (se houver só o README vazio, pode substituir).
3. Copie **todo o conteúdo** desta pasta `pwa-copabo` **para dentro** da pasta do repositório:
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - pasta `icons/`
   - `README.md` (opcional)
4. Volte ao GitHub Desktop. Os arquivos devem aparecer em **Changes**.
5. Em **Summary**, escreva: `Publicar app Defensas Copabo`
6. Clique em **Commit to main**.

### 4) Enviar para o GitHub (nuvem)
1. Clique em **Publish repository** (ou **Push origin**).
2. Deixe **Keep this code private** desmarcado se quiser página pública grátis (GitHub Pages em repo privado exige plano pago em alguns casos).
3. Confirme **Publish repository**.

### 5) Ativar GitHub Pages
1. Abra o site do GitHub no navegador → entre no repositório `defensas-copabo`.
2. Vá em **Settings** (Configurações).
3. No menu esquerdo: **Pages**.
4. Em **Build and deployment → Source**:
   - **Deploy from a branch**
   - Branch: **main**
   - Pasta: **/ (root)**
5. Clique em **Save**.
6. Aguarde 1 a 2 minutos. Atualize a página até aparecer o endereço, por exemplo:

```
https://SEU_USUARIO.github.io/defensas-copabo/
```

Substitua `SEU_USUARIO` pelo seu usuário do GitHub.

---

## Instalar no celular

### Android (Chrome)
1. Abra o link do GitHub Pages no **Chrome**.
2. Toque no menu **⋮** → **Instalar app** ou **Adicionar à tela inicial**.
3. Confirme. O ícone **Defensas Copabo** aparece na tela inicial.

### iPhone / iPad (Safari)
1. Abra o **mesmo link** no **Safari** (não no Chrome).
2. Toque no botão **Compartilhar** (quadrado com seta para cima).
3. Role e toque em **Adicionar à Tela de Início**.
4. Confirme o nome e toque em **Adicionar**.

Depois de instalado, o app abre em tela cheia (sem barra do navegador) e continua funcionando **offline** (inspeções e fotos ficam no aparelho).

---

## Atualizar o app no futuro
1. Substitua o `index.html` (ou outros arquivos) na pasta local do repositório.
2. No GitHub Desktop: **Commit** → **Push origin**.
3. Em até 1–2 minutos o site atualiza. No celular, abra o app online uma vez para o cache renovar.

---

## Teste local (opcional)
No computador, dentro da pasta do app:

```bash
python3 -m http.server 8080
```

Abra `http://localhost:8080` no navegador.  
Service Worker só funciona em `http`/`https` (não em arquivo `file://`).
