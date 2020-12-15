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

