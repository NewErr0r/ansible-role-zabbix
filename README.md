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
