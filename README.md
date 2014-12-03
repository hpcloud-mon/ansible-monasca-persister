#monasca-persister
Installs the [monasca-persister](https://github.com/stackforge/monasca-persister) part of the [Monasca](https://wiki.openstack.org/wiki/Monasca) project.

##Requirements
Requires Variables be defined for:
- zookeeper_uri - A comma seperated list of kafka hosts with optional port
- kafka_uri - A comma seperated list of kafka hosts with optional port
- influxdb_host
- influxdb_user
- influxdb_password

##Example Playbook

    hosts: monasca
    sudo: yes
    roles:
      - {role: tkuhlman.monasca-persister,
         kafka_uri: "{{kafka_hosts}}",
         influxdb_user: "{{persister_influxdb_user}}",
         influxdb_password: "{{persister_influxdb_password}}",
         tags: [persister]}
    

##License
Apache

##Author Information
Tim Kuhlman
Monasca Team email monasca@lists.launchpad.net
