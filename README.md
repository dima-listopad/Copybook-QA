## 1. Тестирование и STLC. Принципы тестирования

Тестирование ПО (software testing) – процесс анализа программного средства и сопутствующей документации с целью выявления дефектов и повышению качества продукта.

Жизненный цикл тестирования ПО (Software Testing Lifecycle) - это последовательность действий, проводимых в процессе тестирования, с помощью которых гарантируется качество программного обеспечения и его соответствие требованиям.

Фазы STLC:
1.	Анализ требований (Requirement Analysis): один из важнейших этапов, потому что именно на нем можно почти бесплатно исправить недостатки проекта;
2.	Планирование тестирования (Test Planning): на этом этапе формируется план тестирования, т.е. мы определяем действия и ресурсы, которые помогут достичь целей тестирования;
3.	Разработка тест-кейсов (Test Case Development): выявление всех возможных случаев использования продукта, его характеристик и особенностей в процессе эксплуатации;
4.	Настройка тестовой среды (Test Environment Setup): настраиваются операционные системы и виртуальные машины, инструменты тестирования, также обращаемся с запросами к DevOps и администраторам, если требуется поддержка;
5.	Выполнение тестов (Test Execution): тесты выполняются на основе готовой тестовой документации и правильно настроенной тестовой среды;
6.	Завершение цикла испытаний (Test Cycle Closure): окончательная генерация отчетов о тестировании для клиента.

Принципы тестирования:
1.	Тестирование показывает наличие дефектов (Testing shows presence of defects) - Тестирование может показать, что дефекты присутствуют, но не может доказать, что дефектов больше нет;
2.	Исчерпывающее тестирование невозможно (Exhaustive testing is not possible) - Для проведения исчерпывающего тестирования придется протестировать все возможные входные значения и все пути выполнения программы, в большинстве случаев число таких вариаций стремится к бесконечности или просто на порядки превосходит отведенное время и бюджет;
3.	Раннее тестирование (Early testing) - Тестовые активности должны начинаться как можно раньше в SDLC, а именно когда сформированы требования;
4.	Скопление дефектов (Defect clustering) - Это может происходить потому, что определенная область кода особенно сложна и запутана, или потому, что внесение изменений производит «эффект домино»;
5.	Парадокс пестицида (Pesticide paradox) - Это эффект, при котором при регулярном прогоне тестовых сценариев ошибки перестают находиться;
6.	Тестирование зависит от контекста (Testing is context dependent) - Тестирование проводится по-разному в зависимости от контекста. Например, программное обеспечение, в котором критически важна безопасность, тестируется иначе, чем новостной портал;
7.	Заблуждение об отсутствии ошибок (Absence of errors fallacy) - Отсутствие найденных дефектов при тестировании не всегда означает готовность продукта к релизу. Система должна быть удобна пользователю в использовании и удовлетворять его ожиданиям и потребностям.

## 2. Виды тестирования

По объекту тестирования:
1.	Функциональное тестирование (functional testing) – проверка того что продукт обладает всем функционалом, который описан в требованиях;
2.	Нефункциональное тестирование (Non-Functional testing) - тестирование свойств, которые не относятся к функциональности системы:
  - Инсталляционное (installation testing) – установка, обновление, удаление;
  - Конфигурационное тестирование (configuration testing) – проверку работы ПО при различных конфигурациях системы (ОС, устройства, версиях браузеров);
  - Тестирование совместимости (compatibility testing) – проверка работы приложения на разных окружениях (кроссбраузерное и кроссплатформенное тестирование);
  - Тестирование удобства использования (usability testing) – тестирование направлено на удобство и понятность работы с приложением;
  - (i18n) Тестирование интернационализации (internationalization testing) – тестирование перевода на разные языки;
  - (l10n) Тестирование локализации (localization testing) – процесс адаптации нашего продукта к языку и культуре, формат даты и времени, правовые особенности, раскладка клавиатуры, контроль символики и цветов клиента;
  - Тестирование безопасности (security testing) – тестируем защищённость нашего программного продукта;
  - Тестирование интерфейса (interface testing) - проверки того, соответствует ли пользовательский интерфейс ПО требованиям;
  - Тестирование доступности (accessibility testing) – тестирование для людей с ограниченными возможностями, также для тех кто ограничен в своих возможностях (к примеру в момент когда человек за рулем);
  - Тестирование производительности (performance testing) – определяет работу вычислительной системы под определённой нагрузкой:
    - Нагрузочное тестирование (load testing) - проверяет способность приложения работать при ожидаемой рабочей нагрузке;
    - Стресс (stress) – проверяем что происходит с продуктом при высоких нагрузках;
    - Стабильность (stability) – тестируем работу сайта с определенными нагрузками в течении определённого времени;
    - Объемное (Volume testing) – проверка на передачу больших объемов информации;
    - Тестирование на отказ и восстановление (failover and recovery testing) – проверка на восстановление после ошибок и сбоев.

