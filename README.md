# ulog stdout

Слушает что присылает ulog server и выводит в стандартный вывод.

## Настройка порта

Для настройки порта для прослушки логов выполняем с 1 аргументом: номер порта.

## Настройка вывода

В добавок ко всему можно настроить и формат вывода сообщений.
Для указания формата запускаем с номером порта и строкой формата в двойных кавычках.

По умолчанию выбран формат `[%i][%t][%l]: %m`

### Описание ключей формата

  * **%i** - порядковый номер сообщения в текущей сессии для сервера
  * **%t** - время (тип *ulong*) в формате time(NULL) * 1000 + ms (где ms - трехзнычное число миллисекунд)
  * **%l** - тип сообщения. Строки Log, Error, Exception, Assert, Warning
  * **%m** - тело сообщения
  * **%s** - стектрейс для текущего сообщения