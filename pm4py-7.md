---
создал заметку: 25-06-24
tags:
  - Практика-pm4py
---
# pm4py tutorials - руководство №7 по обнаружению процессов

**Введение в процесс обнаружения** В этом руководстве мы рассмотрим обнаружение процессов с использованием различных моделей, таких как BPMN, деревья процессов, сети Петри и карты процессов. Мы рассмотрим, как считывать эти модели и обрабатывать шумы в алгоритмах. В текущем примере используется запрос на компенсацию за такие мероприятия, как концерты.

**Понимание моделей BPMN** Модели BPMN начинаются с начальной точки, отмеченной кружком с надписью "start". Действия следуют по дугам, ведущим через точки принятия решений (ромбы), указывающие на выбор или параллелизм (знаки плюс). Например, после регистрации запроса в нашем типовом примере: параллельные действия включают проверку заявок при тщательном или случайном рассмотрении запросов.

**Интерпретация данных о событиях** Журнал событий фиксирует хронологию выполнения процессов, описанных ранее. Каждая строка представляет время завершения действия, но не его продолжительность, что позволяет нам только предполагать последовательности, а не совпадения между задачами, выполняемыми одновременно в реальности.

**Алгоритм "индуктивного майнера" для обнаружения BPMNs** Алгоритм "индуктивного майнера" обнаруживает иерархические шаблоны из журналов событий, рекурсивно формируя структуры, которые могут быть легко преобразованы как в BPML, так и в деревья процессов из-за их строгой природы подмножества по сравнению с другими типами поведения, обнаруженными в них, что делает его простым, но эффективным инструментом при правильном применении к наборам данных, предоставленным во время самих обучающих программ!

**"Дерево процессов": Объяснено иерархическое представление.** Деревья процессов представляют обнаруженные поведения иерархически, где внутренние узлы обозначают операторы, определяющие последовательные / параллельные / циклические действия с выбором, среди прочего, позволяющие легко переводить их обратно между различными форматами, включая BPNM, обеспечивая согласованность представлений, используемых в примерах, приведенных здесь сегодня