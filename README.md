python-flask-docker
Итоговый проект (пример) курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy API: flask Данные: с kaggle - https://www.kaggle.com/codebreaker619/salary-data-with-age-and-experience?select=Salary_Data.csv

Задача: Прогнозирование заработной платы людей на основе их возраста и многолетнего опыта.

Используемые признаки:

YearsExperience (float64)
Age (float64)
Преобразования признаков: ColumnSelector и OHEEncoder

Модель: RandomForestClassifier

Клонируем репозиторий и создаем образ
$ git clone https://github.com/Matvyxa/ML_Project.git
$ cd GB_docker_flask_example
$ docker build -t Matvyxa/gb_docker_flask_example .
Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

$ docker run -d -p 8180:8180  -v <your_local_path_to_pretrained_models>:/app/app/models Matvyxa/gd_docker_flask_example
