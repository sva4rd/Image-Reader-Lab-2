# IMAGE READER

__Image Reader__ — это приложение, которое считывает из графического файла/файлов/архива файлов основную информацию об изображении:

* имя файла

* расширение изображения

* размер изображения в битах

* размер изображения в пикселях

* глубину цвета изображения

* разрешение изображения (dpi)

Обрабатываемые форматы файлов: _jpg, gif, tif, bmp, png, pcx, jpeg_.

Обрабатываемый формат архива — _zip_.

Приложение разработано с помощью кроссплатформенной IDE — Qt Creator (версия: 6.1.3). Адаптировано для ОС Windows.

Приложение использует класс `QZipReader` и стандартные библиотеки Qt: `QtWidgets`. Документация по данной среде разработки и ее библиотекам доступна на ее [веб-сайте](https://doc.qt.io).
___
Функционал приложения представляет из себя считывание информации об изображениях и ее представление в виде таблицы.

Базовый класс приложения — `InfoReader`. Его функционал: 

* выбор файла/файлов/архива файлов при помощи класса `QFileDialog`

* создание временной директории и распаковка архива в нее при помощи классов `QDir` и `QZipReader`

* вывод предупреждения при отсутствии файлов нужного формата в архиве при помощи класса `QMessageBox`

* считывание данных файла при помощи классов `QFileInfo` и `QImage`

* представление и возможность сортировки данных при помощи классов `QTableWidget` и `QTableWidgetItem`

___
Недостатки приложения: невозможность обработки zip-архива, который сделан при помощи WinRAR.