Тестирование, связанное с изменениями:
1.	Дымовое тестирование (smoke test) – проверка самого важного функционала продукта;
2.	Регрессионное тестирование (regression testing) –проверка того, что не нарушилась работоспособность работающей ранее функциональности, если её код мог быть затронут при использовании некоторых дефектов в другой функциональности;
3.	Тестирование сборки (build verification test) – тестирование на соответствие критериям качества новой сборки;
4.	Санитарное тестирование (sanity test) – это тестирование отдельной функциональности.

По исполнению сценария:
1.	Исследовательское тестирование (exploratory testing) – одновременно изучение проекта, функционала, проектирование тест кейсов в уме и тут же их исполнение не записывая и не создавая тестовую документацию;
2.	Свободное тестирование (ad-hoc testing) – импровизация без документации;
3.	Сценарное тестирование (scenario testing) – тестирование по заранее задокументированному сценарию.

По степени важности:
1.	Дымовой тест (smoke test) – проверка самого важного функционала продукта;
2.	Тест критического пути (critical path test) – проверяются типичные задачи продукта;
3.	Расширенный тест (extended test) – всё оставшееся что не проверяли в smoke и critical.

По цели тестирования:
1.	Тестирование новой функциональности (new feature test) – тестирование новой функциональности, которая ранее не тестировалась;
2.	Регрессионное тестирование (regression testing) – проверка того, что не нарушилась работоспособность работающей ранее функциональности, если её код мог быть затронут при исправлении некоторых дефектов в другой функциональности;
3.	Подтверждающее тестирование (re-test) - тестирование, с целью подтвердить успешность исправлений дефекта.

По направлению тестирования (По запуску кода):
1.	Статическое тестирование (static testing) (без запуска программы) – тестирование документации, дизайн. Если опытный программист, то глазами посмотреть код;
2.	Динамическое тестирование (dynamic testing) (с запуском программы).

По методу тестирования:
1.	Метод белого ящика (white box testing) - тестировщик имеет доступ к коду (unit test – это тестирование отдельного участка кода);
2.	Метод черного ящика (black box testing) - тестировщик не имеет доступа к коду (GUI);
3.	Метод серого ящика (grey box testing) - к части кода доступ есть, а к части нет (UI, dev tools, Postman).

По уровню тестирования:
1.	Компонентное (component testing) – это тестирование отдельного модуля (обычно unit test делает разработчик);
2.	Интеграционное (integration testing) - проверка взаимодействия модулей;
3.	Системное (system testing) - полная проверка приложения;
4.	Приемочное (acceptance testing) - вид тестирование на этапе сдачи готового продукта или его части.

По позитивности:
1.	Позитивное (positive testing) - тестирование которое соответствует нормальному поведению системы;
2.	Негативное (negative testing) - применяются сценарии которые соответствуют нештатному поведению системы.

По степени автоматизации:
1.	Ручное (manual testing) – тестировщики выполняют тесты не используя средств автоматизации;
2.	Автоматизированное (automated testing) – с использованием ПО.

По исполнителю тестирования:
1.	альфа-тестирование (alpha testing) - проверка программного продукта на поздней стадии, разработчиками;
2.	бета-тестирование (beta testing) - оценка ПО перед выходом на рынок в фокус-группе или добровольцами.

## 3. QA, QC и тестирование. Верификация и валидация 

Три уровня работы с качеством программного обеспечения:

- Специалист по тестированию занимается выполнением тестов. Тестированием называют проверку соответствия результатов работы программного продукта на соответствие заданным критериям. Тестировщики занимаются тестированием всего продукта в целом или же отдельных компонентов. 

