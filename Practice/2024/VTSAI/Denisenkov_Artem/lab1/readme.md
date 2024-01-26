## Обучение с подкреплением в окружении LunarLander

Студент гр. 4215 Денисенков Артем

Для выполнения работы была выбрана среда [LunarLander](https://gymnasium.farama.org/environments/box2d/lunar_lander/)

#### Описание среды

##### Action space

0. Ничего не делать
1. Поворот по часовой
2. Запуск основного двигателя
3. Поворот против часовой

##### Observation space

8-ми мерный вектор

Координаты X и Y, линейные скорости по осям, угол, угловая скорость, касается ли каждая из опор земли.

##### Параметры

* Continuous - при True action_space будет Box
* Gravity - Сила притяжения
* Enable wind - наличие ветра (выключен, для упрощения обучения)
* Turbulance power - Случайные изменения угла

#### Обучение

Изначально мы вызываем метод learn() для обучения модели. Но при timestamp = 500000 обучение стало эффективнее, а для ускорения стали использовать GPU

#### Результаты

После обучения агент научился успешно садиться на поверхность