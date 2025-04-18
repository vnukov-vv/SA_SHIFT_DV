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

![](https://www.plantuml.com/plantuml/svg/ZLRlInnd4Fx-_XLlfN3drSRGvbC94b6f0KcaKQHGM6nSwT5pJxoLfjzg16svjf5Icc2AzWZzldVclBtV_yAy_r7dcNtTTRExJH3lnpllp3ppp3Dp-w3XRn_uXtirJMVq9xKSEgS9ZSrpwjB07F7xc0Bpmc5RI05TcP_uTSH_WVgewZsj7Uwu-lxIlVcbUyvItVFTP_wTVOwse6wPwxkxrQVk_6R3FMZC7_AhlL9me-xLgfxhlF_YNltRQYrrKPLeOZ6EAJIdZBd3dxiqqkPd2jaGSct7sln6GvpoFqgTK4UNav8rjVbZJzEKkkp2TsXYZYYOLQhnVTNRtpxOtjC_76plRrLt_E_qPtVl8Z42NidbjqoEMbly-l7cXhFrS6FLMLlvSkNHSfdzIw2JfeAm0nVWfAvcdnIzfXb7M5jyjFnaQN5z1Vv-rQ-vcbeK0gYK4DZEwM-y_DvbWhCB8_aSzGNsh6kUuzCNcWOqDB-RqpbDFVXmm27uuV-1fb3p-nJ9sIR8xoYrphseUsN6WFEfn3e5StDw9diuWzD_m1KiI8k-c6FSu18g5RgWDh2ONo9sp8jAXTEobMqlKH2Z2L6ayDUlL6PcOmndNEi8JOw31-YlO2as2gOtILiu1QC1c3ZXG6WAKybUeJ8XQ7m3oFoAKBc6cKABbhnjgH5MdShRbPpgoOyDtzrpLfxvPNfDvnpi_iUt9cK1xNyjcX-R9lMr86wZMijib09V8H78vY_Moxy2gnMn8Q1Es8JIItI6uP6PwTyegSLuZ-cQ8mKbu4h1-fikys3n-GH8K2f62NAVIbWewpgUWIZfUPIK4KxP7W3f9qW5c7z0dGppBOhJk9tG54PuR7C4K6nDDITpAA4lQOAv5QuAD1ZfLpO3RDGJfhl2DFZXMCqvKQev4cbUs_M3c10SgZ77vYXfPpaQNG18aptvbD6yCpdyRG3i72lk0bfbWyoY3W1Fr8Jx32XT2_NdD7jdTr1Mx02gIjpq3X_tA5HVkRLSLdDdFnOx-jwB9bmmMhQmgcMrs9ea2RTZjZWDX5ySU7LZOtr-SVtX_qM0HZyeWeJ8gojkMU4MoyCYo1FNIoibIAu0FP1-i0TSdENY_HVZpjrqsVJEPi5wIq62aGLz6a5YqolgsH_LlBYfPN4PnMX9MHt0XLBjp9jcj2tjZzcLr762ETIurnO9MPM-iuGkCd6XzeumDw5HhFV-xN6Hdygq37F6VOZrcZFqiLeiCpUrNTXov36aiD6nbqN-9W5Rq1yPofUe7aRiFeO3LZ1ImehowhwhQ-wkh-kxEZi8MbMm_cKbcnFJnDSM5WL48_d780cXnOG90F-eroghgHdfEQndijHnVMJ9YHf6rn0h6xeBolLsD32n1bOVRoKFH0_Om4zkIlq7)

<details><summary> Развернуть код </summary>
</details>

## <a id="title4"> 4. Пользовательские сценарии </a>

### Таблица

|п/п|Поле 1|Поле 2|Описание| 
|---|---|---|---|
|---|---|---|---|

### Диаграмма
<details><summary>Развернуть код </summary>
</details>