- QC (Quality Control) — контроль качества продукта. Задача QC-специалиста — проверка конкретного продукта, что включает анализ кода продукта, дизайна, плюс тестирование. QC-инженер разрабатывает стратегию тестирование вполне определенного тестирования, взаимодействует с разработчиками и организует само тестирование.

- QA (Quality Assurance) — обеспечение качества продукта. QA-специалист контролирует и обеспечивает качество работы продукта компании. Он отвечает и за отдельные этапы разработки софта. В частности, за выбор инструментов для разработки, предотвращение возможных проблем. Еще он участвует в процессе совершенствования продукта. QA охватывает все этапы разработки, включая описание проекта, собственно, тестирование, релиз и, зачастую, пост-релизный этап.

Верификация - это проверки, выполняемые в процессе разработки ПО для ответа на вопрос: “правильно ли мы разрабатываем продукт? (Верификация всегда происходит до валидации)

Валидация - это процесс оценки конечного продукта, чтобы проверить, соответствует ли он потребностям бизнеса и ожиданиям клиентов, т.е. отвечает на вопрос: “правильный ли мы разработали продукт?”

Понять, что тестировщик выполнил свою работу хорошо можно по факту выполнения следующих задач:
- продукт проверен на соответствие требованиям;
- сведено к минимуму количество дефектов, которые обнаружит конечный пользователь;
- предоставлена отчетность по актуальному качеству продукта и любых остаточных рисках заинтересованным лицам.

## 4. SDLC. Модели разработки ПО
Жизненный цикл ПО (Software Development Life Cycle) – это период времени который начинается когда принимаются решение о том что нам надо сделать ПО и заканчивается выводом его из эксплуатации.

Идея → Сбор и анализ требований (сбор требований к разрабатываемому программному обеспечению; их систематизацию; документирование; анализ; выявление и разрешение противоречий) → Архитектура и дизайн (программисты и системные архитекторы, руководствуясь требованиями, разрабатывают высокоуровневый дизайн системы) → Разработка и тестирование (разработка алгоритмов – создание логики работы программы; написание исходного кода; компиляция – преобразование в машинный код; тестирование и отладка – юнит-тестирование) → Релиз (когда продукт доступен конечному пользователю) → поддержка (чинятся баги и дописываются новые идеи, чтобы каждый пользователь был счастлив) → вывод из эксплуатации.

МОДЕЛИ РАЗРАБОТКИ ПО:

