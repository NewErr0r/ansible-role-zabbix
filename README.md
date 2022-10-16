<h1>Автоматизация развёртывания платформы мониторинга "Zabbix"</h1>

<p>
    <strong>Шаг 1.</strong> Создание playbook для запуска роли
</p>
<p><i>Пример:</i></p>

    ---
    - name: Deploy Zabbix-Server
      hosts: all 
      become: true 

      roles: 
        - ansible-role-zabbix

<p>
    <strong>Шаг 2.</strong> Склонировать роль в дирректорию с playbook:
</p>

  <pre>git clone https://github.com/NewErr0r/ansible-role-zabbix.git</pre>

<p>

<p>
    <strong>Шаг 3.</strong> Запустить скрипт инициализирующий необходимые переменные:
</p>
 
 <pre>./ansible-role-moodle/configure.variables</pre>
 <i>1. Задать пароль MariaDB для пользователя root</i><br>
 <i>2. Задать имя базы данных MariaDB для zabbix</i><br>
 <i>3. Задать имя пользователя MariaDB для zabbix </i><br>
 <i>4. Задать пароль для этого пользователя </i>
 
 <p>
    <strong>Шаг 4.</strong> Запустить playbook для развёртывания платформы мониторинка Zabbix:
</p>
  
  <pre>ansible-playbook -i inventory playbook.yaml</pre>
