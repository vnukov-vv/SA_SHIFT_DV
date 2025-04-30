<table width="1000" border="1">
<thead>
  <tr>
    <td rowspan="3"><img width="300px" src="https://github.com/user-attachments/assets/b469980a-8e2c-4d9c-b48f-cee80a543b46"></td>
    <td colspan="2" width="700"><p align="center"><b> Проект <br> Модуль "Аварийно-диспетчерская служба" (АДС) </b></p></td>
  </tr>
  <tr>
    <td>Дата</td>
    <td> 30.. .04.2025</td>
  </tr>
  <tr>
    <td>Версия</td>
    <td>1.0</td>
  </tr>
</thead>
</table>

### Работу выполнили 
|Подразделение| Фамилия И.О.|
|---|---|
|Группа 1. Модуль "Прием и обработка заявок"|*Внуков В.В.*|
|Группа 2. Модуль "Личный Кабинет"|*Мельник А.А.*|
|Группа 3. Модуль "Отчеты"|*Царев Д.И.*|


## Содержание
[1. Общая информация](#title1) <br> 
&nbsp; [1.1 Термины и определения](#title1_1) <br>
&nbsp; [1.2 Ссылки на существующую документацию, НПА](#title1_2) <br>
&nbsp; [1.3 Контекстные диаграммы](#title1_3) <br>
[2. Требования (по Вигерсу)](#title2) <br> 
[3. Бизнес-требования](#title3)</br>
[4. Архитектура Системы (HLD)](#title4)</br>
[5. Пользовательские сценарии. Use Cases диаграммы](#title5)</br>
&nbsp; [5.1 Модуль "Личный Кабинет"](#title5_1) <br>
&nbsp; [5.2 Модуль "Прием и обработка Заявок"](#title5_2) <br>
&nbsp; [5.3 Модуль "Отчеты"](#title5_3) <br>

[6. Диаграмма последовательности](#title6)</br>

&nbsp; [4.1 ...](#title4_1) <br>
&nbsp; [4.2 ...](#title4_2) <br>
<br>

## <a id="title1"> 1. Общая информация </a>
### <a id="title1_1"> 1.1. Термины и определения </a>
|Термин	|Определение|
|---|---|
|**Абонент** |*Собственник или пользователь помещения в МКД обслуживаемом **АДС***| 	
|**Аварийно-диспетчерская служба (АДС)**	|*Организация,  осуществляещая текущий контроль за работой внутридомовых инженерных систем многоквартирных домов (МКД), качества коммунальных ресурсов, а такще осуществляющую круглосуточную регистрацию и контроль выполнения **Заявок** собственников и пользователей помещений* |
|**Администратор**|*Роль. Сотрудник **АДС** выполняющий функции по регистрации **Заявок** и/или изменении их атрибутов и/или статусов*|
|**Диспетчер**	|*Роль. Сотрудник **АДС** выполняющий функции по регистрации **Заявок** и/или изменении их атрибутов и/или статусов*|
|**Заявка**	|*Обращение собственника или пользователя помещения в МКД связанным с предоставлением коммунальных и других услуг, выполнением работ по содержанию и ремонту общего имущества или устранением неисправностей и повреждений внутридомовых инженерных систем*|
|**Заявитель** |***Абонент** или иное физическое лицо или организация обратившееся в **АДС***| 
|**Исполнитель работ (Исполнитель)**|*Роль. Сотрудник или совокупность сотрудников **АДС** или внешний подрядчик, привлекаемый **АДС** для выполнения работ/услуг по **Заявке***|
|**Отчет**	|*Шаблонизированный набор данных возвращаемых **Системой** по запросу **Пользователя***|
|**Пользователь отчетных форм (Пользователь)**	|*Роль. Сотрудник **АДС** или внешний пользователь **Системы** имеющий право получать **Отчет** для осуществления или анализа деятельности **АДС***|
|**Руководитель**	|*Частный случай роли **Пользователь отчетных форм***|
|**Система**	|*Разрабатываемая информационная система*|



### <a id="title1_2"> 1.2 Ссылки на существующую документацию, НПА </a>

|п/п|Наименование|Ссылка| 
|---|---|---|
|1.|*Постановление Правительства РФ от 15.05.2013 N 416 "О порядке осуществления деятельности по управлению многоквартирными домами"*|[см. текст](https://docs.cntd.ru/document/499020841) <br> *(с изменениями на 21 декабря 2023 года)*|
|2.|*Постановление Правительства РФ от 27.03.2018 N 331 (ред. от 29.07.2020) "О внесении изменений в некоторые акты Правительства Российской Федерации по вопросам осуществления деятельности по управлению многоквартирными домами и содержанию общего имущества собственников помещений в многоквартирных домах и признании утратившими силу отдельных положений некоторых актов Правительства Российской Федерации"*|[обзор](https://www.garant.ru/hotlaw/federal/1188602/) документа (ИС "Гарант")<br><br>[вносимые изменения](https://www.consultant.ru/document/cons_doc_LAW_294631/0b88710e249ab2806074e06e64d02ae3040609e9/) (ИС "Консультант")|


## <a id="title2"> 2. Требования (по Вигерсу) </a>

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


## <a id="title3"> 3. Бизнес-требования </a>

- *Система* должна обеспечить круглосуточную регистрацию и отработку *Заявок*;
- *Система* должна обеспечить предоставление ответа на *Заявку* не позднее 10 минут с момента поступления;
- *Система* должна обеспечить ведение журнала учёта *Заявок* в ГИС ЖКХ;
- В случае аварийных повреждений внутридомовых инженерных систем *Система* должна обеспечить информирование органа местного самоуправления муниципального образования, на территории которого расположен многоквартирный дом (МКД), о характере повреждения и планируемых сроках его устранения;

### Бизнес-правила



## <a id="title4"> 4. Контекстная диаграмма </a>

### Системы АДС

![АДС_Контекстная_диаграмма](https://github.com/user-attachments/assets/43203029-4abc-4fcc-b8f4-87c400620a40)

[см. в Google Draw](https://docs.google.com/drawings/d/1WK4C3f7dXRz46UVjHfCQ6sbBk8tnQkyMIweeT2CtFcc/edit?usp=sharing)

### Личный Кабинет

![Личный Кабинет](https://github.com/vnukov-vv/SA_SHIFT_DV/blob/main/FILES/Контекстная%20диаграмма.drawio.svg)

### Отчеты
![Отчеты](https://github.com/vnukov-vv/SA_SHIFT_DV/blob/main/FILES/Контекстная%20диаграмма%20отчетов.svg)

[см. в Google Draw](https://docs.google.com/drawings/d/1kmKBb2_9vgw7XziOYgGlHkOIZncMWC968R5Iz-mW2uQ/edit)


## <a id="title4"> 4. Архитектура Системы (HLD) </a>

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

@enduml
```

</details>


## <a id="title5"> 5. Пользовательские сценарии. Use Cases диаграммы </a>
### <a id="title5_1"> 5.1 Модуль "Личный Кабинет" </a>

![SVG](https://www.plantuml.com/plantuml/svg/bPNHIXj158RlvoaEkR6zK2obDqL4CVMcBOZINXLacXrrSRD9ToTjfHJKrfQYe8XNBRGLNo2cXgo99gym-qRzpvOaiqnIeg3kJkPyCvp_FtyMOYqZNIi7z29MIp9Mwy-UBXRNHA0sDEaAHVxcbYRFZrH9-vLGYAbusm-hCf9b2lnGwPsgeagajofYolHCntJJVNEBltlfVdf4MEgI-OFtNPEObkcQMtnUnxv4345XnLEngjB3sVz06gQPxc8zCMq74Cbmcm4F7iqA8Kkw4b71d9XBFiyq-SnNuJrpYggwkS921wml6TVSuF4Rxp59Udo_G3BcJaH2L6LfMsugW7wOxmJQcJalq0T1L8jLISRyoONffRjWDamdFSxkwZBnbXJ8-k4JbjQVon3qbKYLSyGpb5zcn6GappIPvU8MFSzX_KR95LXjxXhksGMrFfwQ1pxnVEqGBp9UPwAxMQoY2XpKBrm80gCUOkEvcI6nq0Dz3-2soxykMD2NldgNKNFOSvIq-9OP3ezrAD102puvTnkGbY8bjLfLRtAa4zD0tt15_1vaAhESsIM_iXNPe233ZWM7k2RVgc8aDtIEUCeqzdJ6Gl5OdWDSLJ5CxJApDgA46sXwVTvd770DInw2DDejMilIrh8Vg5ZSLPL1Jxk3czgIe8qJ47aA-q5WgMIIqSIYqj8FuXpu9-fl_Xd3rNgir38igG34F2eB7LZcBgWLkUDmM5nxU3d7MkcXQOmttx9Itcj4ZVY8R2KxKVf3DIPJACl1DcM3VSKdSh2bH-XrcsS5S97B6PhnPkQjh22YnpGtvuUbeEQf-VaHk-qWc6mtHdr2jZN33XkT64volmkMImH7D4rF0s9phMLxgkrLFj5USqsMXmpyOgz2Udif9wEmZnwsV3XmH4vpt18xGuWcBR5Jeb-YtciLUaw5OuKHXn11XWRiUydVtoDiw39jKITY9gOrZ1SOcgMtvh6UavquaDdZUEaYG_1uJ8Ezj-bXUY06yj1CtWRvRYpWNwqSYBy0)


<details><summary>Развернуть код </summary>

```plantUML
@startuml UseCase_LKADS
left to right direction

'skinparam linetype ortho
'плотность по горизонтали
skinparam nodesep 30
'плотность по вертикали
skinparam ranksep 150

actor "Абонент\n(Владелец помещения)" as User

package "ЛК АДС" {
  usecase "Управлять помещениями"            as UC_ManagePrem
  usecase "Добавить помещение"               as UC_AddPrem
  usecase "Редактировать помещение"          as UC_EditPrem
  usecase "Удалить помещение"                as UC_DelPrem
  usecase "Просмотреть список помещений"     as UC_ViewPrem

  usecase "Создать заявку"                   as UC_CreateReq
  usecase "Автосохранить черновик"           as UC_SaveDraft
  usecase "Восстановить черновик"            as UC_RestoreDraft
  usecase "Прикрепить файлы"                 as UC_AttachFiles

  usecase "Просмотреть список заявок"        as UC_ViewReq
  usecase "Просмотреть детали заявки"        as UC_ViewReqDetails
  usecase "Отменить заявку"                  as UC_CancelReq
  usecase "Оплатить заявку"                  as UC_PayReq
  usecase "Оставить отзыв"                   as UC_Feedback
}

' Управление помещениями как родительский UC
UC_ManagePrem .d.> UC_AddPrem   : <<include>>
UC_ManagePrem .d.> UC_EditPrem  : <<include>>
UC_ManagePrem .d.> UC_DelPrem   : <<include>>
UC_ManagePrem .d.> UC_ViewPrem  : <<include>>

' Создание заявки
User --> UC_ManagePrem
User --> UC_CreateReq
User --> UC_ViewReq
User --> UC_ViewReqDetails
User --> UC_CancelReq
User --> UC_PayReq
User --> UC_Feedback

UC_CreateReq .d.> UC_AttachFiles     : <<include>>
UC_CreateReq .d.> UC_SaveDraft       : <<include>>
UC_CreateReq .d.> UC_RestoreDraft    : <<extend>>
UC_CreateReq .d.> UC_AddPrem         : <<include>>  ' выбор помещения
UC_CreateReq .d.> UC_ViewPrem        : <<include>>  ' выбор из списка

' Оплата заявки только для платных
UC_PayReq .> UC_CreateReq : <<extend>>
@enduml
```
</details>

### <a id="title5_2"> 5.2 Модуль "Прием и обработка Заявок" </a>

![](https://www.plantuml.com/plantuml/svg/VL9FIlj05DxFAHxP_20_AhJTbH8ANa043p1DnZOqJK9cYaWLObrqOQ4k2afLf3U8Ob6iQQ_mvaQ-cKK38cxQl7n_lkyzqf6APseqZ1Zx9mTXdFAC3o4AOw7EKm59fle9YyIf0fL05lRw2e8m4xuAavWnri8xBFGSN_53Jt2D6prh0PV0qvIm1RszmXskzKHFwJUtM20DTc-HBMwm_A7rarXbZ1rnVy1x0fmpqNN6f7Z4Py0bHHKw9y6Ef0Nz5_-jQfXqYVE0Iy1RV27ZaYnBWrjOXagmIyQe6DHg5vvf0TL4wcgoPA3jZcbF7lSYAj5kuyfiOvj-OM5I5hZoF0V6R2I5poMnwWT0j2s-uvlffcVWkliBVUfhrtLCcPF3UgLfaEO92zAKH9nIYD6PWSI_dcc-jsbKDasoeIHAoVNDNz5DSuP0cbKzqwHw9ZjxUpDP8cCT4GVqSNm3)

<details><summary>Развернуть код </summary>

```plantUML
@startuml

'skinparam linetype ortho
left to right direction

:Заявитель: as app
:Диспетчер: as dsp
:Исполнитель: as contr

Package "web"{
:МП Квартплата+: as mob
:ЛК Абонента: as site
}

app --|> dsp 
app --|> mob 
app --|> site 


Rectangle "<<Система АДС>>" {
usecase "1. Создать **Заявку**" as UC1
usecase "2. Назначить на **Исполнителя**" as UC2
usecase "3. Закрыть **Заявку**" as UC3
}

dsp --> UC1
dsp --> UC2
contr --> UC3

@enduml

```
</details>

### <a id="title5_3"> 5.3 Модуль "Отчеты" </a>

![SVG](https://www.plantuml.com/plantuml/svg/XPHFQnD16CRlyobUUb4FiNSFKgds929MeGT1XcGQbsmtONSYHX7IHFHWeIezU13_e3SHbfgrIxD9eP_WdM_a-r27ZferXopPsVVvpVF-cLdBh4vjVoTMiTcsPBkKHks7bbfHQfeswYPAPPqewUbKxr1FDpkwRJRj83Q4xpffnqOftRJTbFYJ6_Cnp_bGVXCktOWBdhez__b0bdRvX0itSY_bEVGVtc5PD5EU1IhrUpTQuVS0kZ6MYJz0xjx8yzKAFLNzp3HrXgZFxZdFtP0hBkK96xaRGJ7tYXNI6TrRVt37zBgf3QHVkGHSuWBXAX_0A-TYhEIZfTIDABOc3QZV-HYPmPHWwkJtaukths-iRjtStBhaKJSU_sNmYmWBdWYW4ZS52iM5G8X_WCG0p-JVBZRob5jT6sqF0ifhdlbi2BcwCP2IMeutpc66I-8AVz4XBX4FkcTUItGyU6B2iZC84v-NmF1ovb1miYF16EmXYI1ppZrrFJNQchiwwmJWZnW9DvPPAHUWptlPDD6ZC-qpfIw8dqEtZtRL3UI-KdMZIer-usem8KlZV3cM1gAZou11py8y5fmSpfNwTvKQeVdw03-fjG7URNs4zraR4BOqJ6RnQKTBmlMWBYtWmZQ3nsyPmr1oXT4wPrUY-echWlZ43SNE2vmQd1TC6su6fVxmHfU3Yj4LElt6fVVXzlZ8ZP7PwNI1ofVnVoeLElUw40GjTBWRu1nMUGxbcabQSYt_0W00)


<details><summary>Развернуть код </summary>

```plantUML
@startuml
left to right direction

skinparam packageStyle rectangle

actor Руководитель
actor Диспетчер
actor Исполнитель

package "Модуль Отчёты" {
usecase "Сформировать отчёт" as UC_Report
usecase "Фильтровать/Детализировать отчёт" as UC_Filter
usecase "Экспортировать отчёт\n(PDF/XLSX)" as UC_Export
usecase "Уведомление о готовности" as UC_Notify
usecase "Анализ трудозатрат\nи материалов" as UC_Analyze
usecase "Создать задание\nна основе отчёта" as UC_CreateTask
usecase "Получить задание" as UC_ReceiveTask
}

'Связи Руководителя

Руководитель -u-> UC_Report
Руководитель -u-> UC_Analyze
Руководитель -u-> UC_Export
Руководитель -u-> UC_Notify

'Связи Диспетчера

Диспетчер --> UC_Report
Диспетчер --> UC_Filter
Диспетчер --> UC_Export

Диспетчер --> UC_Notify
Диспетчер --> UC_CreateTask

'Связи Исполнителя

Исполнитель -d-> UC_ReceiveTask

'Взаимосвязи между прецедентами

UC_CreateTask .> UC_Report : «использует»
UC_CreateTask .> UC_Filter : «использует»

UC_ReceiveTask .> UC_CreateTask : «порождено»

@enduml

```

</details>


### Таблица

|п/п|Поле 1|Поле 2|Описание| 
|---|---|---|---|
|---|---|---|---|




## <a id="title6"> 6. Диаграмма последовательности </a>



