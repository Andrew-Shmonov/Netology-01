# Netology #

## Описание жизненного цикла задачи (разработки нового функционала) ##

Мне нравится использование принципа agile-разработки. Основная цель команды (или команд), чтобы сайт магазина работал без нареканий 25/8, посетители могли совершать покупки и тем самым предоставлять разрабочикам работу и зарплату))
Не буду приводить описание того, как планируется спринт, создается бэклог и т.д., а только цикл некой задачи внутри или вне спринта.

### Собственно, сам цикл: ###

### 1. Создаётся задача. ###
Прилетевшая задача описывается максимально подробно, насколько это возможно на данном этапе и записывается в какую-либо "систему отслеживания" будь то хоть магнитная доска, хоть специализированное ПО.

### 2. Определение ценности задачи. ###
Задача прилетает к разработчику НЕ напрямую, в обязательном порядке она проходит через некое ответственное лицо, к примеру, продуктового менеджера, котрый может оценить приоритетность, стоимость этой задачи. Часто решение принимается при участии команд разработки, посредством совещания, когда компетенция продуктового менеджера не поможет выставить хоть какую-либо объективную ценность задачи. Под ценностью задачи здесь понимается влияние на работу сайта интернет-магазина и определение категории задачи. К примеру, это может быть критический баг, который не дает совершать покупки и владелец бизнеса теряет деньги и репутацию, либо это может быть крутая фича, которая по предварительным "тестам" будет приносить +100500% прибыли.

### 3. Обсуждение задачи. ###
Как только определили ценность задачи начинается этап обсуждения. Уже на этих этапах может требоваться помощь devops, как минимум, в плане высказывания своего мнения. Во время обсуждения шаблонно определяется:
- Сложность задачи (требуется ли разбить задачу на 2 подзадачи или на 102 и распределить между командами)
- Что потребуется сделать, чтобы выполнить задачу
- Требующиеся для выполнения задачи специалисты: разработчики, дизайнеры, аналитики или, как в нашем случае, devops (так же можно предварительно закрепить определенных людей за задачей)
- Определяется некая условная стоимость задачи
- По необходимости происходит переоценка ценности задачи (задача может переместится в системе трекинга задач)

### 4. Работа над задачей. ###
Начинается работа над задачей. Здесь, если это требуется, уже непосредственно участвует devops, то есть создает инфруструктуру для разработки, тестировщиков, чтобы они смогли выполнить задачу в срок. К примеру, если сайт вдруг решил выполнить "переезд" на другую базу данных, подготовить разрабочикам и тестировщикам развертывание серверов, где непосредственно будет происходит разработка и тестирование. (По уму это отдельная задача, но в рамках выдуманной вселенной сойдет). По сути участие devops в такого рода задачах заключается в поддержании, улучшении или развитии инфрастурктуры.

### 5. Тестирование. ###
На этом этапе тестировщики ищут баги, которые в случае обнаружения могут записывать в отдельную систему трекинга багов и передавать разработке для правок. Участие devops аналогично п.5

### 6. Задача готова. ###
Задача выполнена. Теперь новую фичу можно выкатить на "боевой" сервер, но конечно же, сначала все изменения идут на стейдж-сервера, где в очередной раз тестируются и в случае удачного теста попадают на продуктовые сервера. Devops, опять же, обязан создать максимально оптимизированные механизмы обновления поддерживать их, не забывая о развитии и отказоустойчивости, а так же безопасности. Гораздо лучше, если обновление происходит бесшовно и покупатель не заметил никаких проблем во время работы с сайтом, нежели если сервера упали на пол дня с надписью: "сорян, у нас тех работы".

### Резюмируя: ### 
От devops требуется на начальных этапах обсуждения высказать свое мнение по поставленной задаче на уровне своей компетенции, на этапах разработки и тестирования подготавливать разрабочткам инфраструктуру, механизмы и инструменты для работы над задачей. На этапе обновления продуктовых серверой создать максимально опитимзированный механизм для бесшовных обновлений. Бонусом на всех этапах думать над улучшением, возможнсти оптимизации, автоматизации процессов. Заботится о безопасности, в случае отсутствия отдельного специалиста, да и при его наличии тоже не забывать. Создавать безотказность работы всей инфраструктуры и продуктовых серверов. Разрабатывать или находить лучшие инструменты, которые могут быть быть полезны в работе, чтобы интернет-магазин и его разарботка "шагали в ногу со временем".
