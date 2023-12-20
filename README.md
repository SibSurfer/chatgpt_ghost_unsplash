# How to use:
+ Чтобы пользоваться этим скриптом, вам достаточно скачать (командой `pip install <your library>`) библиотеки `requests`, `pyjwt`, `openai` ([ссылка](https://platform.openai.com/docs/api-reference/introduction?lang=python) на источник), `python-unsplash` ([ссылка](https://github.com/yakupadakli/python-unsplash) на источник)
+ Также вам нужно заполнить следующие поля:
    + Ваш ключ от ChatGPT API: поле `client.api_key` в файле - вот [здесь](https://platform.openai.com/api-keys) его можно создать 
    + Сcылка на ваш Ghost instance и ключи к нему: поля `ghost_url`, `AdminAPIKey`, `ContentAPIKey` - [здесь](https://play-ghost.intra.nocloud.today/ghost/#/settings/integrations) вы должны нажать кнопку `Add custom integration`, чтобы получить эти ключи
    + Ключи для Unsplash API: `client_id` (это значение `Access Key` в настройках вашего Unsplash приложения), `client_secret` (значение `Secret key`), `redirect_uri` вот [здесь](https://unsplash.com/oauth/applications) вы можете создать свой Unsplash App и в его настройках можно найти эти ключи
    
В целом на этом всё :) 

Я запускаю ее в терминале Ubuntu командой `python3 <path-to-file>/<file.py>` либо с помощью VSCode

P.S.: иногда генерация запросов к картинке не очень хорошо работает из-за встроенного в сайт Unsplash поиска по картинкам.

Варианты запросов к chatgpt на которых работает неплохо:
```
query = answer_from_AI(f'describe this article using no more than four words  {generated_text}')
# генерируем запрос, выделяя ключевые слова из текста
```
```
query = answer_from_AI(f'reduce this sentence to four words {article_name}') # генерируем запрос, 
сокращая название поста до нескольких слов
```
Обычно, если сокращать количество ключевых слов до 3-5, получается неплохо.


