=== Woocommerce retailCRM ===
Contributors: retailCRM
Donate link: http://retailcrm.ru/
Tags: Интеграция, retailCRM
Requires PHP: 5.3
Requires at least: 4.4
Tested up to: 5.3
Stable tag: 3.5
License: GPLv1 or later
License URI: http://www.gnu.org/licenses/gpl-1.0.html

== Description ==

= Возможности плагина =

Плагин для интеграции Woocommerce и Retailcrm. Плагин позволяет сгенерировать каталог товаров для выгрузки в Retailcrm, настроить двусторонний обмен заказами Woocommerce и Retailcrm, отправлять и принимать изменения по заказам, выгружать остатки из Retailcrm в магазин. При включении функции выгрузки остатков каждые 15 минут остатки по товарам будут выгружаться в магазин (настройка имеет смысл при включении ручного редактирования остатков в Retailcrm, остатки из магазина выгружаются вместе с каталогом товаров каждые 4 часа). Внимание!!! При включении выгрузки остатков плагин включит управление остатками для товаров. Товары, отсутствующие на складе будут скрыты на сайте для посетителей.

= Выгрузка изменений из Retailcrm =

Каждые 5 минут плагин подгружает изменения из Retailcrm в Woocommerce.

= Кастомизация =

Вы можете вносить изменения в базовые классы плагина, разместив копию класса из дериктории include в директории wp-content/retailcrm-custom.

== Installation ==

= Активация и настройка =

