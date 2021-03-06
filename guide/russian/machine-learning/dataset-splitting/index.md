---
title: Dataset Splitting
localeTitle: Разделение набора данных
---
## Разделение набора данных

Разделение на тренировки, кросс-валидация и набор тестов являются общими передовыми методами. Это позволяет вам настраивать различные параметры алгоритма без принятия суждений, которые в точности соответствуют данным обучения.

### мотивация

Dataset Splitting возникает как необходимость устранения смещения для обучения данных в алгоритмах ML. Изменение параметров алгоритма ML для наилучшего соответствия учебным данным обычно приводит к алгоритму переобучения, который плохо работает с фактическими данными теста. По этой причине мы разделили набор данных на несколько дискретных подмножеств, на которых мы обучаем разные параметры.

#### Учебный комплект

Набор Training используется для вычисления фактической модели, которую ваш алгоритм будет использовать при работе с новыми данными. Этот набор данных обычно составляет 60% -80% от всех доступных вами данных (в зависимости от того, используете ли вы набор кросс-валидации).

#### Набор для проверки креста

Множества Cross Validation предназначены для выбора модели (обычно ~ 20% ваших данных). Используйте этот набор данных, чтобы попробовать различные параметры для алгоритма, прошедшего обучение в наборе обучения. Например, вы можете оценить различные параметры модели (полиномиальная степень или лямбда, параметр регуляризации) в наборе кросс-проверки, чтобы увидеть, что может быть наиболее точным.

#### Набор тестов

Набор тестов - это последний набор данных, который вы касаетесь (обычно ~ 20% от ваших данных). Это источник истины. Ваша точность в предсказании набора тестов - это точность вашего алгоритма ML.

#### Дополнительная информация:

*   [AWS ML Doc](http://docs.aws.amazon.com/machine-learning/latest/dg/splitting-the-data-into-training-and-evaluation-data.html)
*   [Хорошее сообщение stackoverflow](https://stackoverflow.com/questions/13610074/is-there-a-rule-of-thumb-for-how-to-divide-a-dataset-into-training-and-validatio)
*   [Учебный документ](https://www.mff.cuni.cz/veda/konference/wds/proc/pdf10/WDS10_105_i1_Reitermanova.pdf)