- Водопадная (waterfall) – суть заключается в том, что мы можем переходить к следующему шагу разработки или тестирования только после того, как предыдущий был успешно завершён. Данная модель разработки подходит для проектов с чётко определёнными требованиями и для которых не предусматривается их изменение в процессе разработки (банковские структуры, медицинские, военные и космические отрасли).
К недостаткам водопадной модели принято относить тот факт, что участие пользователей ПО в ней либо не предусмотрено вообще, либо предусмотрено лишь косвенно на стадии однократного сбора требований. С точки зрения же тестирования эта модель плоха тем, что тестирование в явном виде появляется здесь лишь с середины развития проекта, достигая своего максимума в самом конце.
____
- V-модель –  это усовершенствованная каскадная модель, в которой заказчик с командой программистов одновременно составляют требования к системе и описывают, как будут тестировать её на каждом этапе. Тестирование здесь появляется уже на самых ранних стадиях развития проекта, что позволяет минимизировать риски, а также обнаружить и устранить множество потенциальных проблем до того, как они станут проблемами реальными.
Данная модель обычно используется в проектах где есть временные и финансовые ограничения и для таких задач, которые предполагают более широкое тестовое покрытие.
____
- Итерационная инкрементальная модель (Iterative and incremental model) – Итерационная инкрементальная модель особенностью данной модели является разбиение проекта на относительно небольшие промежутки (итерации), каждый из которых в общем случае может включать в себя все классические стадии. Итогом итерации является улучшение продукта - инкремент, выраженное в промежуточном билде (build).
Длина итераций может меняться в зависимости от множества факторов, однако сам принцип многократного повторения позволяет гарантировать, что и тестирование, и демонстрация продукта конечному заказчику (с получением обратной связи) будет активно применяться с самого начала и на протяжении всего времени разработки проекта. Во многих случаях допускается распараллеливание отдельных стадий внутри итерации и активная доработка с целью устранения недостатков, обнаруженных на любой из (предыдущих) стадий. Итерационная инкрементальная модель очень хорошо зарекомендовала себя на объемных и сложных проектах, выполняемых большими командами на протяжении длительных сроков. Однако к основным недостаткам этой модели часто относят высокие накладные расходы, вызванные высокой «бюрократизированностью» и общей громоздкостью модели.
____
- Спиральная модель (spiral model) - Используя эту модель, заказчик и команда разработчиков серьёзно анализируют риски проекта и выполняют его итерациями. Последующая стадия основывается на предыдущей, а в конце каждого витка — цикла итераций — принимается решение, продолжать ли проект.
Спиральная модель похожа на инкрементную, но здесь гораздо больше времени уделяется оценке рисков. С каждым новым витком спирали процесс усложняется. Эта модель часто используется в исследовательских проектах и там, где высоки риски. Эта модель не подойдет для малых проектов, она для сложных и дорогих, например, таких, как разработка системы документооборота для банка, когда каждый следующий шаг требует большего анализа для оценки последствий, чем программирование.
____
- Agile – это набор методов и принципов гибким управлением проектами. То как мы должны мыслить, какие должны быть ценности, чтобы правильно построить процессы.
Ценности Agile:
1. Люди и взаимодействия важнее процессов и инструментов;
2. Работающий продукт важнее исчерпывающей документации;
3. Сотрудничество с клиентом важнее условий согласования контракта;
4. Готовность к изменению важнее следования первоначального плана.
Методология подходит для больших или нацеленных на длительный жизненный цикл проектов, постоянно адаптируемых к условиям рынка. 
Основополагающие принципы Agile Manifesto:
1. наивысшим приоритетом признается удовлетворение заказчика за счёт ранней и бесперебойной поставки ценного программного обеспечения;
2. изменение требований приветствуется даже в конце разработки (это может повысить конкурентоспособность полученного продукта);
3. частая поставка работающего программного обеспечения (каждые пару недель или пару месяцев с предпочтением меньшего периода);
4. общение представителей бизнеса с разработчиками должно быть ежедневным на протяжении всего проекта;
5. проекты следует строить вокруг заинтересованных людей, которых следует обеспечить нужными условиями работы, поддержкой и доверием;
6. самый эффективный метод обмена информацией в команде — личная встреча;
7. работающее программное обеспечение — лучший измеритель прогресса;
8. спонсоры, разработчики и пользователи должны иметь возможность поддерживать постоянный темп на неопределённый срок;
9. постоянное внимание к техническому совершенству и хорошему проектированию увеличивают гибкость;
10. простота как искусство не делать лишней работы очень важна;
11. лучшие требования, архитектура и проектные решения получаются у самоорганизующихся команд;
12. команда регулярно обдумывает способы повышения своей эффективности и соответственно корректирует рабочий процесс.
Наиболее удачным примером использования Гибкой модели (Agile-model) на сегодняшний день является фреймворк Scrum.
____
- Scrum – это фреймворк для управления проектами. Вся разработка делится на спринты. Вся работа разбивается на итерации, которые называются Спринт (Sprint). Каждый Спринт длиться от 2х до 4х недель.
РОЛИ В SCRIM: 
Development team – это команда работающих над проектом разработчики, тестировщики, бизнес-аналитики. Действет коллективная ответственность; 
Scrum-мастер – человек, который следит, чтобы соблюдались принципы скрама, обучение нового персонала. (не участвует в разработке) Этот человек не руководитель команды, а тренер; 
Product owner – представляет интересы бизнеса, общается непосредственно с заказчиком, выясняет что необходимо и передает эту информацию. представляет клиента, не руководитель команды.
СОБЫТИЯ В SCRUM: 
1. Планирование спринта (Sprint Planning) - это событие в Scrum, которое знаменует начало спринта. В ходе планирования определяется объём работы на спринт и способы выполнения этой работы;
2. Ежедневный Scrum (Daily Scrum) – Что ты делал вчера? Что ты будешь делать сегодня? Какие есть препятствия для выполнения цели?
3. Обзор спринта (Sprint Review) – подводим итоги того что было у нас сделано во время нашего спринта;
4. Ретроспектива (Sprint Retrospective) - проводится в конце спринта. Её суть – выяснить, что можно улучшить исходя из результатов нашей итерации.
АРТЕФАКТЫ В SCRUM:
1. Бэклог продукта (Product Backlog) – это список в котором все задачи для реализации готового продукта;
2. Уточнение бэклога продукта (Product Backlog Refinement) – собирается команда и product owner который представляет вам новый юзер стори который он написал (уточняет интересующие вопросы);
3. Критерии подготовленности (Definition of Ready) – DoR (фокус на уровне бэклога) – помогает заказчику создать хорошо написанные пользовательские истории, которые готовы для разработки;
4. Пользовательские истории (User Stories) – это формулировка намерения, описывающая что-то, что система должна делать для пользователя. As a [Rose], I can [Functionality], So that [Rationale], Acceptance criteria.
5. Покер планирования (Planning poker) – это оценка юзер стори 
6. Бэклог спринта (Sprint Backlog) – выбираем что мы будем реализовывать в данном спринте, перетягиваем из бэклога продукта стори в бэклог спринта;
7. Инкремент продукта (Product Increment) – это всё то что мы разработали до и разработаем в конце данной итерации;
8. Критерии готовности (Definition of Done) – DoD (фокус на уровне спринта или релиза) – помогает проверить работу в соответствии со всеми требованиями проекта, а не только продемонстрировать, что функциональности работают.
МЕТРИКИ SCRUM:
1. Velocity – это скорость нашей команды. Рассчитывается как среднее арифметическое значение завершённых стори поинтов в предыдущих спринтах;
2.Capacity – количество доступного времени членов команды. Рассчитывается: все часы в итерации на каждого штатного разработчика нашей Development команды;
3. Диаграмма сгорания задач (Burndown chart)
4. Накопительная диаграмма потока (Cumulative flow diagram)
____
- Kanban – система, построенная на визуализации процесса выполнения задач команды. Основная идея в системе уменьшать количество задач, выполняемых в данный момент. Задача проходит по всем этапам на доске и как только она выполнена её можно отдавать заказчику. Kanban-доска состоит из колонок каждый из которых это отдельный процесс разработки. Пример: список задач которые нужно сделать, задачи в работе, выполненные задачи, задачи готовые к тестированию, задача протестирована.

