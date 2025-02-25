## Заголовок:

ADR-6: Использовать MessageBroker (Kafka) для организации асинхронного взаимодействия сервисов по модели pub/sub.

## Статус:

Предложение

## Контекст:

В контексте потребностей бизнеса требуется решить задачи снижения нагрузки на систему SD и быстродействия, связанную с пиками по утилизации ресурсов.

## Альтернативы:

1. Использовать синхронное межсервисное взаимодействие.


## Оценка:

Условные обозначения:

- ++ Хорошо
- +- Средне
- -- Плохо

| # | 1 - Sync | 2 - Async |
|----|----|----|
| Производительность | +- | ++ |
| Масштабируемость | +- | ++ |
| Надежность | +- | ++ |
| Стоимость владения | +- | +- |

## Решение:

Основываясь на оценке альтернативных вариантов в контексте потребностей бизнеса предлагается использовать вариант №2 - асинхронное взаимодействие сервисов.
Данное решение позволит повысить производительность функционала Клиенсткого портала и снизить нагрузку на систему ServiceDesk.

## Риски:

* Стоимость владения системой может увеличится в связи необходимостью технической поддержки и обслуживания брокера сообщений.
* Возможно потребуется привлекать к реализации компанию-интегратора или нанимать разработчиков.