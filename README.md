## Для запуска сервера потребуется настроить виртуальное окружение, в котором будет выполняться программа

### Создание виртуального окружения на рабочей Ubuntu 18 с установленной Anaconda и pip:

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

Распознаватель запущен и работает при получении картинки с паспортом по адресу url 'http://localhost:2020/api/test/passrecogn' (http://0.0.0.0:2020/ или http://127.0.0.1:2020)
