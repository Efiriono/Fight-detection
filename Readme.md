Fight Detection App
Приложение для обработки видео с использованием модели YOLOv8 Pose. Оно позволяет детектировать и отслеживать ключевые точки людей на видео и сохранять результаты в виде выходного видео и JSON-файла с координатами.

Функциональность
Графический интерфейс на основе PyQt5 для удобного взаимодействия с пользователем.
Обработка видео с использованием модели YOLO v8 Pose.
Сохранение результатов:
Выходное видео с нанесёнными ключевыми точками.
JSON-файл с координатами ключевых точек для каждого кадра.
Загрузка и скачивание видеофайлов через интерфейс.
Установка
Клонируйте репозиторий:

git clone https://github.com/Efiriono/Fight-detection-app.git
cd fight-detection-app
Создайте виртуальное окружение:

python -m venv venv
source venv/bin/activate  # Для Linux/Mac
venv\Scripts\activate     # Для Windows
Установите зависимости:

pip install -r requirements.txt
Скачайте модель YOLO v8 Pose:

Убедитесь, что в папке проекта есть файл модели yolov8m-pose.pt.
Модель можно скачать с официального репозитория Ultralytics.
Добавьте необходимые ресурсы:

Изображения 1.jpg, 2.jpg, 3.jpg для фонового оформления интерфейса.
Шрифт PIXY.ttf для корректного отображения текста в приложении.
Запуск
Активируйте виртуальное окружение:

source venv/bin/activate  # Для Linux/Mac
venv\Scripts\activate     # Для Windows
Запустите приложение:

python main.py
Использование
Выберите видеофайл:

Нажмите на кнопку "Выберите файл" и укажите путь к видеофайлу формата .mp4 или .avi.
Начало обработки:

После выбора видео обработка начнётся автоматически.
На экране будет показан статус "В обработке...".
Сохранение результатов:

По завершении обработки появится кнопка "Скачать файл".
Нажмите на неё, чтобы сохранить результаты в папку results (будет создана в папке куда установленн объект.
Результаты:

output_video.mp4: Видео с визуализацией ключевых точек.
coordinates.json: JSON-файл с координатами ключевых точек для каждой отслеживаемой персоны по кадрам.
Пример файла coordinates.json
{
  "person_id_1": {
    "frame_0": {
      "nose": [123, 456],
      "left_eye": [120, 450],
      "right_eye": [126, 452],
      ...
    },
    "frame_1": {
      "nose": [125, 460],
      "left_eye": [122, 454],
      "right_eye": [128, 456],
      ...
    }
  }
}
Системные требования
Python 3.8 или выше
Поддержка PyQt5 и OpenCV
Модель YOLOv8 Pose (файл yolov8m-pose.pt)
