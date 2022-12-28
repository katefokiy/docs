# Мониторинг и логи

#### За какими метриками и процессами можно следить с помощью мониторинга? {#monitoring-metrics}

Для всех типов СУБД можно отслеживать:

- загрузку процессора, памяти, сети, дисков в абсолютных величинах;
- загрузку памяти, сети, дисков в процентах от установленных лимитов для класса хостов соответствующего кластера;
- объем данных кластера БД и остаток свободного места в хранилище данных.

Для всех хостов БД можно отслеживать метрики, специфические для типа соответствующей СУБД. Например для {{ PG }} можно отслеживать:
- среднее время выполнения запроса;
- количество запросов в секунду;
- количество ошибок в журналах и т. д.

Мониторинг можно осуществлять с минимальной гранулярностью в 5 секунд.

#### Как тарифицируется хранение логов? {#logging-pricing}

Логи любого уровня пишутся на системный раздел диска, под который отведено 20 ГБ, поэтому не тарифицируются отдельно. Объем создаваемых логов влияет только на частоту их ротации.

{% include [log-duration](../../_includes/mdb/log-duration-qa.md) %}

#### Как следить за свободным объемом хранилища на хостах ZooKeeper? {#zookeeper-storage}

Воспользуйтесь инструкцией в разделе [{#T}](../../managed-clickhouse/operations/monitoring.md), чтобы отслеживать состояние хостов или настроить алерты.