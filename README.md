# lessons

# Программа замены голоса
## Для пользователей
### Для установки надо перейти [Сюда_<Ссылка_не_рабочая>] (URL)
### После запуска программы рекомендуется поставить задержку(Chank) в смене голоса выше 350 ms. во избежании некорректной работы программы.

# Для разработчиков(На ходу придумываем проблемы)
# Программа работает на основе библиотеки pyaudio 
 ```
import pyaudio

CHUNK = 1024
FORMAT = pyaudio.paInt16
CHANNELS = 1
RATE = 44100

p = pyaudio.PyAudio()

stream = p.open(format = FORMAT, channels = CHANNELS, rate = RATE, input = True, frames_per_buffer = CHUNK)

frames = []

while True:
    data = stream.read(CHUNK)
    frames.append(data)
 ```
<!--CHUNK = 1024 корость задержки изменённого голоса -->

<!--RATE = 44100 RATE определяет количество образцов аудиоданных в секунду-->

<!--Количество каналов CHANNELS указывает, сколько каналов аудиоданных используется для записи. -->
- Оптимизирование программы для ПК со слабой производительностью
- Добавлением большего количества голосов
