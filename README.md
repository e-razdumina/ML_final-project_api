python-flask-docker
Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy API: flask 
Данные: с kaggle - https://www.kaggle.com/blackmoon/russian-language-toxic-comments

Задача: предсказать по комментарию является ли он токсичным (поле toxic). Бинарная классификация

Используемые признаки:

comment (text)
Преобразования признаков: tfidf

Модель: GradientBoostingClassifier

Клонируем репозиторий и создаем образ

$ git clone https://github.com/e-razdumina/ML_final-project_api.git
$ cd GB_docker_flask
$ docker build -t e-razdumina/ML_final-project_api .
Запускаем контейнер

$ docker run -d -p 8180:8180 -p 8181:8181 e-razdumina/ML_final-project_api
Переходим на localhost:8181