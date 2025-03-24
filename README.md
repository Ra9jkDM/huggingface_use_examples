Примеры работы с моделями с сайта huggingface.co
----

- huggingface.ipynb - использование разных моделей с ```https://huggingface.co/```
- promt_engineering.ipynb - для генерации текста и ответа на вопросы используется модель ```microsoft/Phi-3-mini-4k-instruct```, для перевода ответов с ru на en и наоборот используются 2 модели: ```Helsinki-NLP/opus-mt-ru-en``` и ```Helsinki-NLP/opus-mt-en-ru```. Функция ```pred(msg, temperature=None, top_p=None)``` автоматически переводит запрос на английский язык и возвращает результат на русском языке
    - msg: 

            [
                {'role': 'system', "content": '''Ты — опытный Python-разработчик.'''},
                {"role": "user", "content": '''Напиши функцию сложения двух чисел, ...'''}, # Вопрос
                {"role": "assistant", "content": '''def sum(a, b): # функция сложения 2-х чисел'''}, # Пример ответа
                {"role": "user", "content": 'Новый вопрос'}
            ]

- BERT_Train.ipynb - бообучение BERT модели для определения тональности (input - text, output - Positive, Neutral, Negative). Код сохранения и загрузки токенизатора и модели
- Text Clustering and Topic Modeling.ipynb - кластеризация текстов с помощью нейронной сети BERTopic
- pyvis.ipynb - работа с графами (data: data/facebook_combined.txt and data/employer_matching.xlsx)
- NER_simple.ipynb - выделение сущностей(PER, LOC, ORG) из текстов и построение графов
