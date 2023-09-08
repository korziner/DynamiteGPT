# DynamiteGPT
List articles with code and fast growing public datataset using LLM. 
AI_Talent_Hub2023 product


Demo https://2b95cc7bef0e99b5cb.gradio.live (link expires in 72 hours

Для лаб и студентов универа, подписанного на некоторые статьи.

Мне нравится вариант опенсорсного решения, не нуждающегосо в инвестициях. Надо скачать сотню-другую статей 5-детней давности и отладить промпт (или серию промптов), который лучше остальных промптов отвечает на вопрос какие из этой сотни статей содержат код для воспроизведения результатов статьи и URL быстро растущей базы омиксных данных. Из 100 варианта промптов верхний квартиль самых уловистых промптов используем в продукте.

В принципе это частично решается и регуляркой (по списку рулов можно тоже определять), но если нам нужно LLM, будет LLM:  https://github.com/imartinez/privateGPT

Модель ggml self-hosted без файнтюна для прототипа. Эксперимент с kobold.cpp - по 3 GPU научились параллелить



Сценарии - примеры промптов. Понятность - возвращает список 8 статей или не возвращает.

Выбрана 
https://huggingface.co/TheBloke/medalpaca-13B-GGML
с прицелом на мультимодальность в расширенных платных версиях опенсорсного продукта (плата за минуты имеющейся GPU Tesla): https://cambridgeltl.github.io/visual-med-alpaca/
![image](https://github.com/korziner/DynamiteGPT/assets/1572185/a46ebea8-9874-42b5-8e29-d1ba5dab0eb9)


LLM reads all articles to its vector DB:

legal alternative to sci-hub.tw is Unpaywall.

We harvest content directly from over 50,000 journals and open-access repositories from all over the world. We also use great open data from PubMed Central...
https://opendata.stackexchange.com/questions/7084/bulk-download-sci-hub-papers


It'll take up roughly 300GB of disk space.

    aws s3 sync "s3://openalex" "openalex-snapshot" --no-sign-request

https://docs.openalex.org/download-all-data/download-to-your-machine
