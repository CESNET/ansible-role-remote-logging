# Ansible role cesnet.remote_logging

Ansible role for remote logging to a central server using syslog-ng.

The role installs syslog-ng on Debian system, and configures it to send logs to a remote server.

The default values of variables match settings for CESNET's central server, connecting over IPv6.

To connect to the logging server over IPv4, set:

`remote_logging_server_ip_version: 4`

You can configure extra templates by setting `remote_logging_extra_templates` variable, without .j2 suffix.
Pre-defined templates:

- `postgresql_json` configures PostgreSQL JSON log forwarding from `/var/log/postgresql/postgresql*.json`