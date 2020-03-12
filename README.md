# -
Простой говорящий робот
# Для первой бибилотеки прописываем также псевдоним
import os
import time
import pyttsx3
import datetime
import speech_recognition as sr
import os
import sys
import webbrowser


engine = pyttsx3.init()

engine.setProperty('rate', 125)#Скорость
engine.setProperty('volume', 0.9)#Громкость

ru_voice_id = "russian"

engine.setProperty('voice', ru_voice_id)

engine.say('Привет.Мой создатель!!!')
print('Привет.Мой создатель!!!')
engine.say('Вот что я могу:')
print('Вот что я могу:')
engine.say('Шутить')
engine.say('Рассказать историю')
print('2.Рассказать историю')
engine.say('Петь')
print('3.Петь')
engine.say('Говорить время')
print('4.Время')
engine.say('Открыть браузер')
print('5.Открыть браузер')
engine.say('Открыть шахматы')
print('6.Открыть шахматы')

engine.runAndWait()

engine.say('Введите число')
engine.runAndWait()
name = input('Введите число 1,2,3,4,5,6,7...')
if int(name) == 1:
	#Шутка
	print('Вот моя шутка:Я не умею шутить.Ха-ха это очень смешно')
	engine.say('Вот моя шутка.')
	engine.say('Я не умею шутить.')
	engine.say('Ха-ха это очень смешно!!!')
elif int(name) == 2:
	#история
	print('Вчера меня делал мой создатель.')
	print('И он очень замучился!!!')
	engine.say('Вчера меня делал мой создатель.')
	engine.say('И он очень замучился!!!')
elif int(name) == 3:
	#Петь
	print('Ляляляляляля.Я яяяяя')
	print('Хорошая песня')
	engine.say('Ляляляляляля.Я яяяяя')
	engine.say('Хорошая песня')
elif int(name) == 4:
	# сказать текущее время
    now = datetime.datetime.now()
    engine.say("Сейчас " + str(now.hour) + ":" + str(now.minute))
    print("Сейчас " + str(now.hour) + ":" + str(now.minute))
elif int(name) == 5:
	#Открыть браузер.
	engine.say('Открываю браузер')
	os.system('/usr/bin/firefox')
elif int(name) == 6:
	#Открыть шахматы
	engine.say('Открываю шахматы')
	os.system('/usr/games/xboard')
elif int(name) == 7:
	#Завершить
	print('Пока.')
	engine.say('Пока')
else:
	print('Такой команды нет!!')
	engine.say('Извни такой команды нет')

engine.say('Пока')
print('Завершенно')
engine.runAndWait()
