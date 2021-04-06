---
description: План тестирования возможности открытия вклада «Накопилка»
---

# Внедрение автоматизации

{% hint style="info" %}
### Автоматизируемые сценарии
{% endhint %}

_QA_-инженер отталкивается от `user story`, поэтому тестироваться будет следующий UI-сценарий: клиент находится на основной странице сайта, затем переходит на страницу вкладов, и на ней нажимает вклад "Накопилка", где заполняет поля и нажимает кнопку "Мы перезвоним".

{% hint style="warning" %}
### Используемые инструменты
{% endhint %}

{% tabs %}
{% tab title="Selenide" %}
![](.gitbook/assets/image.png)



**Selenide** - фреймворк для автоматизированного тестирования веб-приложений на основе `Selenium WebDriver`, дающий следующие преимущества:

* [Изящный `API`](https://ru.selenide.org/documentation.html)`.`
* Поддержка `Ajax` для стабильных тестов.
* Мощные селекторы.
* Простая конфигурация.
* Не нужно заботиться о том, как закрыть браузер, обработать таймауты и `StaleElement Exceptions` или искать соответствующую строку в логах, отлаживая свои тесты.
{% endtab %}

{% tab title="Gradle" %}
![](.gitbook/assets/image%20%281%29.svg)

**Gradle** — система автоматической сборки \(инструмент для автоматизированного тестирования проектов `Java`\).

* Позволяет строить что угодно: писать на `Java`, `C++`, `Python` или на любом другом языке - пакет для развертывания на любой платформе. Позволяет использовать монорепозиторий или мультирепозиторий -  универсальность `Gradle` делает это возможным.
* Позволяет автоматизировать всё: богатый `API` `Gradle` и зрелая экосистема плагинов и интеграций даёт моделировать, интегрировать и систематизировать доставку программного обеспечения от начала до конца.
* Позволяет сделать доставку быстрее: разработку

  можно масштабировать с помощью быстрых сборок. От ухода от ненужной компиляции до расширенного кэширования и не только - разработчики `Gradle` постоянно стремятся к повышению производительности.
{% endtab %}

{% tab title="JUnit 5" %}
![](.gitbook/assets/image%20%281%29.png)

**JUnit** - среда модульного тестирования для языка программирования `Java`. Играет решающую роль в разработке, основанной на тестировании, и представляет собой семейство фреймворков модульного тестирования, известных под общим названием `xUnit`. `JUnit` продвигает идею «сначала тестирование, затем кодинг», что увеличивает производительность программиста и стабильность программного кода - что, в свою очередь, снижает нагрузку на программиста и снижает время, затрачиваемое на отладку. Особенности `JUnit`:

* Предоставляет аннотации для определения методов тестирования, `assertions` для тестирования ожидаемых результатов, средства запуска тестов.
* Тесты `JUnit` могут запускаться автоматически, проверяют свои собственные результаты и предоставляют обратную связь. Нет необходимости вручную просматривать отчёт о результатах тестирования.
* Тесты `JUnit` могут быть организованы в наборы тестов, содержащие тестовые примеры и даже другие наборы тестов.
{% endtab %}

{% tab title="Java" %}
![](.gitbook/assets/image%20%282%29.png)

**Java** - это технология, используемая для разработки приложений, которые делают работу в сети Интернет более увлекательной и удобной. Она протестирована, усовершенствована, расширена и проверена участниками сообщества разработчиков [Java](https://www.java.com/ru/download/), архитекторов и энтузиастов. [Java](https://www.java.com/ru/download/) позволяет разрабатывать высокопроизводительные портативные приложения практически на всех компьютерных платформах, и стала незаменимым инструментом для разработчиков и открыла для них следующие возможности:

* Написание программного обеспечения на одной платформе и его запуск практически на любой другой платформе.
* Создание программ, работающих в веб-браузере и имеющих доступ к веб-службам.
* Разработка приложений на стороне сервера для форумов в Интернете, магазинов, опросов, обработки форм `HTML` и много другого.
{% endtab %}

{% tab title="Katalon Studio" %}
![](.gitbook/assets/image.svg)

**Katalon Studio** \(_альтернативный вариант_\) - эффективный инструмент для автоматизирования процесса тестирования сайтов, веб-сервисов, мобильных приложений. Поддерживает миграцию в том числе и из `JUnit`.

Чтобы комфортно работать с этим инструментом, можно обладать как начальными знаниями в тестировании \(есть [Object Spy](https://docs.katalon.com/katalon-studio/docs/spy-web-utility.html)\), так и быть экспертом своего дела: для более опытных тестировщиков `Katalon Studio` станет весьма полезным инструментальным средством в плане экономии времени как при написании новых библиотек, так и при поддержке уже существующих скриптов.

`Katalon Studio` без проблем интегрируется в `CI/CD` и во время тестирования ПО работает с различными инструментами: `JIRA`, `Jenkins`, `qTest`, `Git`. Встроена функция `Katalon Analytics`, позволяющая получать полное представление о непосредственном процессе тестирования. Для этого на экран выводятся специальные отчёты, оформленные в виде графиков, метрик, диаграмм.
{% endtab %}
{% endtabs %}

{% hint style="success" %}
### Необходимые разрешения от банка
{% endhint %}

Потребуется лишь разрешение на тестирование и автоматизацию. Также можно запросить технические данные полей, чтобы заведомо понимать, какой ввод будет валидным, а какой - нет.

{% hint style="danger" %}
### Возможные риски при автоматизации
{% endhint %}

| Риск | Описание |
| :--- | :--- |
| Неоднозначность требований, неполнота или недостаточная подробность документации | Возникнут затруднения в долгосрочной перспективе |
| Неверный выбор инструментов для тестирования | При использовании нового инструмента с малоизвестным функционалом можно попасть в зависимость от технологий и специалистов |
| Проблемы с согласованиями | Если согласовывать нужно много и цепочка согласований большая |
| Проблемы с автоматизацией | Если строгие требования к безопасности: например, выполнение тестов в `CI` с использованием `VPN` |
| Проблемы с настройкой контейнеров и `CI` | Если нет специального человека для выполнения этих задач |

{% hint style="info" %}
### Необходимые специалисты
{% endhint %}

В первую очередь нужен достаточно опытный специалист, владеющий перечисленными выше инструментами, а также помощник начального уровня.

{% hint style="warning" %}
### Интервальная оценка с учётом рисков
{% endhint %}

Для двух специалистов \(опытный`+`помощник\) с запасом `15~25%` можно выделить **16** часов рабочего времени.