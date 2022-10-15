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