## 5. Виды тестовой документации. Тест-кейс vs Чек-лист

Тестовая документация бывает двух видов внешняя и внутренняя:

Внешняя документация:
- Замечание – комментарий о небольшой неточности в реализации продукта;
- Баг-репорт – это технический документ, который содержит в себе полное описание бага;
- Запрос на изменение (улучшение) – описание требований, которые не были учтены при планировании/реализации продукта. И пути/рекомендации по модификации продукта;
- Отчет о тестировании (тест репорт) – документ, предоставляющий сведения о соответствии/ несоответствии продукта требованиям.

Внутренняя документация:
- Тест план (Test Plan) - это документ, описывающий весь объем работ по тестированию, начиная с описания объекта, стратегии, расписания, критериев начала и окончания тестирования, до необходимого в процессе работы оборудования, специальных знаний, а также оценки рисков с вариантами их разрешения.
(Хороший тест план отвечает на вопросы: Что тестируем? Где тестируем? Когда тестируем? Как тестируем?);
- Тестовый сценарий – последовательность действий над продуктом. Фактически при успешном прохождении всего тестового сценария мы можем сделать заключение о том, что продукт может выполнять ту или иную возложенную на него функцию;
- Тест набор (Test suite) -  набор тест-кейсов, собранных в группу для достижения некоторой цели. (Выполнения каждого являются некоторыми предусловиями для начала выполнения следующего. Тест кейсы идут по порядку);
- Чек-лист (check-list) – набор идей тестов;
- Тест кейс (test case) – набор входных данных, условий выполнения и ожидаемых результатов, разработанный с целью проверки того или иного св-ва или поведение программного средства.  

