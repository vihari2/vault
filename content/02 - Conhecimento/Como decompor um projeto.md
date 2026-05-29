## O problema que eu tinha

Eu sabia lógica de programação mas travava na hora de começar um projeto. O motivo: cursos ensinam a resolver problemas já decompostos. A habilidade que faltava era **decompor o problema do zero**.

## Como decompor um projeto

Pega o projeto e fica perguntando _"o que precisa existir pra isso funcionar?"_ até chegar em algo pequeno o suficiente pra codar.

Separa sempre em:

- **Essencial** → faz agora (versão 1)
- **Extra** → faz depois (versão 2)

## O que é CRUD

As 4 operações básicas de qualquer app:

- **C**reate → criar
- **R**ead → listar
- **U**pdate → editar
- **D**elete → excluir

## JavaScript que eu usei

```js
// Pegar elemento do HTML
document.getElementById('id')

// Criar elemento
document.createElement('li')

// Colocar HTML dentro de um elemento
elemento.innerHTML = '<p>texto</p>'

// Colocar texto simples
elemento.innerText = 'texto'

// Adicionar filho dentro de um pai
pai.appendChild(filho)

// Remover filho de um pai
pai.removeChild(filho)

// Trocar um filho por outro
pai.replaceChild(novo, antigo)

// Escutar evento
elemento.addEventListener('click', function() {})

// Aplicar CSS pelo JavaScript
elemento.style.textDecoration = 'line-through'
```

## Como os dados evoluem

|Nível|Onde ficam os dados|
|---|---|
|JS puro|Memória do navegador (some ao atualizar)|
|localStorage|Navegador (limite de 5MB, por navegador)|
|Backend + banco|Servidor (acessível de qualquer lugar)|

## Fluxo profissional (Front + Back)

1. Front faz requisição HTTP pro backend (`GET`, `POST`, `PUT`, `DELETE`)
2. Backend recebe, salva no banco e devolve um status
3. Front recebe o status (`200` sucesso, `201` criado, `404` não encontrado, `500` erro) e atualiza a tela

## Ambientes de uma empresa

- **Local** → você desenvolve no seu PC, banco no HD
- **Homologação** → servidor de teste, cliente aprova
- **Produção** → servidor real, onde os usuários acessam


## Por que existem rotas no backend

A rota é o **endereço** do recurso, o método HTTP é a **ação** que você quer fazer nele.
 
```
GET     /tarefas        → listar tarefas
POST    /tarefas        → criar tarefa
PUT     /tarefas/1      → editar tarefa de id 1
DELETE  /tarefas/1      → excluir tarefa de id 1
 
GET     /usuarios       → listar usuários
POST    /usuarios       → criar usuário
```
 
Sem rotas o backend não saberia distinguir se você quer criar uma tarefa ou deletar um usuário.
