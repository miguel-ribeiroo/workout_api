🔧 Como executar o projeto
1️⃣ Clone o repositório
git clone https://github.com/miguel-ribeiroo/workout_api.git
cd workout_api
2️⃣ Suba o banco de dados com Docker
docker compose up -d

O banco será iniciado na porta 5432.

3️⃣ Crie e ative o ambiente virtual
Windows
python -m venv .venv
.venv\Scripts\activate
Linux / Mac
python -m venv .venv
source .venv/bin/activate
4️⃣ Instale as dependências
pip install -r requirements.txt

Caso não exista o arquivo requirements.txt, instale manualmente:

pip install fastapi uvicorn sqlalchemy asyncpg psycopg2-binary alembic pydantic-settings
5️⃣ Execute a aplicação
python -m uvicorn workout_api.main:app --reload
🌐 Acessando a API

Após iniciar o servidor, acesse:

http://127.0.0.1:8000/docs

A documentação interativa é gerada automaticamente pelo FastAPI (Swagger UI).