После активации плагина необходимо открыть настройки Woocommerce, выбрать вкладку "Интеграция" и в настройках RetailCRM указать адрес CRM (например https://example.retailcrm.ru) и API-ключ, сгенерированный в CRM (инструкция по добавлению ключа в CRM - http://www.retailcrm.ru/docs/Users/ApiKeys), выбрать желаемую версию API (API v5 доступна только c версии Retailcrm 6.0 и выше)

== Frequently Asked Questions ==

= Нет списка справочников для настройки соответствия =

Проверьте, что для созданного API-ключа доступны все методы

= Заказы не попадают в Retailcrm =

API-ключ должен быть для отдельного магазина

== Screenshots ==

1. Введите адрес CRM, API-ключ и выберите версию API, нажмите на кнопку сохраниения настроек. Если после сохранения не появилось никаких других настроек, обновите страницу.
2. В появившихся списках справочников настройте соответствие способов доставки и оплаты, а так же статусов заказов. Отметьте галочку "Выгружать остатки", если хотите выгружать остатки из Retailcrm в магазин (подробнее смотрите в описании).

== Changelog ==
= 3.6.2 =
* Исправлена ошибка, которая приводила к дублированию некоторых клиентов

= 3.6.1 =
* Исправлена ошибка генерации каталога товаров

= 3.6.0 =
* Добавлена настройка передачи суммы оплаты в retailCRM

= 3.5.2 =
* Исправлен баг с выгрузкой заказов в retailCRM

= 3.5.1 =
* Исправлен баг при активации плагина

= 3.5.0 =
* Добавлена настройка деактивации выгрузки изменений заказа в retailCRM
* Добавлена настройка активации выгрузки SKU в xmlId и связь товаров по полю xmlId
* Добавлена настройка передачи номера заказа в retailCRM

= 3.4.5 =
* Исправлен баг с добавлением скидки при уменьшении количества товара в retailCRM

= 3.4.4 =
* Добавлена генерация уникального id к внешнему id отправляемой оплаты при использовании 5 версии api

= 3.4.3 =
* Исправлено сохранение типа оплаты при создании заказа при обработке истории изменений на стороне WC
* Исправлено сохранение типа оплаты при ризменении заказа при обработке истории изменений на стороне WC

= 3.4.2 =
* Исправлено изменение типа оплаты на стороне WC
* Добавлен вывод неактивных типов оплаты в настройках

= 3.4.1 =
* Исправлены некоторые ошибки

= 3.4.0 =
* Добавлена настройка Daemon Collector
* Изменена логика передачи данных по заказам и клиентам. Данные доставки передаются в заказ, данные оплаты в карточку клиента.

= 3.3.8 =
* Добавлена выгрузка картинок для категорий товаров в ICML

= 3.3.7 =
* Исправлен баг активации модуля интеграции

= 3.3.6 =
* Исправлена активация модуля в маркетплейсе retailCRM при использовании api v4

= 3.3.5 =
* Добавлена активация модуля в маркетплейсе retailCRM

= 3.3.4 =
* Улучшена обработка истории заказов

= 3.3.3 =
* Добавлены кнопки для перехода в настройки плагина и для генерации каталога в админ-панели wordpress
* Улучшена механика передачи данных оплаты заказа

= 3.3.2 =
* Задачи в wp-cron теперь активируются в настройках плагина

= 3.3.1 =
* Исправлена ошибка с дублированием товаров с WC

= 3.3.0 =
* Переработана механика обработки истории изменений

= 3.2.0 =
* Улучшен метод выборки данных о доставках и оплатах в настройках плагина
* Исправлены ошибки при обработке истории изменений
* Добавлены тесты для обработки истории изменений

= 3.1.1 =
* Исправлен код отправки данных в UA
* Добавлены новые фильтры, добавлена передача новых параметров в существущие

= 3.1.0 =
* В интерфейс настроек плагина добавлена возможность ручной выгрузки заказов
* Исправлена инициализация кода UA для отправки заказов на всех страницах

= 3.0.0 =
* Произведен рефакторинг кода

= 2.1.4 =
* Исправлена ошибка при активированном модуле без настроек
* Добавлен фильтр при формировании массива заказа
* Исправлена генерация icml с неполной картинкой товара

= 2.1.3 =
* Исправлена ошибка на php5.3

= 2.1.2 =
* Добавлена локализация плагина
* Добавлена интеграция с UA

= 2.1.1 =
* Исправлена ошибка с редактированием клиента

= 2.1.0 =
* Переработана механика генерации icml каталога товаров
* В icml каталог добавлена выгрузка налоговой ставки
* Исправлен пересчет итогов после изменения количества товара в RetailCRM

= 2.0.6 =
* Исправлено возникновение Warning на PHP 7.2 при генерации каталога товаров
* Добавлена настройка выгрузки заказов из RetailCRM с определенными способами оформления
* Выгрузка изменений из RetailCRM осуществляется по sinceId

= 2.0.5 =
* Исправлен неверный подсчет скидки на товары

= 2.0.4 =
* Улучшена механика пакетной выгрузки клиентов и заказов
* Добавлена возможность выгрузки заказов с товарами, которые уже удалены с сайта

= 2.0.3 =
* Изменен механизм рассчета стоимости товара в заказе
* Улучшена передача информации об изменениях в заказе
* Устранены мелкие баги

= 2.0.2 =
* Изменен механизм передачи скидок в CRM

= 2.0.1 =
* Добавлена выгрузка размеров товаров
* Улучшена выгрузка веса товаров
* Улучшена механика выгрузки заказов из CRM

= 2.0.0 =
* Улучшен поиск типов доставок на сайте
* Добавлена кнопка генерации icml каталога в настройках плагина
* Переработан механизм выгрузки заказов из CRM
* Улучшена генерация каталога, добавлена выгрузка размеров

= 1.2.3 =
* Добален опциональный выбор статусов товаров, выгружаемых в каталоге
* Улучшен механизм формирования цены товара в заказе (с учетом скидок и налогов)

= 1.2.2 =
* Исправлены ошибки

= 1.2.1 =
* Доработана система кастомизации.

= 1.2.0 =
* Улучшена возможность кастомизации плагина.
* Добавлена возможность кастомизации обработки остатков, клиентов и истории.

= 1.1 =
* Добавлена возможность выбора версии API.
* Исправелены ошибки.

== Upgrade Notice ==
= 3.6.0 =
Добавлена возможность отключить передачу суммы оплаты в retailCRM, тогда сумма будет рассчитываться в retailCRM

= 3.4.2 =
Исправлено изменение типа оплаты на стороне WC
Добавлен вывод неактивных типов оплаты в настройках

= 3.4.0 =
Внедрен Daemon Collector

= 3.3.5 =
После обновления плагина необходимо пересохранить настройки для того, чтобы активировать модуль в маркетплейсе retailCRM

= 3.3.4 =
Улучшена обработка истории заказов

= 3.3.3 =
Добавлены кнопки для перехода в настройки плагина и для генерации каталога в админ-панели wordpress
Улучшена механика передачи данных оплаты заказа

= 3.3.2 =
Добавлена настройка для активации задач в wp-cron

= 3.3.1 =
Исправлена ошибка с дублированием товаров с WC

= 3.3.0 =
Переработана механика обработки истории изменений

= 3.2.0 =
Улучшен метод выборки данных о доставках и оплатах в настройках плагина
Исправлены ошибки при обработке истории изменений
Добавлены тесты для обработки истории изменений

= 3.1.1 =
Исправлен код отправки данных в UA
Добавлены новые фильтры, добавлена передача новых параметров в существущие

= 3.1.0 =
В интерфейс настроек плагина добавлена возможность ручной выгрузки заказов

= 3.0.0 =
Произведен рефакторинг кода

= 2.1.4 =
Исправлена ошибка при активированном модуле без настроек
Добавлен фильтр при формировании массива заказа
Исправлена генерация icml с неполной картинкой товара

= 2.1.3 =
Исправлена ошибка на php5.3

= 2.1.2 =
Добавлена локализация плагина
Добавлена интеграция с UA

= 2.1.1 =
Исправлена ошибка с редактированием клиента

= 2.1.0 =
Переработана механика генерации icml каталога товаров
В icml каталог добавлена выгрузка налоговой ставки
Исправлен пересчет итогов после изменения количества товара в RetailCRM

= 2.0.6 =
Исправлено возникновение Warning на PHP 7.2 при генерации каталога товаров
Добавлена настройка выгрузки заказов из RetailCRM с определенными способами оформления

= 2.0.4 =
Улучшена механика пакетной выгрузки клиентов и заказов
Добавлена возможность выгрузки заказов с товарами, которые уже удалены с сайта

= 2.0.3 =
Изменен механизм рассчета стоимости товара в заказе
Улучшена передача информации об изменениях в заказе
Устранены мелкие баги

= 2.0.2 =
Изменен механизм передачи скидок в CRM

= 2.0.1 =
Добавлена выгрузка размеров товаров
Улучшена выгрузка веса товаров
Улучшена механика выгрузки заказов из CRM

= 2.0.0 =
Улучшен поиск типов доставок на сайте
Добавлена кнопка генерации icml каталога в настройках плагина
Переработан механизм выгрузки заказов из CRM
Улучшена генерация каталога, добавлена выгрузка размеров

= 1.2.3 =
Исправлены ошибки, доработан функционал
