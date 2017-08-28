# Ansible Role: Kibana

Ansible role for installing Kibana on CentOS

## Requirements
Oracle JVM 1.8u40+

or

IcedTea OpenJDK 1.8.0.91+

## Variables
|Variable Name | Default Value |
|:------------|:-------|
`kb_yum_repo_baseurl` | `https://artifacts.elastic.co/packages/5.x/yum`
`kb_yum_repo_gpgkey` | `https://artifacts.elastic.co/GPG-KEY-elasticsearch`
`kb_server_port` | `5601`
`kb_server_host` | `localhost`
`kb_server_name` | `"{{ inventory_hostname }}"`
`kb_elasticsearch_url` | `http://localhost:9200`
`kb_logging_dest` | `/var/log/kibana/kibana.log`

## Usage
```
roles:
  - role: erumble.kibana
    kb_server_host: 0.0.0.0
    kb_logging_dest: /var/log/kibana.log
```
