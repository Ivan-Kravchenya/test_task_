1. Выполнить git pull 
2. Перейти в рабочий каталог
3. Выполнить docker-compose up -d
4. Выполнить ansible-playbook ansible.yaml --ask-become-pass
5. http://0.0.0.0/login - grafana 
6. http://0.0.0.0:3903/metrics - сбор метрик filestash файл /var/log/logstash/logstash-plain.log
   Например mtail_log_lines_total{logfile="/var/log/logstash/logstash-plain.log"}  - количество строк лога.
7. logstash собирает логи контейнеров prometheus и node exporter в фaйл 
 /var/log/test/containers.log
