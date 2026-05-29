
> Você não precisa virar designer. Precisa saber o suficiente para entregar páginas que parecem profissionais e convertem. Este guia cobre exatamente isso.

---

## Parte 1 — UI: a aparência visual

### 1.1 Tipografia

A tipografia sozinha é responsável por 80% da percepção de profissionalismo de uma página.

**Regras práticas:**

- Use no máximo 2 fontes: uma para títulos, uma para corpo
- Título: fontes com personalidade (serifadas ou display)
- Corpo: fontes limpas e legíveis (sans-serif)
- Tamanho mínimo de corpo: 16px
- Nunca use Arial, Roboto ou Times New Roman em projetos de cliente

**Pares de fontes que funcionam bem (todos no Google Fonts):**

|Título|Corpo|Estilo|
|---|---|---|
|Playfair Display|Lato|Elegante, feminino|
|DM Serif Display|DM Sans|Moderno, sofisticado|
|Syne|Inter|Tech, startup|
|Fraunces|Source Sans 3|Editorial, orgânico|
|Space Grotesk|Mulish|Neutro, profissional|

**Hierarquia de tamanhos (base desktop):**

```
H1 (título principal):  48–64px
H2 (subtítulos):        32–40px
H3 (cards, seções):     20–24px
Corpo:                  16–18px
Legenda / detalhe:      13–14px
```

---

### 1.2 Cores

**A regra 60-30-10:**

- **60%** — cor neutra (fundo, espaços em branco)
- **30%** — cor principal (textos, elementos estruturais)
- **10%** — cor de destaque (CTAs, botões, links)

  Então sim, você vai testar. O processo na prática é:

1. Pega a cor principal da logo
2. Abre o [coolors.co](https://coolors.co)
3. Gera uma paleta a partir dessa cor
4. Escolhe um neutro claro para o fundo
5. Escolhe uma cor de destaque que contraste bem
6. Testa os contrastes no [coolors.co/contrast-checker](https://coolors.co/contrast-checker)

**Erros mais comuns:**

- Usar muitas cores sem propósito
- CTA com cor que não contrasta o suficiente
- Texto cinza claro em fundo branco (ilegível)
- Gradiente roxo em fundo branco (clichê de AI/tech)

**Contraste mínimo para acessibilidade (WCAG):**

- Texto normal: contraste de pelo menos 4.5:1
- Texto grande (+18px): contraste de pelo menos 3:1
- Ferramenta para checar: [coolors.co/contrast-checker](https://coolors.co/contrast-checker)

**Como montar uma paleta do zero:**

1. Escolha a cor principal do cliente (ou da marca)
2. Gere variações claras e escuras no [coolors.co](https://coolors.co)
3. Defina uma cor de destaque complementar (roda cromática)
4. Adicione neutros: off-white para fundo, carvão para texto

---

### 1.3 Espaçamento

Espaçamento generoso = página profissional. Espaçamento apertado = página amadora.

**Use uma escala de 8px:**

```
4px   → micro espaços (entre ícone e texto)
8px   → espaço interno de componentes
16px  → espaço entre elementos relacionados
24px  → espaço entre grupos
48px  → espaço entre seções
80px  → padding vertical de seções
```

**Padding de seções no mobile:** nunca menos de 24px nas laterais. Conteúdo colado na borda da tela quebra a experiência.

---

### 1.4 Hierarquia visual

O olho humano segue padrões previsíveis. Você precisa guiar o visitante para o CTA.

**Padrão F (texto denso):** o olho varre horizontalmente no topo, depois desce pelo lado esquerdo.

**Padrão Z (landing page):** o olho vai do canto superior esquerdo ao direito, desce na diagonal e varre novamente — comum em páginas com imagem e texto lado a lado.

**Como criar hierarquia:**

- O elemento mais importante deve ser o maior e mais contrastante
- Use peso da fonte (bold) com moderação — se tudo é bold, nada é
- Espaço em branco é tão importante quanto o conteúdo
- Um único CTA por dobra de tela (o que o usuário vê sem rolar)

---

## Parte 2 — UX: a experiência do usuário

### 2.1 O fluxo de uma landing page

O visitante segue uma jornada emocional previsível. Sua página precisa acompanhar esse fluxo:

```
Atenção     → Hero: headline forte, imagem relevante
Interesse   → Problema: "isso é exatamente o que eu sinto"
Desejo      → Solução + Benefícios: "quero isso"
Confiança   → Prova social: "outras pessoas já tiveram resultado"
Ação        → CTA: formulário ou botão de compra
```

Se o visitante sair antes do CTA, uma dessas etapas falhou.

---

### 2.2 O botão de CTA

O CTA (Call to Action) é o elemento mais importante da página. Trate com cuidado.

**Boas práticas:**

- Texto do botão deve dizer o que acontece ao clicar: "Quero minha consulta gratuita" é melhor que "Enviar"
- Use verbos na primeira pessoa: "Quero", "Preciso", "Me inscrever"
- Cor do botão deve contrastar fortemente com o fundo
- Tamanho mínimo no mobile: 48px de altura (para caber o dedo)
- Adicione micro-copy abaixo: "Sem compromisso" ou "Resposta em 24h"

**Exemplos de CTA fraco vs forte:**

|Fraco|Forte|
|---|---|
|Enviar|Quero garantir minha vaga|
|Saiba mais|Ver como funciona|
|Clique aqui|Começar agora — é gratuito|
|Cadastrar|Quero receber meu desconto|

---

### 2.3 Formulários

Formulário longo = menos conversão. Peça apenas o essencial.

**Regra:** cada campo a mais reduz a taxa de conversão em média 10%.

- Para captura de leads: nome + e-mail (ou só e-mail)
- Para orçamento: nome + WhatsApp + objetivo
- Para venda: o mínimo necessário para processar o pedido

**Boas práticas de UX em formulários:**

- Labels acima dos campos, nunca só placeholder
- Mensagem de erro clara: "E-mail inválido" em vez de "Campo obrigatório"
- Botão de envio deve mudar de estado após clique (evita duplo envio)
- Página ou mensagem de agradecimento após envio

---

### 2.4 Design responsivo (mobile first)

Mais de 70% dos acessos vêm do celular. Projete para mobile primeiro, depois adapte para desktop.

**O que muda do desktop para o mobile:**

- Colunas lado a lado viram uma coluna só
- Textos maiores para legibilidade
- Botões com largura total (100%)
- Imagens redimensionadas
- Menus colapsados

**Como testar no VS Code:**

Abra o arquivo no navegador → F12 → ícone de dispositivo móvel → escolha um celular.

**Breakpoints essenciais:**

```css
/* Mobile (padrão — escreva tudo aqui primeiro) */

/* Tablet */
@media (min-width: 768px) { }

/* Desktop */
@media (min-width: 1024px) { }
```

---

## Parte 3 — Como desenvolver o olho clínico

Saber olhar para um design bom e entender por que ele funciona é uma habilidade que se treina.

### Sites para estudar referências

- [land-book.com](https://land-book.com) — curadoria de landing pages reais
- [awwwards.com](https://www.awwwards.com) — sites premiados por design
- [dribbble.com](https://dribbble.com) — referências de UI e componentes
- [screenlane.com](https://screenlane.com) — detalhes de UI (botões, formulários, cards)
- [mobbin.com](https://mobbin.com) — referências de UX mobile

### Como estudar uma página de referência

Quando encontrar uma página que parece profissional, pergunte:

1. Qual é a hierarquia visual? O que meu olho vê primeiro?
2. Quais fontes estão sendo usadas? (Use a extensão WhatFont no Chrome)
3. Quais são as cores principais? (Use a extensão ColorZilla)
4. Quanto espaço em branco existe entre os elementos?
5. Como o CTA se destaca do resto?
6. Como a página se comporta no mobile?

---

## Parte 4 — Ferramentas essenciais

|Ferramenta|Para que serve|Custo|
|---|---|---|
|[Figma](https://figma.com)|Prototipar o layout antes de codar|Gratuito|
|[Coolors](https://coolors.co)|Criar e testar paletas de cores|Gratuito|
|[Google Fonts](https://fonts.google.com)|Fontes para projetos web|Gratuito|
|[Squoosh](https://squoosh.app)|Comprimir imagens sem perder qualidade|Gratuito|
|[WhatFont](https://chrome.google.com/webstore/detail/whatfont)|Identificar fontes em qualquer site|Gratuito|
|[ColorZilla](https://www.colorzilla.com)|Capturar cores de qualquer site|Gratuito|
|[Unsplash](https://unsplash.com)|Fotos gratuitas de alta qualidade|Gratuito|

---

## Resumo: os 10 princípios para não errar

1. **Máximo 2 fontes** por projeto
2. **CTA com cor que contrasta** fortemente — nunca apague o botão no fundo
3. **Espaçamento generoso** — em dúvida, coloque mais espaço
4. **Uma única ação esperada** por página
5. **Mobile primeiro** — teste sempre no celular antes de mostrar ao cliente
6. **Hierarquia clara** — o título principal deve ser o elemento dominante
7. **Texto do CTA em primeira pessoa** e orientado à ação
8. **Formulário curto** — peça só o essencial
9. **Imagens otimizadas** — página lenta mata conversão
10. **Estude referências** — 30 minutos por semana no land-book.com já faz diferença

---

> **Lembrete:** o cliente não vai elogiar seu CSS. Ele vai elogiar a página. Invista tempo em design — é o que diferencia um freelancer mediano de um que cobra bem.