Атрибуты тест-кейса:
1. Уникальный идентификатор тест-кейса (необходим для удобной организации хранения и навигации по нашим тест-наборам).
2. Название (основная тема, или идея тест-кейса. Кратное описание его сути);
3. Предусловия (описание условий, которые не имеют прямого отношения к проверяемому функционалу, но должны быть выполнены. Например, оставить комментарий на вашем портале может только зарегистрированный пользователь. Значит для тест-кейса «Создание комментария» будет необходимо выполнение предусловия «пользователь зарегистрирован», и «пользователь авторизован»)
4. Шаги (описание последовательности действий, которая должна привести нас к ожидаемому результату);
5. Фактический результат;
6. Ожидаемый результат;
7. Дефект.

Преимущества: простота прохождения, удобство обучения;

Недостатки: долго писать, много копипасты, трудно поддерживать, долго писать.

Атрибуты чек-листа:
1. Версия билда;
2. Окружение;
3. Дата;
4. Автор;
5. Тип тестов;
6. Описание теста;
7. Результат теста.

Преимущества: мало текста, нет копипасты, проще поддерживать, быстрее писать.

Недостатки: малопонятны новичкам, возможное непонимание проверки (может быть непонятен замысел автора той или иной проверки).

## 6. Требования

Требования — это спецификация (описание) того, что должно быть реализовано.

Уровни требований:
1. Бизнес требования (Цель, ради которой создаётся продукт (для чего? Какая польза? Как получить прибыль?));
2. Пользовательские требования (задачи, которые пользователь может выполнять с помощью продукта);
3. Продуктные требования: 
  - Функциональные требования (охватывают предполагаемое поведение системы, определяя действия, которые система способна выполнять. Описывается в системной спецификации. В основном влияют на дизайн системы);
  - Нефункциональные требования (охватывают свойства системы (удобства использования, надежность, масштабируемость) которыми она должна обладать при реализации своего поведения)).

Пути выявления требований:
- Интервью (беседую с заказчиком или пользователями);
- Наблюдение (наблюдая за работой пользователя в похожем продукте или в старой версии и выяснить что их интересует и что нужно улучшить);
- Самостоятельное описание (мы можем самостоятельно написать требования включив здравый смысл);
- Прототипирование (т.е. разрабатывая сайт и у нас есть конкурент, мы можем зайти к нему и посмотреть, как он работает, как реализованы разные функции);

Свойства требований:
- Завершённость (требование должно содержать всю необходимую информацию);
- Непротиворечивость (одни требования не должны противоречить другим);
- Корректность (требование должно четко указывать на то, что должно выполнять приложение);
- Недвусмысленность (точность формулировки в требованиях может по-разному интерпретироваться тестировщиками, разработчиками и другими участниками проекта);
- Проверяемость (требование должно быть проверено на предмет того, выполняется оно или нет. Если мы что-то не можем проверить значит такое требование не нужно записывать);
- Модифицируемость (исправление / внесение правок в требования должно быть простой операцией.);
- Прослеживаемость (возможность отследить связь между требованием и другими артефактами проекта, каждое требование имеет уникальный идентификатор, по которому оно легко прослеживается).

Как упростить работу с требованиями:
- Написать тест-кейсы – когда мы получаем требования мы можем сразу написать тест-кейсы, если мы не можем написать его (мы не можем придумать проверки, которые покрыли бы это требование). В данном случае мы можем обратиться к нашему Product owner чтобы он связался с заказчиком, и они переформулировали это требование, узнали точно ли нужна эта функциональность. 
- Задавать вопросы – самое простое мы обращаемся к нашему аналитику или заказчику (если есть такая возможность) и задаём уточняющие вопросы.
- Нарисовать схему – интеллект-карты (мы берём большое требование и разбиваем его на маленькие функциональности, а их ещё на более мелкие), Use-cases (так называемые варианты использования, которые описывают все действия, которые наш пользователь может произвести и реакцию системы на эти действия).
- Рецензирование – когда кто-то пишет требования и мы выступаем рецензором этого требования.

Способы представления (как они могут выглядеть):
- Use-cases – это перечень действий, сценарий по которому пользователь взаимодействует с приложением, программой для выполнения какого-либо действия для достижения конкретной цели.
- User story - это короткая формулировка намерения, описывающая что-то, что система должна делать для пользователя.
- Ui mockup – требования могут выглядеть непосредственно как mockup, шаблоны нашего ui - которого мы видим на экране.
- Спецификации - документ, устанавливающий требования. 

## 7. Отчет о дефекте. Severity и Priority. ЖЦ дефекта

