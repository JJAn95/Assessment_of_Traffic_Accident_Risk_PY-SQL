# Assessment_of_Traffic_Accident_Risk_PY-SQL

**Project Description**
We have received an order to create a system that could assess the risk of traffic accidents along a selected route. The risk refers to the probability of a traffic accident with any damage to the vehicle. As soon as the driver has reserved a car, got behind the wheel, and chosen a route, the system should assess the level of risk. If the risk level is high, the driver will see a warning and recommendations for the route.

The idea of creating such a system is in the preliminary discussion and development stage. There is no clear working algorithm or similar solutions in the market yet. The current task is to understand whether it's possible to predict traffic accidents based on historical data from one of the regions.

The customer's proposed solution:

- Create a traffic accident prediction model (the target value is 'at_fault' in the parties table).
- Select the type of at-fault party for the model — only the car.
- Choose cases where the traffic accident led to any damage to the vehicle, except for the type SCRATCH.
- Limit the modeling to data from 2012 — the most recent.
- A mandatory condition is to consider the age factor of the vehicle.
- Based on the model, explore the main factors of traffic accidents.

Understand whether the results of modeling and analysis of the importance of factors can help answer the questions:
- Is it possible to create an adequate system for assessing driver risk when issuing a car?
- What other factors need to be considered?
- Is it necessary to equip the car with any sensors or a camera?
- The client invites you to work with the accident database and form your ideas for creating such a system.

**Description of the Tables**
- collisions — general information about traffic accidents. It has a unique case_id. This table describes the general information about the accident. For example, where and when it happened.

- parties — information about the participants in the accident. It has a non-unique case_id, which is matched with the corresponding accident in the collisions table. Each row here describes one of the sides involved in the accident. If two cars collided, there should be two rows with the same case_id in this table. If a unique identifier is needed, it is the case_id and party_number.

- vehicles — information about the damaged cars. It has non-unique case_id and party_number, which are matched with the collisions table and the parties table. If a unique identifier is needed, it is the case_id and party_number.



## Описание проекта

Поступил заказ: нужно создать систему, которая могла бы оценить риск ДТП по выбранному маршруту движения. Под риском понимается вероятность ДТП с любым повреждением транспортного средства. Как только водитель забронировал автомобиль, сел за руль и выбрал маршрут, система должна оценить уровень риска. Если уровень риска высок, водитель увидит предупреждение и рекомендации по маршруту.

Идея создания такой системы находится в стадии предварительного обсуждения и проработки. Чёткого алгоритма работы и подобных решений на рынке ещё не существует. Текущая задача — понять, возможно ли предсказывать ДТП, опираясь на исторические данные одного из регионов.

Идея решения задачи от заказчика: 
- Создать модель предсказания ДТП (целевое значение — at_fault (виновник) в таблице parties)
- Для модели выбрать тип виновника — только машина (car).
- Выбрать случаи, когда ДТП привело к любым повреждениям транспортного средства, кроме типа SCRATCH (царапина).
- Для моделирования ограничиться данными за 2012 год — они самые свежие.
- Обязательное условие — учесть фактор возраста автомобиля.

На основе модели исследовать основные факторы ДТП.
- Понять, помогут ли результаты моделирования и анализ важности факторов ответить на вопросы:
- Возможно ли создать адекватную системы оценки водительского риска при выдаче авто?
- Какие ещё факторы нужно учесть?
- Нужно ли оборудовать автомобиль какими-либо датчиками или камерой?

Заказчик предлагает вам поработать с базой данных по происшествиям и сформировать свои идеи создания такой системы. 

### Описание таблиц

- collisions — общая информация о ДТП. Имеет уникальный case_id. Эта таблица описывает общую информацию о ДТП. Например, где оно произошло и когда.

- parties — информация об участниках ДТП. Имеет неуникальный case_id, который сопоставляется с соответствующим ДТП в таблице collisions. Каждая строка здесь описывает одну из сторон, участвующих в ДТП. Если столкнулись две машины, в этой таблице должно быть две строки с совпадением case_id. Если нужен уникальный идентификатор, это case_id and party_number.

- vehicles — информация о пострадавших машинах. Имеет неуникальные case_id и неуникальные party_number, которые сопоставляются с таблицей collisions и таблицей parties. Если нужен уникальный идентификатор, это case_id and party_number.
