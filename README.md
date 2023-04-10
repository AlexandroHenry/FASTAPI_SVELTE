# FASTAPI_SVELTE

## BACKEND

\n Virtual Environment
python3 -m venv venv

* Entering VENV
source venv/bin/activate

pip install fastapi
python -m pip install --upgrade pip

pip install "uvicorn[standard]"

main.py

pip install sqlalchemy
pip install alembic -> alembic init migrations

* edit alembic.ini 
sqlalchemy.url = sqlite:///./myapi.db

* edit env.py
(... 생략 ...)
import models
(... 생략 ...)
target_metadata = models.Base.metadata
(... 생략 ...)

alembic revision --autogenerate
alembic upgrade head

pip install "pydantic[email]"
pip install "passlib[bcrypt]"
pip install python-multipart
pip install "python-jose[cryptography]"



## FRONTEND

npm create vite@latest frontend -- --template svelte
npm install
npm run dev

* Svelte 라우터
npm install svelte-spa-router

npm install bootstrap
npm install moment
npm install qs