Баг – это несоответствие фактического результата и ожидаемого.

Баг-репорт – это технический документ, который содержит в себе полное описание бага.
 
Атрибуты баг-репорта:
1. Id (уникальный номер);
2. Summary (оглавление, краткое описание);
3. Environment (окружение);
4. Preconditions (предварительные условия);
5. Step to reproduce (шаги для воспроизводства);
6. Expected result (ожидаемый результат);
7. Actual result (фактический результат);
8. Attachments (картинки, видео, логи – это текстовые файлы, в которых хранится информация о посещениях, параметрах посещений вашего сайта и ошибках, которые возникали на нем);
9. Priority (приоритет);
10. Severity (серьёзность);
11. Status (статус).
 
Серьёзность проблемы:
- Blocker — устанавливается, если баг блокирует дальнейшую работу приложения или процесс тестирования;
- Critical — присваивается при значительном влиянии проблемы на поведение ПО, но без блокировки его работы или процесса тестирования;
- Major — Весьма серьезная ошибка, свидетельствующая об отклонении от бизнес логики или нарушающая работу программы. Не имеет критического воздействия на приложение;
- Minor — Незначительный дефект, не нарушающий функционал тестируемого приложения, но который является несоответствием ожидаемому результату. Например, ошибка дизайна;
- Trivial – Баг, не имеющий влияние на функционал или работу программы, но который может быть обнаружен визуально. Например, ошибка в тексте.
 
Приоритет проблемы:
- High – исправить необходимо в первую очередь;
- Medium – требуется исправить, но не оказывает критическое воздействие на работу приложения;
- Low – исправить в последнюю очередь.
 
Жизненный цикл дефектов:
1. Новый (New). Тестировщик нашел баг, дефект успешно занесен в «Bug-tracking» систему;
2. Открыт (Opened). После того, как тестировщик отправил ошибку, она либо автоматически, либо вручную назначается на человека который должен её проанализировать (обычно Project Manager). В зависимости от решения менеджера проекта, баг может быть:
3. Отложен (Deferred). Исправление этого бага не несет ценности на данном этапе разработки или по другим, отсрочивающим его исправление причинам;
4. Отклонен (Rejected). По разным причинам дефект может и не считаться дефектом или считаться неактуальным дефектом, что вынуждает отклонить его;
5. Дубликат (Duplicate). Если описанная ошибка уже ранее была внесена в «Bug-tracking» систему, то статус такой ошибки меняется на «дубликат»;
6. Назначен (Assigned). Если ошибка актуальна и должна быть исправлена в следующей сборке (build), происходит назначение на разработчика который должен исправить ошибку;
7. Исправлен (Fixed). Ответственный за исправление бага разработчик заявляет, что устранил дефект. В зависимости от того, исправил ли разработчик дефект, дефект может быть:
8. Проверен (Verified). Тестировщик проверяет, действительно ли ответственный разработчик исправил дефект, или все-таки разработчик безответственный. Если бага больше нет, он получает данный статус;
9. Повторно открыт (Reopened). Если опасения тестировщика оправданы и баг в новом билде не исправлен – он все так же потребует исправления, поэтому заново открывается;
10. Закрытый (Closed). В результате определенного количества циклов баг все-таки окончательно устранен и больше не потребует внимания команды – он объявляется закрытым.

## 8. ТЕХНИКИ ТЕСТ-ДИЗАЙНА
 
Тест-дизайн – это этап процесса тестирования ПО, на котором проектируются и создаются тестовые случаи (тест-кейсы) в соответствии с определёнными ранее критериями качества и целями тестирования.
 
Тест-дизайнер должен выстроить процесс тестирования всех важнейших частей программного продукта, используя минимально возможное количество проверок.
 
Методики:
1. Тестирование Классами Эквивалентности (Equivalence Class Testing) - Тестовые данные разбиваются на определенные классы допустимых значений. В рамках каждого класса выполнение теста с любым значением тестовых данных приводит к эквивалентному результату. После определения классов необходимо выполнить хотя бы один тест в каждом классе.
____
2. Тестирование Граничных Значений (Boundary Value Testing) - Эта техника основана на том факте, что одним из самых слабых мест любого программного продукта является область граничных значений. Для начала выбираются диапазоны значений – как правило, это классы эквивалентности. Затем определяются границы диапазонов. На каждую из границ создается 3 тест-кейса: первый проверяет значение границы, второй – значение ниже границы, третий – значение выше границы.
____
3. Таблица Принятия Решений (Decision Table Testing) - способ компактного представления модели со сложной логикой; инструмент для упорядочения сложных бизнес требований, которые должны быть реализованы в продукте. Это взаимосвязь между множеством условий и действий.

