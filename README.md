# devops


## PROD

Update inventory/hosts file with your target servers in respective groups 

```
[airflow_prod]
localhost

[airflow_dev]
localhost
```


### To install airflow in prod run below command 

```bash 
ansible-playbook playbooks/airflow_setup.yml -e "host_group=airflow_prod" -vv
```

### To uninstall airflow in dev run below command

```bash
ansible-playbook playbooks/airflow_setup.yml -e "host_group=airflow_prod airflow_setup_state=absent" -vv
```

##Dev

### To install airflow in dev run below command

```bash
ansible-playbook playbooks/airflow_setup.yml -e "host_group=airflow_dev" -vv
```

### To uninstall airflow in dev run below command

```bash
ansible-playbook playbooks/airflow_setup.yml -e "host_group=airflow_dev airflow_setup_state=absent" -vv
```
