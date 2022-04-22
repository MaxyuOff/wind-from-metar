import re
import sys

text = input()
match = re.findall(r'\d{5}MPS|AUTO|\d{5}KT|\d{5}KMH', text)

if match == []:
	print('Вы ввели неверные данные')
	sys.exit()

if match[0] == 'AUTO':
	print('AUTO (AUTO в METAR указывает на полностью автоматизированный отчет без вмешательства человека)')
match2 = re.findall(r'^\d{3}', match[0])
if 'MPS' in match[0]:
	match3 = re.sub(r'MPS', 'м/с', match[0])
	match4 = re.findall(r'\d{2}м/с$', match3)
	print('Направление ветра - ' + match2[0] + ', Скорость - '+ match4[0])
elif 'KMH' in match[0]:
	match3 = re.sub(r'KMH', 'км/ч', match[0])
	match4 = re.findall(r'\d{2}км/ч$', match3)
	print('Направление ветра - ' + match2[0] + ', Скорость - '+ match4[0])
elif 'KT' in match[0]:
	match3 = re.sub(r'KT', 'узл', match[0])
	match4 = re.findall(r'\d{2}узл$', match3)
	print('Направление ветра - ' + match2[0] + ', Скорость - '+ match4[0])
