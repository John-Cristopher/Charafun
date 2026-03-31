# Endpoints (URLs)

## ENDPOINT PÚBLICOS (Open)
> GET - /charadas - (Todas as charadas) <br>
> GET - /charadas/aleatorias - (1 charada sorteada)<br>
> GET - /charadas/id - (1 charada pelo id)<br>

## ENDPOINT PRIVADO (Autenticação Bearer)
> POST - /charadas - (Criar uma nova charada)<br>
> PATCH - /charadas/<int:id> - (Alterar parcialmente pelo id)<br>
> PUT - /charadas/<int:id> - (Alterar inteiramente pelo id)<br>
> DELETE - /charadas/<int:id> - (Apagar 1 charada pelo id)<br>

Database: FIrebase Firestone da Google (NO-SQL - Não relacional) <br>
HOST: Vercel


1. Task: Instalar o JWT
pip install PyPWT

2. Task: Apagar 