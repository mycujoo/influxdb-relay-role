InfluxDB Relay Ansible role
=========

This role will install the influxdb relay with Ansible.

Requirements
------------

No additional requirements.

Role Variables
--------------

```
influxdb_relay_http_bind_address: 0.0.0.0
influxdb_relay_http_port: 9096

influxdb_relay_udp_enabled: True
influxdb_relay_udp_bind_address: 0.0.0.0
influxdb_relay_udp_port: 9096
influxdb_relay_udp_read_buffer: 0
influxdb_relay_udp_precision: "n"

influxdb_relay_ssl_certificate: ""


influxdb_relay_http_hosts:
  - { name: "localhost", "location": "localhost:8086/write", "timeout": 10s, "skip_tls_verification": false }

influxdb_relay_udp_hosts:
  - { name: "localhost", "location": "localhost:8089", "mtu": 512 }
```
Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: joshualund.golang }
         - { role: mycujoo.influxdb-relay-role }

License
-------

MIT
