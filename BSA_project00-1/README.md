# DAY 00 – SA

## Contents

1. [Chapter I](#chapter-i) \
    1.1. [Preamble](#preamble)
2. [Chapter II](#chapter-ii) \
    2.1. [General rules](#general-rules)
3. [Chapter III](#chapter-iii) \
    [Theory](#theory)  
    3.1. [Жизненный цикл разработки ИТ-систем](#жизненный-цикл-разработки-ИТ--систем)  
    3.2. [Выявление источников информации](#выявление-источников-информации)  
    3.3. [Глоссарий](#глоссарий)  
    3.4. [Правила размещения, именования и другие правила](#правила-размещения-именования-и-другие-правила)  
    3.5. [Декомпозиция. Основные понятия](#декомпозиция-основные-понятия)  
    3.6. [Правила декомпозиции](#правила-декомпозиции)  
    3.7. [Рекомендации по построению декомпозиции](#рекомендации-по-построению-декомпозиции)  
4. [Chapter IV](#chapter-iv) \
    4.1. [Задача 1](#задача-1)   
    4.2. [Задача 2](#задача-2)  
5. [Chapter V](#chapter-v) \
    5.1. [Exercise 00](#exercise-00)   
    5.2. [Exercise 01](#exercise-01)   
    5.3. [Exercise 02](#exercise-02)  
    5.4. [Exercise 03](#exercise-03)  
    5.5. [Exercise 04](#exercise-04)  
    5.6. [Exercise 05](#exercise-05)  
    5.7. [Exercise 06](#exercise-06)  

<h2 id="chapter-i" >Chapter I</h2>
<h2 id="preamble">Preamble</h2> 

Типовой жизненный цикл разработки программного обеспечения состоит из этапов: обследование, проектирование, разработка, тестирование, внедрение, эксплуатация, вывод из эксплуатации. Вы познакомитесь с типовым составом команды и работами на каждом этапе. 

А еще в текущем проекте вы рассмотрите несколько навыков ИТ-аналитика, который выполняет те или иные работы на каждом этапе разработки:

1. Выявление источников информации.  
Практически во всех проектах информации, указанной первоначально в условиях задачи, недостаточно. Поэтому мы должны уметь быстро выявлять дополнительную информацию.  

2. Единство терминов и понятий.  
Неточности в трактовке терминов и понятий чреваты ошибками проекта. Ведение глоссария проекта позволяет максимально снизить вероятность неточного трактования.

3. Декомпозиция.  
Один из основных приемов проектирования программного обеспечения и разработки сложных ИТ-систем.

В этом проекте вы научитесь:  
- собирать источники информации и использовать их в дальнейшем;  
- создавать и вести глоссарий для единого толкования терминов и понятий;  
- «разделять слона на кусочки», применяя принципы и правила декомпозиции.  

Литература:
1. [Принципы декомпозиции модели процесса](https://cyberleninka.ru/article/n/printsipy-dekompozitsii-modeli-protsessa/viewer)
2. [Обзор структурной декомпозиции работ](https://docs.microsoft.com/ru-ru/dynamics365/project-operations/prod-pma/work-breakdown-structures). 


<h2 id="chapter-ii">Chapter II</h2>
<h2 id="general-rules">Genеral rules</h2>

1. Всю дорогу вас будет сопровождать чувство неопределенности и острого дефицита информации: это нормально. Не забывайте, что информация в репозитории и Google всегда с вами. Как и пиры, и Slack. Общайтесь. Ищите. Опирайтесь на здравый смысл. Не бойтесь ошибиться.  
2. Будьте внимательны к источникам информации. Проверяйте. Думайте. Анализируйте. Сравнивайте.   
3. Будьте внимательны к тексту задания. Перечитайте несколько раз.   
4. Читайте примеры внимательно. В них может быть что-то, что не указано в явном виде в самом задании.  
5. Вам могут встретиться несоответствия, когда что-то новое в условиях задачи или примере противоречит уже известному. Если встретилось такое — попробуйте разобраться. Если не получилось — запишите вопрос в открытые вопросы и выясните в процессе работы. Не оставляйте открытые вопросы неразрешенными.   
6. Если задание кажется непонятным или невыполнимым — так только кажется. Попробуйте его декомпозировать. Скорее всего, отдельные части станут понятными. 
7. На пути вам встретятся разные задания. Те, что помечены звездочкой (*) — подходят для более дотошных. Они с повышенной сложностью и не обязательны к выполнению. Но если вы их сделаете, то получите дополнительный опыт и знания.  
8. Не пытайтесь обмануть систему и окружающих. В первую очередь вы обманете себя.  
9. Есть вопрос? Спроси своего соседа справа. Если это не помогло — соседа слева.  
10. Когда пользуетесь помощью — всегда разбирайтесь до конца: почему, как и зачем. Иначе помощь не будет иметь смысла.  
11. Всегда делайте push только в ветку develop! Ветка master будет проигнорирована. Работайте в директории src.  
12. В вашей директории не должно быть иных файлов, кроме тех, что обозначены в заданиях.  

<h2 id="chapter-iii">Chapter III</h2>
<h2 id="theory">Theory</h2>
<h2 id="жизненный-цикл-разработки-ИТ--систем">Жизненный цикл разработки ИТ-систем</h2>  

Любое ПО проходит через 6 основных этапов, от начального замысла до использования её конечным пользователем. Эти этапы в разных методологиях могут называться по-разному, мы приведем наиболее употребляемые термины. Вот эти этапы:  
- Обследование (сбор требований);  
- Проектирование;  
- Разработка;  
- Тестирование;  
- Внедрение;  
- Сопровождение.   

В общем случае, в команде разработки присутствуют специалисты, выполняющие такие роли:  
- ИТ-аналитик (может быть отдельно бизнес-аналитик и системный аналитик);  
- Архитектор (архитекторы могут быть разных направлений);  
- Разработчик (разработчики тоже могут быть разных направлений);  
- Тестировщик (и они бывают разные);  
- Специалист внедрения/сопровождения;  
- Менеджер;  
- Специалист DevOps;  
- Технический писатель.  

И это только роли, не отдельные специалисты. Каждую роль может выполнять несколько человек, и один человек может выполнять несколько ролей.   


<h2 id="выявление-источников-информации">Выявление источников информации</h2>

Существует много методов выявления информации о задаче, о некоторых мы поговорим позже. Но один метод надо понимать всегда и начинать с него. Это — изучение материалов, до которых можем дотянуться в начальный момент: нормативно-правовые документы, официальный сайт, статьи в СМИ, описание процессов, научно-популярные ролики. В случае госорганов — список функций, возложенных государством (их тоже можно найти на официальном сайте).  
Мы не сможем изучить все документы в сжатые сроки, поэтому создаем каталог источников информации, к которому можем обратиться в нужный момент.  

Заносим туда:  
1. Нормативно-правовые акты;  
2. Приказы, распоряжения;  
3. Сайты, статьи в СМИ, ролики;  
4. Регламенты, инструкции;  
5. Интервью, опросы;  
6. Мировой опыт, лучшие практики, опыт конкурентов;  
7. И т.д.  

Чтобы не потеряться в этих источниках, рекомендуется указывать некоторые параметры. Эти параметры вы должны выбрать самостоятельно, исходя из здравого смысла, чтобы быстро ориентироваться в большом объеме документов, например:  
1. Источник (название, автор, дата выпуска, откуда получен, и пр.);  
2. Адрес размещения;  
3. Приоритет изучения;   
4. Актуальность, легитимность (не устаревшая ли информация? насколько можно доверять источнику?);  
5. Дата ввода / прекращения действия (если это нормативно-законодательные документы); 
6. Кто добавляет источник в каталог;  
7. Дата занесения;  
8. Отметка об изучении;  
9. Примечание (содержание, комментарии, заметки).  

Даже кратко записанное содержание и небольшие комментарии помогут вам вспомнить и вернуться к источнику при необходимости.  

<h2 id="глоссарий">Глоссарий</h2> 

Часто одно понятие называют разными словами, например, “стейкхолдеры” и “заинтересованные стороны”. А иногда одним именем называют совсем разные понятия, например, лицевой счет и балансовый счет сокращенно могут называть «счет». Путаница в понятиях отрицательно сказывается на результатах анализа, а затем и проектирования, повышает риск ошибок, может потребовать переделки уже выбранных решений, увеличить сроки работ. Для исключения этого, с самого начала следует создать глоссарий и поддерживать его на протяжении всей работы над проектом. Надо понимать, что понятия могут изменять свое значение, например, при изменении нормативно-правовых документов. Поэтому следует вести историю изменений глоссария, указывать дату добавления/обновления каждого понятия и фиксировать его источник.   

<h2 id="правила-размещения,-именования-и-другие-правила">Правила размещения, именования и другие правила</h2>  

Для уменьшения ошибок из-за нестыковок и досадных недоразумений, рекомендуется придерживаться правил размещения и именования создаваемых артефактов. Обычно эти правила вырабатываются командой продукта/проекта в начале работ. Если вы пришли в команду в процессе работы — выясните эти правила и выполняйте их. Если таких правил не выработано, то выработайте их самостоятельно, доведите до других членов команды и, при согласовании, придерживайтесь их. 
Ниже — вариант правил, который можно использовать в работе над проектами.   

1. Для каждого продукта (задачи) определите префикс — трех- или четырехбуквенное осмысленное выражение и создайте для каждого продукта (задачи) отдельную директорию, названную с указанием префикса.  
2. Размещайте все рабочие и проектные документы в созданной директории. Часто в директории дополнительно создают отдельные папки для разделения документации по типам: контрактная, рабочая, проектная, пользовательская и пр.   
3. Текстовые рабочие документы, состоящие из списков, сохраняйте в формате .xlsx. Так проще добавлять новые признаки и свойства, необходимые для работы. Также можно сохранять в формате .docx альбомной ориентации.  
4. Списки, каталоги размещайте на разных листах в файле формата .xlsx.   
5. При создании каталогов кодируйте как сам каталог, так и его элементы. Один из вариантов кодировки:  
   a. Каждый каталог обозначается осмысленным трехбуквенным выражением, например:   
   - STA — каталог заинтересованных сторон (стейкхолдеров);  
   - INF — каталог источников информации.  
   b. Элементы каталогов обозначаются по шаблону <XXXYYYYY>, где:  
   - XXX — буквенное обозначение каталога;  
   - YYYYY — числовое значение, уникальный неизменяемый номер в каталоге, количество знаков — на усмотрение разработчика каталога.  
6. Создайте документ «Содержание», где отражайте все созданные аналитиками артефакты, место их размещения, автора (ответственного). Допустимо размещать его как отдельный лист в файле каталога.  
7. Актуализируйте документ «Содержание» в процессе работы.  

P.S.  Принципы кодировки и размещения могут отличаться в зависимости от сложности системы, предметной области, правил компании или команды.
**Пример:**
![Пример правил размещения, именования и другие правила](misc/images/Ch3.4.png)

<h2 id="декомпозиция.-основные-понятия">Декомпозиция. Основные понятия</h2>

Декомпозиция, то есть процесс разделения целого на части, позволяет рассматривать любую систему, как состоящую из отдельных взаимосвязанных подсистем, которые, в свою очередь, также могут быть декомпозированы.   
Мы применяем процесс декомпозиции в ИТ повсеместно, когда разбиваем на небольшие части свои цели, задачи, а также функции и компоненты самой ИТ-системы.   
Декомпозировать можно различными способами, видов декомпозиции довольно много. При разработке ИТ-систем обычно применяют такие виды декомпозиции:  

**1. Функциональная** - структурирование функций. Например, в задаче 1 (Chapter IV) клиент барбершопа может выполнить действия (функции):  
   - Регистрация на сайте;  
   - Просмотр расписания мастеров;  
   - Выбор мастера, услуги, времени;  
   - Запись на услугу.  

**2. Объектная, компонентная** – расчленение на объекты. Так, в задаче 1 (Chapter IV) услуги подразделяются на:
   - Первый уровень: тип услуги (парикмахерские, косметические);  
   - Второй уровень (парикмахерские): стрижка, покраска, укладка и т.д.;  
   - Второй уровень (косметические): чистка, массаж, питательная маска и т.д.  

**Цели разбиения**  
Вид декомпозиции выбираем исходя из стоящей перед нами цели. В таблице 1 приведены цели выполнения декомпозиции и соответствующие им основные виды, а также вопросы, помогающие выполнить декомпозицию.   

Таблица 1. Вопросы для выявления вида декомпозиции
![CH3.t1](misc/images/CH3.t1.png)

**Уровень (глубина) декомпозиции**  

Уровень декомпозиции, т.е. глубина разбиения и подробности описания, зависит от предназначения декомпозиции и пользователя (для кого предназначена). В качестве элементарного уровня выбирают уровень, достаточный для выполнения работ. Искомая система принимается за нулевой уровень и не учитывается при подсчете уровней декомпозиции, т.к. разбиения на нулевом уровне нет, поскольку на нем система представлена в целостном виде.      

**Документирование декомпозиции**  
Декомпозицию можно записать в виде схемы, таблицы, каталога. 
Для наглядности каждому элементу декомпозиции присваивается уникальный идентификатор, соответствующий уровню и, например, порядковому номеру на уровне с использованием разделителей типа табуляции, знаков препинания и т. д. На рисунке 1 представлена декомпозиция завтрака.  

Для обозримости рекомендуют выделять на каждом уровне 7 (+/- 2) подсистем/элементов. Естественно, это не всегда получается. Иногда количество элементов довольно велико. В таких случаях декомпозиция представляется в табличном виде или в виде каталога.  

Часто на схеме показывают не только декомпозируемую систему, но и вышестоящую (надсистему), в которую входит рассматриваемая система, и смежные системы — другие подсистемы надсистемы. На рисунке 2 — декомпозиция системы Система1. Дополнительно на этой же схеме указаны надсистема и смежная Система2.

Рисунок 1. Декомпозиция подготовки завтрака
![CH3.t2](misc/images/CH3.t2.png)

Рисунок 2. Декомпозиция системы Система 1
![CH3.t3](misc/images/CH3.t3.png)


<h2 id="правила-декомпозиции">Правила декомпозиции</h2>

При построении декомпозиции применяют следующие правила:

1. Подчиненность;
2. Единственность критерия;
3. Целостность.

**Подчиненность**   
Построение декомпозиции обычно начинается сверху вниз. Исходная система располагается на нулевом уровне и представляется в виде частей одинаковой значимости, которые не пересекаются между собой и полностью закрывают верхний уровень. Это первый уровень декомпозиции. Расчленение этих подсистем приводит к появлению подсистем второго уровня и т.д.    

**Единственность критерия**  
Система расчленяется только по одному, постоянному для уровня, критерию. Критерии уровней выбираются в зависимости от цели декомпозиции. Критерием декомпозиции может быть:  
1. Назначение (выполнение функций);  
2. Конструктивное устройство (части системы, вид материалов, формы поверхностей и др.);  
3. Структурные признаки (способы построения и др.);  
4. Виды этапов и процессов (жизненный цикл, физическое состояние и др.);  
5. Предметные характеристики (экономические, информационные, технологические и др.);  
6. И другие.  

Например, выделение в составе автомобиля мотора, шасси и кузова проводится в соответствии с функциональным признаком (назначение частей).   

**Целостность**  
Целостность обеспечивается правилами:  

**1. Полнота:**  вычленяемые подсистемы на одном уровне в сумме должны полностью характеризовать систему верхнего уровня. Не должно оставаться чего-то, что не входит в одну из групп. Если нет возможности определить полный набор элементов, допустимо ввести группу «другие», «прочие» и т.п.;    
**2. Взаимное непересечение:** элементы, входящие в одну группу, не должны входить в другую группу на этом же уровне.  

P.S. Иногда в работе целесообразно отойти от этих правил, и в дальнейших проектах мы рассмотрим такие примеры.   

<h2 id="рекомендации-по-построению-декомпозиции">Рекомендации по построению декомпозиции</h2>

Перед тем, как выполнять декомпозицию, определите:  
1. Зачем декомпозировать? Что хотим показать?  
2. Для какого пользователя выполняем декомпозицию? В чем потребность пользователя?  
3. Какой показатель выбираем для разбиения? Что будет составными частями?   
4. По каким критериям хотим разделять подсистемы и элементы декомпозиции?  
В ответах на эти вопросы раскроется цель и потребность декомпозиции, и далее вы определите ее вид.  

P.S. Не всегда хорошая декомпозиция получается с первого раза (точнее — редко получается с первого раза). Хорошее решение приходит с опытом.  

**Примерный порядок создания декомпозиции методом Сверху-вниз**  
1. Определите верхний (корневой, нулевой) уровень декомпозиции — систему, которая подлежит разбиению.    
2. Выберите несколько критериев (два-три) для разделения подсистем первого уровня, соответствующих цели декомпозиции.   
3. Разбейте корневую систему по каждому критерию.  
4. Проверьте, что по каждому критерию выполняются правила декомпозиции:    
   a. Система верхнего уровня разделена полностью (не осталось неохваченной части);  
   b. Все части нижнего уровня входят в верхний уровень системы; 
   c. Выделенные части нижнего уровня разделены по единому критерию;  
   d. Выделенные части не пересекаются между собой.  
5. Сравните результаты разбивки по выбранным критериям, выберите оптимальный с учетом дальнейших действий.    
6. Повторите операции 2-5 для каждой подсистемы первого и всех последующих уровней.   
7. Остановитесь на том уровне, который достаточен для выполнения теми, кто будет работать с выделенными элементами (функциями, работами или объектами).  

<h2 id="chapter-iv">Chapter IV</h2>  

## Задача 1
### Запись на стрижку  (Sign up for a haircut)  

Руководство сети барбершопов приняло решение о внедрении системы, обеспечивающей онлайн-запись на прием. Основная цель — развитие бизнеса путем расширения клиентской базы за счет возможности онлайн-записи, а также снижение трудозатрат сотрудников и уменьшение ручного труда за счет автоматического информирования клиентов по каналам связи.   

Запись может осуществлять как зарегистрированный, так и незарегистрированный посетитель сайта. При записи можно выбрать тип услуги: парикмахерские или косметологические, а также саму услугу, мастера и время из свободных интервалов. Система должна обеспечивать автоматическую отправку напоминаний клиентам через выбранный клиентом канал связи (тг, вотсап, vk, смс) по настроенному менеджером расписанию. После получения услуги система предлагает клиенту оценить услугу и написать предложения по улучшению работы.  

Расписание мастеров и выполняемые каждым мастером услуги должен вводить менеджер, возможно это будет не один человек. Он же отвечает за актуальность расписания и при необходимости корректирует его, осуществляет связь с клиентами в ручном режиме, проставляет отметку о выполнении услуги, начисляет и принимает оплату, передает данные об оплате в бухгалтерию. Также менеджер может получать отчеты о выполненных услугах и просматривать отзывы клиентов.  

Любой мастер имеет возможность посмотреть расписание и запись на свои услуги, отзывы клиентов. 
 
## Задача 2 
### Доставка заказов (Delivery of orders)

В локдаун многие продуктовые магазины и предприятия питания резко увеличили объемы онлайн-продаж, и возросла потребность в быстрой доставке мелких партий товаров индивидуальным клиентам. Компания студентов собралась и решила создать стартап службы доставки. Идея состоит в том, чтобы оперативно получать информацию о заказах, месте и сроке комплектации, месте доставки, желаемых сроках доставки и раздавать инфо курьерам, которые будут получать заказ в месте комплектации и доставлять в место доставки. Решили развернуть онлайн-систему, куда стекаются заказы и откуда курьеры оперативно разбирают заказы для выполнения. На первом этапе решили собирать заказы от магазинов и предприятий питания любым доступным способом и вводить в систему в едином формате силами оператора, но разработать мобильное приложение для курьеров.  

Курьер должен иметь возможность просматривать информацию о заказах, выбирать заказ из свободных, бронировать его, забирать в точке выдачи и доставлять  клиенту. Результат своих действий курьер должен оперативно отражать в системе через мобильное приложение. Также в системе должен работать диспетчер, который контролирует курьеров и при необходимости переназначает заказы. Информация о поступивших заказах должна направляться в бухгалтерию (в другую ИТ-систему) для расчета с поставщиками заказов за доставку.  

Также в бухгалтерию должна направляться информация о доставке заказа, где будет производиться расчет оплаты курьеров. Начисленная оплата должна передаваться в систему и отражаться в личном кабинете курьера. И еще запланировано рабочее место администратора, регистрирующего курьеров и назначающего всем права доступа.

<h2 id="chapter-v">Chapter V</h2>  

## Exercise 00 
### Creating a workspace (Создание пространства) 

**Для каждой задачи:**  
1. Определить префикс продукта.  
2. Создать отдельную директорию в своем GIT-репозитории в подпапке src, имя директории должно содержать префикс продукта.   

## Exercise 01
### Identifying information sources (Выявление источников информации)

**Для каждой задачи:**. 

1. Создать каталог источников информации. 
2. Найти не менее 5 источников информации и занесите их в каталог.  
3. Указать приоритет изучения источников информации.  
4. Определить необходимые параметры каталога.  
5. Указать ваши ответы в файле ex01_<префикс продукта>_infosources.xlsx.   

## Exercise 02 
### Creating and maintaining a glossary (Создание и ведение глоссария) 

**Для каждой задачи:**   

1. Создать глоссарий.  
2. Разместить в глоссарии не менее 10 понятий.  
3. Указать ваши ответы в turn-in файле ex02_<префикс продукта>_glossary.xlsx.  

**Рекомендации по выполнению задания:**   
В работе над проектами (здесь и далее) в качестве даты добавления понятия в глоссарий следует указывать номер проекта, выполняя который было добавлено данное понятие (Пример: Day 00).  


## Exercise 03 
### Concept of Decomposition (Основные понятия декомпозиции)

1. Найти демографическую пирамиду РФ. Отразить найденную пирамиду в файле.  
2. Указать показатель разбиения демографической пирамиды.  
3. Указать цель составления демографической пирамиды.  
4. Определить вид декомпозиции демографической пирамиды.  
5. Указать:  
   a. Сколько уровней декомпозиции у демографической пирамиды;   
   b. Какие это уровни;   
   c. Какие критерии применяются для разбиения каждого уровня.    
6. Определить порядок построения демографической пирамиды.  
7. Указать ваши ответы в turn-in файле ex03_decomposition.docx.   

## Exercise 04 
### Types of Decomposition (Виды декомпозиции)

**Меню завтрака:** вареное яйцо, тост с маслом, сок, чай.

1. Рассмотреть декомпозицию завтрака на рисунке 3:  
  a. Определить цель и вид декомпозиции;   
  b. Указать количество уровней декомпозиции;  
  c. Найти ошибки декомпозиции и перечислить их;  
  d. Исправить ошибки в декомпозиции и применять исправленную версию для следующего задания.  
2. Разработать объектную декомпозицию завтрака на основе уточненной декомпозиции в пункте выше:  
  a. Указать цель декомпозиции;    
  b. Построить декомпозицию до уровня 2;  
  c. Указать критерии разбиения для каждого уровня построенной декомпозиции.  
3. Указать ваши ответы в turn-in файле ex04_types.docx.  

Рисунок 3. Декомпозиция завтрака
![CH5.ex5](misc/images/Ex04.png)

**Условия:**  
Средство для изображения декомпозиции – на ваше усмотрение.

## Exercise 05 
### Types of Decomposition (Виды декомпозиции)

**Для задачи 2:**

1. Изучить задачу 2 (Chapter IV).  
2. Разработать декомпозицию действий курьеров.  
3. Определить цель и вид декомпозиции.   
4. Указать количество уровней.  
5. Разработать объектную декомпозицию действующих лиц (ролей) задачи.  
6. Указать цель объектной декомпозиции.  
7. Указать количество уровней.  
8. Указать ваши ответы в turn-in файле ex05_types.docx.  

## Exercise 06 
### Decomposition Rules (Правила декомпозиции)

**Активности дня:**  
1. Перечислить не менее 10 активностей своего дня.  
2. Определить минимум 2 цели декомпозиции, в рамках каждой цели определить пользователей и потребности.  
3. Построить событийную декомпозицию активностей своего дня в соответствии с выбранной целью. Во время построения придерживаться правил декомпозиции.  
4. Указать ваши ответы в turn-in файле ex06_rules.docx.  


**Рекомендации по выполнению задания:**  
Нет единственно верного пути создания декомпозиции. Всегда идите от цели создания, потребности того пользователя, для которого создается декомпозиция. Выбирайте вид декомпозиции исходя из цели. Определяйте активности исходя из ответов на «Вопросы для выявления вида декомпозиций». Возможно, активности будут разноуровневые — на этапе перечисления активностей это нормально. Но далее обязательно посмотрите и перераспределите активности по уровням в зависимости от критерия.  
Следите, чтобы элементы одного уровня были равнозначными, отвечали на один и тот же вопрос, выделялись по одному критерию. Относились именно к этому уровню, а не к более высокому или низкому. Сделайте несколько вариантов и выберите наиболее подходящий вашей цели, вашим потребностям и условиям.  

>Пожалуйста, оставьте обратную связь по проекту в [форме обратной связи.](https://forms.gle/xy6m8PNb8xD8t2jb9)

