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

