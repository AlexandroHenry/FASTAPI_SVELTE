# FASTAPI_SVELTE

## BACKEND

* Virtual Environment
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
# add your model's MetaData object here
# for 'autogenerate' support
# from myapp import mymodel
# target_metadata = mymodel.Base.metadata
target_metadata = models.Base.metadata
(... 생략 ...)

alembic revision --autogenerate
alembic upgrade head





## FRONTEND

npm create vite@latest frontend -- --template svelte
npm install
npm run dev