
## Stack

- **Frontend:** Vue 3 + Vite + Pinia + Vue Router → deploy no Netlify ou GitHub Pages
- **Backend:** Node.js + Express → deploy no Railway
- **Banco de dados:** PostgreSQL
- **Imagens:** Cloudinary (upload e hospedagem)
- **Auth:** JWT (JSON Web Token)

---

## Arquitetura

```
frontend/
  src/
    views/          ← Login, Register, Home, Profile
    components/     ← PinCard, PinModal, Navbar
    stores/         ← auth.js, pins.js (Pinia)
    router/         ← index.js

backend/
  routes/           ← auth.js, pins.js
  middleware/       ← authMiddleware.js
```

---

## Banco de dados

```sql
users   → id, email, password_hash, username
pins    → id, user_id, image_url, title, description, created_at
saved   → id, user_id, pin_id   ← tabela de relacionamento para "salvar pin"
```

---

## Endpoints da API

|Método|Rota|O que faz|
|---|---|---|
|POST|`/auth/register`|Cria usuário|
|POST|`/auth/login`|Retorna JWT|
|GET|`/pins`|Feed com todos os pins|
|POST|`/pins`|Cria pin com upload de imagem|
|DELETE|`/pins/:id`|Deleta pin próprio|
|POST|`/pins/:id/save`|Salva pin de outro usuário|
|GET|`/pins/saved`|Pins salvos pelo usuário logado|

---

## MVP — o mínimo para o projeto funcionar

|Funcionalidade|Por quê é essencial|
|---|---|
|Registro e login|Sem isso não tem "usuários diferentes"|
|Criar pin (upload de imagem + título)|É a ação principal do app|
|Feed masonry com todos os pins|É o que define visualmente o Pinterest|
|Salvar pin no seu perfil|A funcionalidade mais característica do Pinterest|
|Ver seus pins salvos|Fechar o loop do "salvar"|

---

## Fora do MVP (evoluir depois)

- Boards (categorias de pins salvos)
- Comentários
- Seguir outros usuários
- Busca por pins
- Perfil editável com avatar

---

## Fases de desenvolvimento

### Fase 1 — Back-end

- [ ] Configurar projeto Node.js + Express
- [ ] Conectar PostgreSQL e criar tabelas
- [ ] Rotas de auth (register + login com JWT)
- [ ] Rota de criar pin com upload via Cloudinary
- [ ] Rota de salvar pin (tabela `saved`)
- [ ] Rota de feed e pins salvos

### Fase 2 — Front-end

- [ ] Configurar Vue 3 + Vite + Vue Router + Pinia
- [ ] Telas de Login e Registro
- [ ] Store de auth (token no localStorage)
- [ ] Feed com masonry grid
- [ ] Modal de criar pin (upload de imagem)
- [ ] Botão de salvar pin
- [ ] Página de pins salvos

### Fase 3 — Deploy

- [ ] Back-end no Railway + variáveis de ambiente
- [ ] Banco no Railway (PostgreSQL)
- [ ] Front-end no Netlify ou GitHub Pages
- [ ] Testar fluxo completo em produção

---

## Complexidade estimada

|Dedicação|Estimativa|
|---|---|
|~2h por dia|3 a 4 semanas|
|Final de semana intenso|MVP funcional possível|

---

## Decisão importante: armazenamento de imagens

**Cloudinary** é a escolha recomendada:

- Gratuito até 25GB
- Você manda a imagem pra API deles, eles hospedam e devolvem uma URL
- Funciona bem no Railway (sem risco de perder arquivos no restart do servidor)

**Multer local** é mais simples de implementar, mas os arquivos somem se o servidor reiniciar — só serve pra protótipo local.