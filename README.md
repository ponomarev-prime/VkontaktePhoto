![](vk_photo_title.png)
---
## VK_Photo_API

### VK_SAVED_IMAGES.py

Скрипт `VK_SAVED_IMAGES.py` преднозначен для сохранения фото из альбома "Сохранённые фотограйии".

Подготовка: Создать `.venv`: `python3 -m venv .venv` и установить модули `python -m pip install -r requirements.txt`.

Для работы скрипта нужно создать файл `config.ini` со следующим содержанием:
```
[auth]
VK_USER_ID = [ид аккаунта пользователя ВК]
VK_TOKEN = [токен]
VK_APP_ID = [ид приложения ВК]

[path]
SAVED_PHOTO_FOLDER = SAVED_PHOTO/
JSON_FOLDER = json/
```
Заполняем поля:

1. Получаем `ид аккаунта пользователя ВК`: для этого нужно скопировать ид своего аккаунта.

2. Получаем `ид приложения ВК`: для этого нужно создать приложение в ВК.

3. Получаем `токен`: для этого нужно перейти по ссылке https://oauth.vk.com/authorize?client_id=5490057&display=page&redirect_uri=https://oauth.vk.com/blank.html&scope=friends&response_type=token&v=5.52 предварительно заменив `5490057` на `ид приложения ВК`

В дире `JSON_FOLDER` пожно найти ответ на запрос `getAlbums` и список ссылок на фото в разном разрешении.

В дире `SAVED_PHOTO_FOLDER` будут скаченные фотографии.