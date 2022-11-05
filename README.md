# devops-django-react-task

## Backend development workflow

```json
virtualenv env
source env/bin/activate
pip install -r requirements.txt
python manage.py runserver
```

## Frontend development workflow

You are to update your name in ./frontend/components/App.js

```json
npm i
npm start
npm run build
```

## For deploying

```json
docker-compose up -d
NB: Image Architecture is Linux, arm64 (M1/M2 chip) to build for a amd64 chip please recompile Dockerfile
```

It should look like this if successful
<img width="1440" alt="Screen Shot 2022-11-02 at 19 30 22" src="https://user-images.githubusercontent.com/66765302/199572589-43bd05b7-95a6-455c-bc25-3cd437c95339.png">
