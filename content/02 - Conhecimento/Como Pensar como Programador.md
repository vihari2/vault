
> Programar é resolver problemas. O código é só a consequência.

---

## O Mindset Base

- **Decomponha** — quebre qualquer problema em partes menores
- **Padrões** — reconheça soluções que já existem
- **Debug** — errou? Investigue, não entre em pânico
- **Abstraia** — modele o mundo em estruturas simples

---

## 🎨 Frontend — O que o usuário vê

O frontend é tudo que acontece no **navegador**.

### Como pensar:

- _O que o usuário precisa ver e fazer aqui?_
- _Como os dados chegam até a tela?_
- _O que muda quando o usuário interage?_

### Fluxo mental:

```
Usuário clica → Evento dispara → Estado muda → Tela atualiza
```

### Conceitos-chave:

|Conceito|O que é|
|---|---|
|HTML|Estrutura (esqueleto)|
|CSS|Estilo (aparência)|
|JavaScript|Comportamento (ação)|
|Estado|Os dados que a tela exibe|
|Componente|Pedaço reutilizável da interface|

---

## ⚙️ Backend — O que acontece por baixo

O backend é o **servidor**: regras, dados e segurança.

### Como pensar:

- _De onde vêm os dados?_
- _Quem tem permissão de fazer o quê?_
- _Como garantir que os dados estejam corretos?_

### Fluxo mental:

```
Requisição chega → Verifica permissão → Processa lógica → Retorna resposta
```

### Conceitos-chave:

|Conceito|O que é|
|---|---|
|API|A ponte entre front e back|
|Rota|Um endereço que o servidor responde|
|Banco de dados|Onde os dados ficam guardados|
|Autenticação|Confirmar quem é o usuário|
|CRUD|Criar, ler, atualizar, deletar dados|

---

## 🔄 O Fluxo Completo

```
[Usuário] 
    ↓ digita e clica
[Frontend]
    ↓ envia requisição HTTP
[API / Backend]
    ↓ consulta ou salva
[Banco de Dados]
    ↑ retorna os dados
[Backend]
    ↑ formata e responde
[Frontend]
    ↑ exibe na tela
[Usuário] ← vê o resultado
```

---

## 💡 Dica Prática

Antes de codar, responda 3 perguntas:

1. **O que entra?** (input do usuário)
2. **O que acontece?** (lógica)
3. **O que sai?** (resultado na tela ou no banco)

Isso vale tanto pro frontend quanto pro backend.

---

## 🛤️ Por onde começar

```
HTML + CSS → JavaScript → um framework (React) → Node.js ou Python no back → Banco de dados
```

Não precisa aprender tudo de uma vez. **Um passo de cada vez.**

[[Essencial para landing pages]]





