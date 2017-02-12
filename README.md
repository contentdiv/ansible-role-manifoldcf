# ansible-role-manifoldcf

Role to install Apache ManifoldCF with Postgres


#### Installation

This has been tested on Ansible 2.1.2.0.


#### Dependencies

- ANXS.postgresql ([Galaxy](https://galaxy.ansible.com/ANXS/postgresql/)/[GH](https://github.com/ANXS/postgresql))
- williamyeh.oracle-java ([Galaxy](https://galaxy.ansible.com/williamyeh/oracle-java/)/[GH](https://github.com/William-Yeh/ansible-oracle-java))

#### Variables

```yaml

# Basic settings

install_owner_name: itadmin
install_owner_password: xxxxxx
install_os_group: itadmin
install_software_tempdir: /home/itadmin/software
installation_mode: single
installation_database: postgres

mcf_install_dir: /opt/manifoldcf/
mcf_apache_download_base_url: http://archive.apache.org/dist/manifoldcf/apache-manifoldcf-
mcf_version: 2.6

jcifs_version: 1.3.18

postgres_version: 9.5
postgresql_admin_user: postgres
postgresql_admin_password: postgres
postgresql_db_port: 5432

service_name: mcf-contentdiv


```

Refer to the defaults/main.yml for more settings.


#### Testing

This project comes with a Vagrantfile, this is a fast and easy way to test changes to the role, fire it up with `vagrant up`

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with vagrant

Once your VM is up, you can reprovision it using either `vagrant provision`, or `ansible-playbook mcf-agents.yml -i dev`

#### License

Licensed under the Apache License. See the [LICENSE](./LICENSE) file for details.


#### Thanks


#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/contentdiv/ansible-role-manifoldcf/issues)!
