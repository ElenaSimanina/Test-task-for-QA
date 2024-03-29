   # **Задача №2.**
***Вы QA в приложении заказа еды и только что узнали, что пользователи больше не получают push уведомления. Каковы ваши дальнейшие действия по локализации ошибки?***

Для локализации ошибки первоначально нужно вопроизвести проблему, т.е. нужно воспроизвести баг снова при тех же условиях. Если ошибка
не        повторилась при очередном тестировании, то нужно разобраться, точно ли были соблюдены все действия и шаги воспроизведения, приведшие к этому результату. Возможно, дефект появляется только при первоначальной загрузке системы (при первом использовании). Для того, чтобы более точно определить условия воспроизведения ошибки, необходимо эту ошибку локализовать.  Если проблема подтвердилась, необходимо собрать максимальное количество информации о ее воспроизведении, выявить причины возникновения дефекта.

***Чтобы локализовать баг, необходимо собрать максимальное количество информации о его воспроизведении:***
- Выявить причины возникновения дефекта;
- Проанализировать возможность влияния найденного дефекта на другие области - проверить, затрагивает  ли найденный дефект  другие компоненты системы; 
- Исследовать окружение - необходимо воспроизвести баг в разных операционных системах (iOS, Android, Windows и т.д.) и браузерах (Google Chrome, Mozilla, Internet Explorer и др.). При этом нужно проверить требования к продукту, чтобы выяснить, какие системы должны поддерживаться. Некоторые приложения работают только в определенных ОС или браузерах, поэтому нет нужды проверять другие варианты. 
- Нужно проверить воспроизведение бага на различных устройствах, при этом также нужно проверить  требования к ПО, в которых должно быть указано, с какими устройствами наше ПО совместимо.
- Проверить в разных версиях ПО - иногда тот или иной баг воспроизводится в одной версии продукта, но не воспроизводится в другой. Этот атрибут обязательно необходимо указывать в баг-репорте, чтобы программист понимал, в какой ветке нужно искать проблему.
- Для локализации проблемы также нужно проверить, не находится ли ресурс в "черном списке", возможно сайт был взломан и с него происходила рассылка спама. Возможно, мы "перестарались" с рассылкой, и большинство получателей отметили наши сообщения, как спам - от этого наша репутация, как отправителя, стала низкой. Сервер или IP-фдрес, на котором расположен наш сайт, имеет низкую репутацию. 
- Нужно посмотреть состояние системы, если есть дашборды grafana,  которая показывает - как уходят нотификации пользователям (если есть доступ).  

Доказательства воспроизведения бага нужно обязательно  фиксировать при помощи логов, скринов или записи экрана. Все найденные дефекты
обязательно нужно задокументировать, чтобы каждый задействованный на проекте специалист мог получить инструкции по воспроизведению обнаруженного дефекта и понять, насколько это критично. Дефект, который не задокументирован – не найден! 

Когда вся необходимая информация собрана, а баг локализован, можно приступать к оформлению баг-репорта. Чем точнее описание бага, тем меньше времени нужно для его исправления.  Необходимо очень подробно описать все условия и шаги, чтобы разработчик смог проверить и устранить ошибку
    
После составления баг-репорта и формирования задачи для разработчиков, нужно дождаться  исправленной версии приложения и провести тестирование на исправление бага. 
 