В таблицах решений представлен набор условий, одновременное выполнение которых должно привести к определённому действию.
____
4. Тестирование Состояний и Переходов (State-Transition Testing) - Суть заключается в том что любая система находится в различных состояниях и определённые действия приводят к изменению этого состояния (Удобнее нарисовать и стрелками соединит там где должны быть переходы и где нельзя из одного состояния попасть в другое)
____
5. Метод Парного Тестирования (Pairwise testing) - Суть метода не в том, чтобы перебрать все возможные пары параметров, а в том, чтобы подобрать пары, обеспечивающие максимально эффективную проверку при минимальном количестве выполняемых тестов.
____
6. Доменный анализ (Domain Analysis Testing) - Это техника основана на разбиении диапазона возможных значений переменной (или переменных) на поддиапазоны (или домены), с последующим выбором одного или нескольких значений из каждого домена для тестирования. Во многом доменное тестирование пересекается с известными нам техниками разбиения на классы эквивалентности и анализа граничных значений. Но доменное тестирование не ограничивается перечисленными техниками. Оно включает в себя как анализ зависимостей между переменными, так и поиск тех значений переменных, которые несут в себе большой риск (не только на границах).
____
7. Сценарий использования (Use Case Testing) - Use Case описывает сценарий взаимодействия двух и более участников (как правило – пользователя и системы). Пользователем может выступать как человек, так и другая система. Для тестировщиков Use Case являются отличной базой для формирования тестовых сценариев (тест-кейсов), так как они описывают, в каком контексте должно производиться каждое действие пользователя. Use Case, по умолчанию, являются тестируемыми требованиями, так как в них всегда указана цель, которой нужно достигнуть, и шаги, которые надо для этого воспроизвести.

## 9. Аутентификация и авторизация

Идентификация - процедура, в результате выполнения которой для субъекта идентификации выявляется его идентификатор, однозначно определяющий этого субъекта в информационной системе (логин).

Аутентификация - процедура проверки подлинности, например проверка подлинности пользователя путем сравнения введенного им пароля с паролем, сохраненным в базе данных.

Авторизация - предоставление определенному лицу или группе лиц прав на выполнение определенных действий.

Популярные методы аутентификации:
- Проверка подлинности на основе пароля (Password-based authentication) - это простой метод проверки подлинности, требующий ввода пароля для подтверждения личности пользователя.
- Беспарольная аутентификация (Passwordless authentication) - это когда пользователь проверяется с помощью одноразового ПИН-а (OTP - One-time pins) или magic link, доставленной на зарегистрированный адрес электронной почты или номер телефона;
- Для двухфакторной аутентификации/многофакторной аутентификации (2FA/MFA) требуется более одного уровня безопасности, например дополнительный PIN-код или контрольный вопрос, для идентификации пользователя и предоставления доступа к системе;
- Единый вход (SSO) позволяет пользователям получать доступ к нескольким приложениям с одним набором учетных данных;
- Социальная аутентификация (Social authentication) проверяет и аутентифицирует пользователей с существующими учетными данными на платформах социальных сетей.
- Биометрия (Biometrics) - пользователь предъявляет отпечаток пальца или скан глаза, чтобы получить доступ к системе.

Популярные методы авторизации:
- Управление доступом на основе ролей (RBAC - Role-based access controls) может быть реализовано для управления привилегиями от системы к системе и от пользователя к системе.
- Веб-токен JSON (JWT - JSON web token) - это открытый стандарт для безопасной передачи данных между сторонами, а пользователи авторизуются с помощью пары открытый/закрытый ключ.
- SAML - это стандартный формат единого входа (SSO), в котором аутентификационная информация передается через XML-документы с цифровой подписью.
- Авторизация OpenID проверяет личность пользователя на основе аутентификации сервера авторизации;
- OAuth позволяет API аутентифицировать и получать доступ к запрошенной системе или ресурсу.
