# SF_Project_2
Учебный проект на Python.
В этом проекте я провел один из важнейших видов исследований в продуктовой аналитике — анализ поведения пользователей в продукте.
Продуктом выступает вымышленная мобильная игра, которая является сборником вопросов в различных форматах и темах, на которые игрокам нужно давать ответы. Игра одиночная, то есть каждый игрок отвечает на вопросы самостоятельно.

Игра состоит из следующих этапов:

Регистрация (registration) — это обязательный этап. Без регистрации пользователь не может пройти на следующие этапы работы с приложением.

Старт обучения (tutorial_start) — опциональный этап. Пользователь после регистрации может перейти к обучению работе с приложением, а может и не перейти. При этом вернуться к обучению можно в любой момент. А ещё можно пройти обучение несколько раз.

Завершение обучения (tutorial_finish) может произойти только в случае, если ранее произошло событие «Старт обучения», но при этом пользователь может не завершить обучение.

Выбор уровня сложности вопросов (level_choice) — это обязательное событие, которое нужно для того, чтобы перейти к выбору пакетов вопросов. Таким образом, пользователь может не пройти обучение или даже не начинать его, но прежде чем начать отвечать, он обязан выбрать уровень сложности.

Выбор пакетов вопросов (pack_choice, другое название training_choice) — это этап, на котором пользователь выбирает себе бесплатный набор пакетов вопросов, на которые он будет отвечать.

Покупка платных пакетов вопросов — это факт совершения оплаты за вопросы, которые не доступны в списке бесплатных вопросов.

Из данных есть 2 csv-файла: 7_4_Events и purchases.

Формализованные задачи выглядели так:
1. Проверить, отличается ли время прохождения различных этапов для пользователей, которые прошли обучение, от пользователей, не начинавших обучение. Насколько обучение сокращает время прохождения этапов?

2. Посмотреть, существует ли зависимость между вероятностью оплаты вопросов и количеством обучений, которые начинал или завершал пользователь. Нужно доказать, что успешное обучение само по себе влияет на оплату, и без разницы, каким этапом оно шло.

3. Дополнительная задача. Как часто пользователи начинают обучение после того, как они выбрали уровень сложности? Это позволит нам понять, насколько прозрачен процесс взаимодействия с игрой: если пользователи после выбора уровня сложности обращаются к обучению, значит, работа с приложением непонятна.
