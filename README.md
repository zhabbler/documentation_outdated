# <img align="right" src="https://zhabbler.ru/assets/images/icon.png" alt="Жабблер" title="Жабблер" width="12%">documentation
API документация Жабблера
# Как вызвать функцию?
Чтобы вызвать функцию, необходимо перейти по URL адресу: ```https://zhabbler.ru/public_api/?type={НАЗВАНИЕ ФУНКЦИИ}```.<br>
К примеру, чтобы вызвать функцию ```GetAllPosts```, необходимо перейти по этому URL: ```https://zhabbler.ru/public_api/?type=GetAllPosts```.
# Функции
## Функции с постами
### GetAllPosts
Нет параметров.<br>
Функция для получения всех новых постов.<br>
Пример ответа по URL:```https://zhabbler.ru/public_api/?type=GetAllPosts```<br>
```json
[
  {
    "id":"833ddf021ed4618d0863f322610a4335de73bf352e1594932c10e16649d652f99469950b",
    "nickname":"zhabbler",
    "profile_pic_url":"{длинный url}",
    "title":"",
    "uploaded":"2023-09-12",
    "content":"Ква.",
    "likes":14
  }
]
```
### GetPostsByNickname
Параметры: ```nickname```.<br>
Функция для получения всех постов от пользователя.<br>
В параметре ```nickname``` необходимо ввести никнейм пользователя.<br>
Пример ответа по URL:```https://zhabbler.ru/public_api/?type=GetPostsByNickname&nickname=zhabbler```<br>
```json
[
  {
    "id":"833ddf021ed4618d0863f322610a4335de73bf352e1594932c10e16649d652f99469950b",
    "nickname":"zhabbler",
    "profile_pic_url":"{длинный url}",
    "title":"",
    "uploaded":"2023-09-12",
    "content":"Ква.",
    "likes":14
  }
]
```
### GetRepost
Параметры: ```id```.<br>
Функция для получения всех репостов с поста.<br>
В параметре ```id``` необходимо ввести id поста.<br>
Пример ответа по URL:```https://zhabbler.ru/public_api/?type=GetRepost&id=0878995fc083195f1eb6bd94f87a00f5b8d046479b6c5928e0c52942f738040fa71b4e65```<br>
```json
[
  {
    "id":"55a138cdb14a75ec38d5c8b16b9273ae18dcd6591335942758232eb32febea7f3550d219",
    "repostTo":"0878995fc083195f1eb6bd94f87a00f5b8d046479b6c5928e0c52942f738040fa71b4e65",
    "nickname":"zhabbler",
    "profile_pic_url":"{длинный url}",
    "title":"",
    "uploaded":"2024-01-01",
    "content":"Команда Жабблера поздравляет вас с Новым годом!<br>Желаем вам счастья, больше радости в жизни, и чтобы вы больше тратили времени на себя и на своё любимое хобби.<br>С Новым годом!",
    "likes":2
  }
]
```
### GetPost
Параметры: ```id```.<br>
Функция для получения информации поста.<br>
В параметре ```id``` необходимо ввести id поста.<br>
Пример ответа по URL:```https://zhabbler.ru/public_api/?type=GetPost&id=833ddf021ed4618d0863f322610a4335de73bf352e1594932c10e16649d652f99469950b```<br>
```json
[
  {
    "id":"833ddf021ed4618d0863f322610a4335de73bf352e1594932c10e16649d652f99469950b",
    "nickname":"zhabbler",
    "profile_pic_url":"{длинный url}",
    "title":"",
    "uploaded":"2023-09-12",
    "content":"Ква.",
    "likes":14
  }
]
```
### GetPostsPhotos
***Внимание!*** **Скоро данная функция будет отключена.**<br>
Параметры:```id```<br>
Функция для получения фотографий из поста.<br>
В параметре ```id``` необходимо ввести id поста.<br>
Пример ответа по URL:```https://zhabbler.ru/public_api/?type=GetPostsPhotos&id=aaa47d4731681282041d5abb3d86e4029cc6a857642ea9640e639d2463e402fd6fa3cdde```<br>
```json
[
  {
    "url":"{длинный url}",
    "post_id":"aaa47d4731681282041d5abb3d86e4029cc6a857642ea9640e639d2463e402fd6fa3cdde"
  },
  {
    "url":"{длинный url}",
    "post_id":"aaa47d4731681282041d5abb3d86e4029cc6a857642ea9640e639d2463e402fd6fa3cdde"
  }
]
```
## Функции с комментариями
### GetComments
Параметры:```id```<br>
Функция для получения комментариев из поста.<br>
В параметре ```id``` необходимо ввести id поста.<br>
Пример ответа по URL:```https://zhabbler.ru/public_api/?type=GetComments&id=aaa47d4731681282041d5abb3d86e4029cc6a857642ea9640e639d2463e402fd6fa3cdde```<br>
```json
[
  {
    "nickname":"nickname",
    "profile_pic_url":"{длинный url}",
    "content":"Превосходно."
  }
]
```
