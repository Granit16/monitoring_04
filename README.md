# Домашнее задание к занятию 15 «Система сбора логов Elastic Stack»

## Задание 1

С помощью **docker** запустил и связал между собой:
 - elasticsearch (hot и warm ноды);
 - logstash;
 - kibana;
 - filebeat.
   
**Logstash** сконфигурирован для приёма по tcp json-сообщений.

**Filebeat** сконфигурирован для отправки логов docker в **Logstash** ```/var/lib/docker/containers/*/*.log```.

Cкриншот ```docker ps```:

![](https://github.com/Granit16/monitoring_04/blob/main/docker_ps.png)


Cкриншот интерфейса **Kibana**:

![](https://github.com/Granit16/monitoring_04/blob/main/kibana.png)


## Задание 2

Создал несколько index-patterns:
 - Все логи: ```log*```
 - Логи от 27.01.2025 г.: ```logstash-2025.01.27```

С помощью инструмента **Discover** изучил, как отображаются логи, как производить поиск по логам, полученным от dummy-приложения, которое генерирует рандомные события в stdout-контейнера.
