# 🖥️ O que é um Servidor?

## Definição simples

Um **servidor** é um computador (ou programa) que fornece serviços, dados ou recursos para outros computadores — chamados de **clientes**. A relação entre eles é chamada de modelo **cliente-servidor**.

> 💡 **Analogia:** Pense em um servidor como um garçom em um restaurante. Você (cliente) faz um pedido, o garçom (servidor) vai até a cozinha buscar e te entrega o que você pediu.

---

## Como funciona?

```
[ Cliente ]  ──── requisição ────▶  [ Servidor ]
[ Cliente ]  ◀─── resposta ────────  [ Servidor ]
```

1. O **cliente** faz uma **requisição** (ex: acessar um site)
2. O **servidor** recebe, processa e devolve uma **resposta** (ex: a página HTML)
3. O cliente exibe o resultado para o usuário

---

## Tipos de Servidor

| Tipo | O que faz | Exemplo |
|------|-----------|---------|
| **Web** | Entrega páginas de sites | Apache, Nginx |
| **Banco de Dados** | Armazena e consulta dados | MySQL, PostgreSQL |
| **Arquivos** | Compartilha arquivos em rede | FTP, Samba |
| **E-mail** | Envia e recebe e-mails | Postfix, Exchange |
| **DNS** | Traduz domínios em IPs | BIND, Cloudflare |
| **Aplicação** | Executa lógica de negócio | Node.js, Tomcat |
| **Proxy** | Intermediário entre cliente e servidor | Nginx, Squid |

---

## Servidor físico vs. virtual

### 🏗️ Servidor Físico (Bare Metal)
- Um computador real, dedicado
- Alta performance
- Custo elevado de manutenção
- Usado em grandes empresas

### ☁️ Servidor Virtual (VPS / Cloud)
- Simulado dentro de um servidor físico
- Mais barato e flexível
- Fácil de escalar
- Exemplos: AWS, Google Cloud, Azure

---

## Partes essenciais de um servidor

```
┌─────────────────────────────────┐
│           SERVIDOR              │
│                                 │
│  🧠 CPU     → processa dados    │
│  💾 RAM     → memória rápida    │
│  🗄️ HD/SSD  → armazena dados   │
│  🌐 Rede    → conecta ao mundo  │
│  🔋 Fonte   → energia 24/7      │
└─────────────────────────────────┘
```

> Servidores geralmente ficam ligados **24 horas por dia, 7 dias por semana** — diferente de um computador pessoal.

---

## Exemplo do dia a dia: acessando um site

1. Você digita `www.google.com` no navegador
2. O navegador (cliente) consulta o **servidor DNS** para saber o IP do Google
3. O navegador se conecta ao **servidor web** do Google
4. O servidor web retorna o HTML da página
5. Seu navegador exibe a página na tela

```
Você → Navegador → DNS → Servidor Web do Google → Página exibida ✅
```

---

## Conceitos importantes

- **IP**: endereço único do servidor na rede (ex: `192.168.0.1`)
- **Porta**: canal de comunicação específico (ex: porta `80` = HTTP, `443` = HTTPS)
- **Protocolo**: linguagem usada para comunicação (ex: HTTP, FTP, SMTP)
- **Latência**: tempo de resposta entre cliente e servidor
- **Uptime**: tempo que o servidor fica disponível sem cair

---

## Resumo

| Conceito | Explicação rápida |
|----------|-------------------|
| Servidor | Computador que fornece serviços |
| Cliente | Quem faz a requisição |
| Requisição | Pedido do cliente ao servidor |
| Resposta | O que o servidor devolve |
| Protocolo | Regras da comunicação |

---

> 📚 **Próximos passos:** Aprenda sobre **HTTP/HTTPS**, **APIs REST** e **containers Docker** para se aprofundar no mundo dos servidores!