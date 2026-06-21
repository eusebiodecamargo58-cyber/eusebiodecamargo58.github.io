[README.md](https://github.com/user-attachments/files/29182556/README.md)
# Scanner de Figurinhas - Copa do Mundo 2026

Aplicação web de página única (Single-Page Application) para escanear códigos alfanuméricos do verso das figurinhas do álbum da Copa do Mundo FIFA 2026 usando a câmera do smartphone e OCR.

## 🚀 Como Rodar Localmente

### Opção 1: Abrir diretamente no navegador
1. Abra o arquivo `index.html` diretamente no seu navegador
2. **Nota**: O acesso à câmera pode não funcionar em alguns navegadores devido a restrições de segurança quando o arquivo é aberto localmente (file:// protocolo). Para testar a câmera, use um servidor local ou faça o deploy.

### Opção 2: Usando Python (se instalado)
```bash
python -m http.server 8000
```
Depois acesse: `http://localhost:8000`

### Opção 3: Usando Node.js (se instalado)
```bash
npx serve
```
Ou instale o http-server globalmente:
```bash
npm install -g http-server
http-server
```

### Opção 4: Usando VS Code Live Server
1. Instale a extensão "Live Server" no VS Code
2. Clique com o botão direito no `index.html` e selecione "Open with Live Server"

## 📦 Deploy

### GitHub Pages

1. **Crie um repositório no GitHub**:
   - Vá para github.com e crie um novo repositório
   - Faça upload do arquivo `index.html`

2. **Ative o GitHub Pages**:
   - Vá para Settings > Pages
   - Em "Source", selecione "Deploy from a branch"
   - Selecione a branch `main` (ou master)
   - Clique em "Save"

3. **Aguarde o deploy**:
   - Em alguns minutos, seu site estará disponível em: `https://seu-usuario.github.io/Leitor-Figurinhas/`

### Vercel

1. **Instale a Vercel CLI** (opcional):
```bash
npm install -g vercel
```

2. **Deploy via CLI**:
```bash
cd c:/Users/migue/Projects/Leitor-Figurinhas
vercel
```

3. **Deploy via Dashboard**:
   - Vá para [vercel.com](https://vercel.com)
   - Clique em "Add New Project"
   - Importe o repositório do GitHub
   - Clique em "Deploy"

## ⚠️ Importante: HTTPS

O acesso à câmera do dispositivo **requer** conexão segura HTTPS. Por isso:
- **Localmente**: Alguns navegadores podem bloquear o acesso à câmera em `http://localhost`. Use `https://localhost` ou faça o deploy.
- **Produção**: GitHub Pages e Vercel fornecem HTTPS automaticamente.

## 📱 Como Usar

1. Abra a aplicação no seu smartphone (recomendado) ou computador
2. Conceda permissão para acessar a câmera quando solicitado
3. Posicione o código da figurinha dentro do retângulo verde
4. Clique no botão "ESCANEAR"
5. Aguarde o processamento OCR
6. O código detectado aparecerá na tela

## 🛠️ Stack Tecnológica

- **Frontend**: HTML5, CSS3, JavaScript Vanilla
- **OCR**: Tesseract.js v5 (via CDN)
- **Deploy**: GitHub Pages ou Vercel

## 📋 Requisitos Técnicos Implementados

✅ Arquivo único index.html  
✅ Tesseract.js via CDN  
✅ Tema escuro (#1a1a1a)  
✅ Design mobile-first responsivo  
✅ Elemento de vídeo centralizado  
✅ Retângulo de foco verde (3px solid #00ff00)  
✅ Botão ESCANEAR com destaque  
✅ Texto indicador de status  
✅ Área de resultado com fonte grande  
✅ Acesso à câmera traseira com fallback  
✅ Mecanismo de crop (recorte) da imagem  
✅ Pré-processamento (escala de cinza + contraste)  
✅ Processamento OCR com Tesseract.js  
✅ Sanitização de string (maiúsculas, trim, remove newlines)  
✅ Tratamento de erros (código < 2 caracteres)  
✅ Botão desativado durante processamento  
✅ Tratamento de permissão negada da câmera  

## 🔧 Solução de Problemas

### Câmera não funciona
- Verifique se você concedeu permissão de câmera
- Certifique-se de estar usando HTTPS (necessário para acesso à câmera)
- Tente usar um navegador diferente (Chrome, Firefox, Safari)
- No desktop, a câmera pode não funcionar devido a restrições de hardware

### OCR não detecta o código
- Melhore a iluminação
- Aproxime mais a câmera
- Certifique-se de que o código está dentro do retângulo verde
- Evite movimentos bruscos durante o escaneamento

### Erro de carregamento do Tesseract.js
- Verifique sua conexão com a internet (o CDN precisa ser acessado)
- Tente recarregar a página

## 📄 Licença

Este projeto é open source e está disponível para uso pessoal e educacional.
