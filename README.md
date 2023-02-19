# Ansible Role: Docker Volumes

Ansible role to manage Docker volumes via inventory.

## Variables
### Defaults
Default values are located in ```defaults/main.yml```.

## Examples
```
docker_volumes:
  - name: foo
    driver_options:
      type: tmpfs
      device: tmpfs
  - name: bar
  - name: foobar
    driver: some_driver
```
Volumes listed within ```docker_volumes``` will be created. The default driver is the loacal driver.
All options regarding volume creation should be supported (e.g Volume Name, Labels, Drivers, Driver Options etc.).


```
docker_volumes_deleted:
  - name: foo
  - name: bar
```
Volumes listed within ```docker_volumes_deleted``` will be deleted on the next run. 
