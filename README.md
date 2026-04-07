
# Charafun API

API de charadas (baseado em helldivers) desenvolvida em Flask com Firestore e deploy na Vercel.

- URL pública: https://charafun.vercel.app/
- Backend: `app.py`
- Autenticação: JWT via `auth.py` (token obrigatório em rotas de criação/atualização/exclusão)

## Endpoints

### 1) GET /  
Retorna status básico da API.

Resposta:
```json
{
  "api": "charafun",
  "Version": "1.0",
  "Author": "J. Cristopher"
}
```

### 2) POST /login
Login admin e geração de token JWT.

Body JSON:
```json
{
  "usuario": "<ADMIN_USER>",
  "senha": "<ADMIN_PASS>"
}
```

Resposta:
```json
{
  "message": "Login realizado com sucesso!",
  "token": "<JWT>"
}
```

### 3) GET /charadas
Lista todas as charadas (open, sem token).

Resposta: array de objetos:
- id (int)
- pergunta (string)
- resposta (string)

### 4) GET /charadas/random
Retorna uma charada aleatória (sem token).

### 5) GET /charadas/<id>
Retorna charada por `id` (sem token).

Retorno 404 se não encontrar:
```json
{ "error": "Charada não encontrada" }
```

- Tratamento de erros 404/500 e validação de dados está implementado.
