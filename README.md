# Lana Del Rey Fan Club (site completo)

Fã clube não oficial: cadastro/login com JWT, 4 CRUDs autenticados e paginados (Músicas com upload/download, Álbuns, Fotos, Fun Pages & Redes), tema branco e vermelho, responsivo.

## Rodando com Docker
```
cp .env.example .env     # edite as senhas
docker compose up --build
```
Acesse http://localhost (só o Nginx expõe porta; MySQL fica numa rede interna).

## Rodando sem Docker (dev)
- MySQL local + `backend/.env` com DB_HOST, DB_USER, DB_PASSWORD, DB_NAME, JWT_SECRET → `cd backend && npm i && npm run dev`
- `cd frontend && npm i && npm run dev` (http://localhost:5173, proxy para a API)

## API
`POST /api/auth/login` · `POST /api/users` · `GET /api/users/me` · `PUT /api/users/:id`
`/api/{albums,songs,photos,posts}` (GET paginado `?page=&limit=&q=`, GET/:id, POST, PUT/:id, DELETE/:id) · `GET /api/songs/:id/download`
# Lana_FunPage
