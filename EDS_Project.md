<table width="1000" border="1">
<thead>
  <tr>
    <td rowspan="3"><img width="300px" src="https://github.com/user-attachments/assets/b469980a-8e2c-4d9c-b48f-cee80a543b46"></td>
    <td colspan="2" width="700"><p align="center"><b> Проект <br> Модуль "Аварийно-диспетчерская служба" (АДС) </b></p></td>
  </tr>
  <tr>
    <td>Дата</td>
    <td> ... .04.2025</td>
  </tr>
  <tr>
    <td>Версия</td>
    <td>1.0</td>
  </tr>
</thead>
</table>


## Содержание
[1. Требования (по Вигерсу)](#title1) <br> 
[2. Бизнес-требования](#title2)</br>
[3. Контекстная диаграмма](#title3)</br>
[4. Пользовательские сценарии](#title4)</br>
&nbsp; [4.1 ...](#title4_1) <br>
&nbsp; [4.2 ...](#title4_2) <br>
<br>



## <a id="title1"> 1. Требования (по Вигерсу) </a>

### Бизнес-требования

- *Система* должна консолидировать бизнес-процессы *АДС* в единое информационное пространство;
- *Система* должна увеличить скорость обработки *Заявок* от *Пользователей*.

### Пользовательские

- *Пользователь* с ролью *Диспетчер* должен иметь возможность работать с разными типами *Заявок*;
- *Пользователь* с ролью *Администратор работ* должен иметь возможность изменять атрибуты *Заявок*;
- *Пользователь* с ролью *Исполнитель работ* должен иметь возможность просмотра *Заявок*.

### Системные
- В *Системе* должна быть реализована возможность управления *Заявками*;
- В *Системе* должна быть реализована возможность хранения *Дополнительных материалов* к *Заявкам*.

### Ограничения
- *Система* должна иметь совместимость с сертифицированными операционными системами;
- Расчетное время выполнения *Заявки* не должно превышать срок описанный в НПА (бизнес-правило).


## <a id="title2"> 2. Бизнес-требования </a>

- *Система* должна обеспечить круглосуточную регистрацию и отработку *Заявок*;
- *Система* должна обеспечить предоставление ответа на *Заявку* не позднее 10 минут с момента поступления;
- *Система* должна обеспечить ведение журнала учёта *Заявок* в ГИС ЖКХ;
- В случае аварийных повреждений внутридомовых инженерных систем *Система* должна обеспечить информирование органа местного самоуправления муниципального образования, на территории которого расположен многоквартирный дом (МКД), о характере повреждения и планируемых сроках его устранения;

### Бизнес-правила
[см. Постановление Правительства РФ от 15.05.2013 N 416](https://docs.cntd.ru/document/499020841)

## <a id="title3"> 3. Контекстная диаграмма </a>

### "Классическая"

![АДС_Контекстная_диаграмма](https://github.com/user-attachments/assets/43203029-4abc-4fcc-b8f4-87c400620a40)

[см. в Google Draw](https://docs.google.com/drawings/d/1WK4C3f7dXRz46UVjHfCQ6sbBk8tnQkyMIweeT2CtFcc/edit?usp=sharing)

### В нотации С4 
> **Заявитель** не отображается т.к. не взаимодействует с системой напрямую. Легенда выключена

![](https://www.plantuml.com/plantuml/svg/ZLPVRzDM57_tfxYh9YNDiW2YUvaGecghCQbYrQ12aof5NkDIYzI9ObUZRssw3L0OHHjYQ9lO-h1tDqrR9mtDLxZt6-rtVdOyXq2nH8Xpxxddz-USUznRVc2tWksjkcLzudhhzUsQeswiprrPcAikDBp0UHHKcjYz-TvTs_MSLhAlCX6DZGrttRcowZij_ygsdyPy8ABXrP6e-l70hSRtRdqYq5gU_-wRrNlLvVaxYtSNvbUMYhDM8Lcx__MzszNbfQ-MxYnYrIheaJxN5wQjt-B_FTCspnIMBfG-nkzT7UapVQ7VOZz4N6Jv3rslQRViBUKrQexlDDNrgvSawUeJiulrI0-c4hHixw4a-E8gQ03a670XCaJcCUAxU3xHGsMUO04ym65VcL-G0wluW1BET5KHtoTw8AXA7-7nJA21YaUoqU5i1lI7bjsyxzQ2JNLDS0Ctg3jA7m832PWwLFg5VgaFrppz1wMd-P4lD0TAzy0cJEWEUMBDAoxCLQvLakQ0svkENNDQQiL-uAZRVBOA6ur6W6-elIuSmpW1kBRbwKi5ZyxDS_Euh60w081-BXhn6IWTANoFX6ZiaZwf81D_9-Um1h_Q5JseA4ISm7ucmZAEzY2ZJnbTio-WokpX7n9GDoBwE8Nm4Ifse8Tctpot2Ylei8PNNNeK5ErciwnczEzY0ZBp782VpSZgtqG8cRTKqc_qaMWoJn4Y5JqebHG8eYoi49MVmTiEMB8r08nS7PZ-1dRiiSodupOWLsb1REsRlHdqRSohMFF9wILj6D5Aef3JFyXnB3iqE8Ai_SluwGlklIjGR2kLW9b0shKjIVu2SeVIbYb0A1q9w4jt0P3jDjC1CBg7_i5BtZPeJg2ZiiBEHAEOpYovf6LPHy-r1FCrBK0QeAR5MVDu-4Z4aTclfZEEWafQcmQOZfAzh0a3GQRy32H63H6dIQSDKKHMRiwkUH-Ae-EiLrjQmVoap8ySEaEfyDqTFt2sYlwEJqDvKEP0NwxrvxhtRibv3q1QIVUWqgVG58grlCspGefbJzLA-7jwGQfTLaWmOcYN7S3xDkMBZkXCp9JE-6xWb6TkV9ePtZSL7FYJKqtwlQzuzeZD0VBO91_v5SzPfLzXylnBmeUcdKx5dx5Lc3HYIczXaWvU3SA6RuWCcxy01mAi2So4Ceh50dwSZkMkUGNm89ffSyA7Gk-pGjn7a84LtQEDXOmnaP2miZIQzWx5yFvtfN0e_JYZwJ3VwsJISgn2QqHbgCEuGMH0OIKpgR5GLg8Qcqaz9kLxZS3Tc8A6LrsSx-7yC2rkFziVo9zQsuMgC_JgzFGwPqsdPzWaXmSk-_St23pCLlOLbEt6Hx9zXL7FdlheIq8SxAMk8DdJySkNKoEDwd7i7JDEzlH8fM_g9sFn5S1zwzJZ4O-PcXqdlBZnv4n66qbZHv9sqvQEbq7z_qno6ov9jHa4JN_Y01erHxmbyMI9uP0ZNi9ZAldZoKJ2Sx6fBlAra3z_TJMUstcFn9ePYuRAgO7Xl7lvmzChaqlsCby5-KNSShoQ_5Nz7m00)

<details><summary> Развернуть код </summary>

```plantUML
@startuml

!include <c4/C4_Context.puml>
!include <c4/C4_Container.puml>
 
!include <office/Users/user.puml>
!include <office/Users/online_user.puml>
!include <office/Users/mobile_user.puml>

LAYOUT_LANDSCAPE()
'LAYOUT_WITH_LEGEND()

'плотность по горизонтали
skinparam nodesep 30
'плотность по вертикали
skinparam ranksep 50

'ограничиваем ширину элементов (текст без переноса)
skinparam wrapWidth 150

title Система АДС\nКонтекстная диаграмма \n(C4.1.Context)
'header Page Header
'footer


'3 параметра: ключ, заголовок и описание.

'исключим т.к. не взаимодействует с ситемой напрямую
'Person_Ext(app, "Заявитель", "Подает **Обращения** через разные каналы\nОтслеживает статус")

Person(dsp, "Диспетчер", "Регистрирует **Обращения** от **Заявителей**")
Person(adm, "Администратор", "Администратор **Системы** \n(Пользователи, Параметры)")
Person_Ext(contr, "Исполнитель\nработ", "Выполняет работы по **Заявкам**")
Person_Ext(user, "Пользователь", "(роль)\nПользователь отчетных форм")

System(sys, "Аварийно-диспетчерская служба\n(АДС)", "Обработка **Обращений**, управление **Заявками**")
System_Ext(site,"<$online_user> \nЛичный кабинет\nабонента ЖКХ", "Страница 'Аварийная служба'")
System_Ext(mob,"<$mobile_user> \nМобильное приложение\n'Квартплата+'", "Вкладка 'Заявки'")


System_Ext(pay, "Сервис оплаты", "Интеграция с учетной системой, банками")
System_Ext(notify, "Сервис уведомлений", "Обратная связь через различные каналы")
System_Ext(gis, "ГИС ЖКХ", "Журнал **Заявок**")


'3 параметра: ключ одной сущности, ключ другой тип отношений.

'Rel(app, dsp, "Использует", "Аналоговый канал")
'Rel(app, site, "Использует", "https")
'Rel(app, mob, "Использует", "https")

Rel(dsp, sys, "Использует", "https")
Rel(site, sys, "Использует", "https")
Rel(mob, sys,"Использует", "https")

Rel_D(adm, sys, "Использует", "https")
Rel_U(contr, sys, "Использует", "https")


Rel(sys, gis, "Использует", "https")
Rel(sys, pay, "Использует", "https")
Rel(sys, notify, "Использует", "https")

Rel_L(user, sys, "Использует", "https")

@enduml```

</details>




## <a id="title4"> 4. Пользовательские сценарии </a>

### Таблица

|п/п|Поле 1|Поле 2|Описание| 
|---|---|---|---|
|---|---|---|---|

### Диаграмма
<details><summary>Развернуть код </summary>
</details>




