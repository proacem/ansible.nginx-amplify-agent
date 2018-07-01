# Ansible Role: nginx_amplify_agent

[![Build Status](https://travis-ci.org/sbaerlocher/ansible.nginx_amplify_agent.svg?branch=master)](https://travis-ci.org/sbaerlocher/ansible.nginx_amplify_agent) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://sbaerlo.ch/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-nginx_amplify_agent-blue.svg)](https://galaxy.ansible.com/sbaerlocher/nginx_amplify_agent)

## Description

## Installation

```bash
ansible-galaxy install sbaerlocher.nginx_amplify_agent
```

## Requirements

## Role Variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| nginx_amplify_agent_api_key | |
| nginx_amplify_agent_hostname |  "{{ ansible_fqdn | default(ansible_hostname) }}" |
| nginx_amplify_agent_uuid | |
| nginx_amplify_agent_imagename | |
| nginx_amplify_agent_user | www-data |
| nginx_amplify_agent_configfile | /etc/nginx/nginx.conf |
| nginx_amplify_agent_stub_status | /nginx_status |
| nginx_amplify_agent_plus_status | |
| nginx_amplify_agent_exclude_logs | |
| nginx_amplify_agent_https | |
| nginx_amplify_agent_api_url | `https://receiver.amplify.nginx.com:443/1.3` | |
| nginx_amplify_agent_api_timeout | 5.0 |
| nginx_amplify_agent_phpfpm | true |
| nginx_amplify_agent_mysql | true |
| nginx_amplify_agent_mysql_host | |
| nginx_amplify_agent_mysql_port | |
| nginx_amplify_agent_mysql_unix_socket | /var/run/mysqld/mysqld.sock |
| nginx_amplify_agent_mysql_user | amplify-agent |
| nginx_amplify_agent_mysql_password | amplify-agent |
| nginx_amplify_agent_listers_keys | syslog-default
| nginx_amplify_agent_listener_syslog_default_address |
| nginx_amplify_agent_loggers_keys | root,devnull,agent-default |
| nginx_amplify_agent_handlers_keys | root,devnull,agent-default |
| nginx_amplify_agent_formatters_keys | simpleFormatter |
| nginx_amplify_agent_formatter_simpleFormatter_format | "%(asctime)s [%(process)d] %(threadName)s %(message)s" |
| nginx_amplify_agent_formatter_simpleFormatter_datefmt | |
| nginx_amplify_agent_logger_devnull_level | DEBUG |
| nginx_amplify_agent_logger_devnull_qualname | devnull |
| nginx_amplify_agent_logger_devnull_handlers | devnull |
| nginx_amplify_agent_logger_devnull_formatter | simpleFormatter |
| nginx_amplify_agent_logger_devnull_propagate | 0 |
| nginx_amplify_agent_handler_devnull_class | logging.handlers.WatchedFileHandler |
| nginx_amplify_agent_handler_devnull_level | DEBUG |
| nginx_amplify_agent_handler_devnull_formatter | simpleFormatter |
| nginx_amplify_agent_handler_devnull_args | ('/dev/null',) |
| nginx_amplify_agent_logger_root_level | DEBUG |
| nginx_amplify_agent_logger_root_handlers | root |
| nginx_amplify_agent_logger_root_qualname | root |
| nginx_amplify_agent_logger_root_formatter | simpleFormatter |
| nginx_amplify_agent_logger_root_propagate | 0 |
| nginx_amplify_agent_handler_root_class | logging.handlers.WatchedFileHandler |
| nginx_amplify_agent_handler_root_level | DEBUG |
| nginx_amplify_agent_handler_root_formatter | simpleFormatter |
| nginx_amplify_agent_handler_root_args | ('/dev/null',) |
| nginx_amplify_agent_logger_agent_default_level | INFO |
| nginx_amplify_agent_logger_agent_default_qualname | agent-default |
| nginx_amplify_agent_logger_agent_default_handlers | agent-default |
| nginx_amplify_agent_logger_agent_default_formatter | simpleFormatter |
| nginx_amplify_agent_logger_agent_default_propagate | 0 |
| nginx_amplify_agent_handler_agent_default_class | logging.handlers.WatchedFileHandler |
| nginx_amplify_agent_handler_agent_default_level | INFO |
| nginx_amplify_agent_handler_agent_default_formatter | simpleFormatter |
| nginx_amplify_agent_handler_agent_default_args | ('/var/log/amplify-agent/agent.log', 'a', None, 1) |

## Dependencies

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.nginx_amplify_agent
```

## Changelog

### 1.1

# renmae role

### 1.0.1

* update tags and defaults vars

### 1.0

* inital commit

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2017, Simon Bärlocher