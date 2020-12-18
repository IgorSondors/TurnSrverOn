## Для запуска сервера потребуется настроить виртуальное окружение, в котором будет выполняться программа

### Требования - ОС Ubuntu с установленной Anaconda и pip

```
No LSB modules are available.

Distributor ID: Ubuntu

Description: Ubuntu 18.04.4 LTS

Release: 18.04

Codename: bionic
```

### Создание виртуального окружения:

#### Запустите терминал: ctrl+alt+T

- conda create -n ИМЯ_ВИРТ_ОКРУЖЕНИЯ python=3.7

### Упрощенная установка виртуального окружения при помощи Anaconda, pip и предустановленного apt:

- conda activate ИМЯ_ВИРТ_ОКРУЖЕНИЯ
- sudo apt-get update
- apt install swig  
- pip install jamspell  
- python -m pip install --upgrade pip setuptools  
- conda install -c anaconda tensorflow-gpu==1.15
- pip install flask
- pip install jsonpickle
- sudo apt-get install aptitude
- sudo aptitude safe-upgrade
- pip install opencv-python
- pip install easydict
- pip install glog
- pip install tqdm
- pip install python-Levenshtein

## Запуск сервера

1) Откройте терминал из папки, в которой содержится код сервера (cloud_server)

![](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-10-06.jpg)

- Кликните правой кнопкой мыши на папку, выбирите Open in Terminal

2) Введите команду в терминале

- conda activate ИМЯ_ВИРТ_ОКРУЖЕНИЯ

![Теминал должен выглядеть примерно так](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-14-32.jpg)

- Командой ls также можно из терминала увидеть содержимое папки, в которой мы находимся

![](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-15-59.jpg)

3) Запускаем сервер, прописываем в терминале

- python server.py

В терминале свидетельствует о запуске сервера такая картина 

![](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-23-45.jpg)

Распознаватель запущен и работает при получении картинки с паспортом по адресу url 'http://localhost:2020/api/test/passrecogn' (http://0.0.0.0:2020/api/test/passrecogn или http://127.0.0.1:2020/api/test/passrecogn)

4) Для проверки работы сервера можно запустить скрипт client_for_test.py, который имитирует запрос клиента на сервер в нужном формате

- Запустить можно из терминала, открытого из папки cloud_server, а также с активированным виртуальным окружением (conda activate ИМЯ_ВИРТ_ОКРУЖЕНИЯ)

- Либо запускаем client_for_test.py из текстового редактора 

![](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-35-54.jpg)

Нажимаем Дебаггинг - клиентский запрос отправлен. Через 5-10 секунд видим ответ с сервера, который пришел обратно клиенту на адрес, с которого приходил запрос

![](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-36-57.jpg)

На стороне сервера так же видим весь процесс и его логи

![](https://github.com/IgorSondors/TurnSrverOn/blob/main/screenshots/photo_2020-12-15_11-37-01.jpg)
