# 📥 Instagram Video Downloader - Full Stack Project

Este projeto é uma ferramenta web para baixar vídeos do Instagram (Reels/Posts) utilizando uma arquitetura moderna dividida entre Frontend e Backend.

---
[[Base de conhecimento — Shell próprio em Python]]
## 🏗️ Arquitetura do Sistema

O projeto funciona através da comunicação de dois serviços distintos hospedados na nuvem:

1.  **Frontend (O Rosto):** Hospedado no **GitHub Pages**. Escrito em HTML5, CSS3 e JavaScript Vanilla.
2.  **Backend (O Cérebro):** Hospedado no **Render**. Escrito em **Python** com o framework **Flask**.

---

## 🛠️ Tecnologias Utilizadas

### Backend (Python)
* **Flask:** Micro-framework para criar a API que recebe os links.
* **yt-dlp:** Biblioteca poderosa que faz a "raspagem" e extração do vídeo real dos servidores do Instagram.
* **Flask-CORS:** Essencial para permitir que o site no GitHub Pages tenha permissão de acessar o servidor no Render.
* **Gunicorn:** Servidor HTTP de produção para rodar o Python de forma estável na nuvem.

### Frontend (JavaScript)
* **Fetch API:** Utilizada para enviar a URL via método `POST` e receber o arquivo binário.
* **Blobs:** O vídeo é recebido como um "Blob" (Binary Large Object), permitindo o download direto no navegador sem armazenar arquivos permanentemente no servidor.

---

## 🧠 O que eu aprendi neste projeto?

### 1. Comunicação entre Domínios (CORS)
Aprendi que navegadores bloqueiam requisições entre sites diferentes por segurança. Para resolver isso, configurei o **Cross-Origin Resource Sharing (CORS)** no Flask para aceitar apenas o meu domínio do GitHub.

### 2. Manipulação de Arquivos Binários
No JavaScript, aprendi a transformar uma resposta de rede em um link de download temporário usando `URL.createObjectURL(blob)`, simulando um clique invisível para o usuário.

### 3. Deploy e Variáveis de Ambiente
Configurei o **Render** para rodar o Python, entendendo a importância da variável `PORT` e do comando de inicialização `gunicorn main:app`. Também aprendi a configurar o **Root Directory** quando o código está em subpastas.

### 4. Gerenciamento de Dependências
Uso do `requirements.txt` para garantir que o servidor na nuvem tenha exatamente as mesmas versões das bibliotecas que usei no meu computador (Ubuntu).

---

## 🚀 Como Rodar Localmente

1. **Backend:**
   ```bash
   cd backend
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   python3 main.py[[Base de conhecimento — Shell próprio em Python]]