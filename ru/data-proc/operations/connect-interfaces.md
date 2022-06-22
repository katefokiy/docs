# Подключение к интерфейсам компонентов

Вы можете подключиться к интерфейсам компонентов {{ dataproc-name }} либо с помощью [UI Proxy](#ui-proxy), либо с помощью [промежуточной виртуальной машины](#routing). Подробнее см. в разделе [{#T}](../concepts/interfaces.md).

## UI Proxy {#ui-proxy}

{% note warning %}

Для использования UI Proxy может потребоваться дополнительная [настройка групп безопасности](connect.md#configuring-security-groups).

{% endnote %}

### Включить веб-интерфейсы компонентов {#ui-proxy-enable}

{% list tabs %}

* Консоль управления

    1. Перейдите на [страницу каталога]({{ link-console-main }}) и выберите сервис **{{ dataproc-name }}**.
    1. Выберите кластер и нажмите кнопку ![pencil](../../_assets/pencil.svg) **Изменить кластер** на панели сверху.
    1. В блоке **Настройки** включите опцию **UI Proxy**.
    1. Нажмите кнопку **Сохранить изменения**.

* CLI

    {% include [cli-install](../../_includes/cli-install.md) %}

    {% include [default-catalogue](../../_includes/default-catalogue.md) %}

    Чтобы включить доступ к веб-интерфейсам компонентов кластера, задайте значение `true` для параметра `--ui-proxy`:

    ```bash
    yc dataproc cluster update <идентификатор или имя кластера> \
        --ui-proxy=<включение опции UI Proxy: true или false>
    ```

    Идентификатор и имя кластера можно получить со [списком кластеров в каталоге](cluster-list.md#list).

* API

    Воспользуйтесь методом [update](../api-ref/Cluster/update.md) и передайте в запросе:

    * Идентификатор кластера в параметре `clusterId`. Его можно получить [со списком кластеров в каталоге](cluster-list.md#list).
    * Значение `true` в параметре `uiProxy`.
    * Список полей конфигурации кластера, подлежащих изменению (в данном случае — `uiProxy`), в параметре `updateMask`.

    {% include [Note warning update mask](../../_includes/mdb/note-api-updatemask.md) %}

{% endlist %}

### Получить список URL для подключения {#ui-proxy-list}

{% list tabs %}

* Консоль управления

    1. Перейдите на [страницу каталога]({{ link-console-main }}) и выберите сервис **{{ dataproc-name }}**.
    1. Нажмите на имя нужного кластера.
    1. Ссылки для подключения к веб-интерфейсам компонентов находятся в блоке **UI Proxy**.

* CLI

    {% include [cli-install](../../_includes/cli-install.md) %}

    {% include [default-catalogue](../../_includes/default-catalogue.md) %}

    Чтобы получить список URL для подключения к веб-интерфейсам компонентов кластера {{ dataproc-name }}, выполните команду:

    ```bash
    yc dataproc cluster list-ui-links <идентификатор или имя кластера>
    ```

    Идентификатор и имя кластера можно получить со [списком кластеров в каталоге](cluster-list.md#list).

* API

    Воспользуйтесь методом API [listUILinks](../api-ref/Cluster/listUILinks.md) и передайте идентификатор кластера в параметре `clusterId` запроса.

    Идентификатор кластера можно получить со [списком кластеров в каталоге](cluster-list.md#list).

{% endlist %}

## Перенаправление портов {#routing}

Чтобы получить доступ к сетевому интерфейсу компонента из интернета, [создайте](../../compute/operations/vm-create/create-linux-vm.md) промежуточную виртуальную машину в сервисе {{compute-full-name}}.

Требования к промежуточной ВМ:

* Наличие публичного IP-адреса.
* Размещение в одной сети с нужным кластером {{ dataproc-name }}.
* [Настройки групп безопасности](../concepts/network.md#security-groups) должны разрешать обмен трафиком с кластером через порты соответствующих компонентов.

Пошаговые инструкции по настройке групп безопасности для перенаправления портов приведены в разделе [{#T}](connect.md#configuring-security-groups).

Чтобы соединиться с нужным портом хоста {{ dataproc-name }}, выполните команду:

```bash
ssh -A \
    -J <публичный IP-адрес ВМ> \
    -L <номер порта>:<FQDN хоста Data Proc>:<номер порта> <имя пользователя>@<FQDN хоста Data Proc>
```

Где:

* `-A` — включает перенаправление соединения от агента аутентификации с промежуточной ВМ (jump host) на целевой хост кластера {{ dataproc-name }}.
* `-J` — подключение к целевому хосту через промежуточную ВМ. Устанавливает SSH-соединение с промежуточной ВМ, которая будет перенаправлять пакеты к целевому хосту в кластере {{ dataproc-name }}.
* `-L` — перенаправление локального порта на хост кластера {{ dataproc-name }}.

    Для подключения к хостам кластера с [версией образа](../concepts/environment.md) 1.x используйте имя пользователя `root`, для версии 2.x — `ubuntu`.

Найти FQDN хоста {{ dataproc-name }} можно на странице кластера {{ dataproc-name }}, на вкладке **Хосты**, в столбце **Имя хоста**.

Номера портов для компонентов {{ dataproc-name }} приведены в разделе [Интерфейсы и порты компонентов](../concepts/interfaces.md#port-numbers).