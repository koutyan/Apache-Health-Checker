# Apache-Health-Checker
Monitor the connection to the Apache server and restart apache if there is a problem.

Other web server software can be supported by changing the `service_name` parameter in `vars.yml`.

It is assumed to be run periodically by cron. (`$ crontab -e`)

(Example)
```
$ crontab -l
# Edit this file to introduce tasks to be run by cron.

30 * * * * cd /home/ubuntu/Apache-Health-Checker/ && ansible-playbook playbook.yml > /home/ubuntu/Apache-Health-Checker/mycron.log 2>&1
```