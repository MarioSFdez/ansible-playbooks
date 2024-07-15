# ansible-playbooks
Este repositorio contiene varios playbooks de Ansible para automatizar diversas tareas de configuración y gestión de sistemas.  

## Utilización
Cada playbook está diseñado para ejecutar tareas específicas mediante Ansible.  
Asegúrate de revisar los archivos de configuración y adaptarlos según las necesidades de tu infraestructura.

Modifica el fichero [hosts](cluster-swarm-ansible/hosts) con las direcciones IP correspondientes
```
[swarm_manager]
192.168.0.22

[swarm_worker]
192.168.0.20
192.168.0.21
```
Ejecuta el playbook de Ansible indicando el fichero `hosts` y el archivo principal `swarm-ansible.yml`
```
ansible-playbook -i hosts swarm-ansible.yml
```

## Archivos
- **[cluster-swarm-ansible:](cluster-swarm-ansible)** Configuración del clúster Swarm.
- **[actualizar-paquetes.yml](actualizar-paquetes.yml):** Playbook para la actualización de paquetes.
- **[backup-rsync.yml](backup-rsync.yml):** Playbook para copias de seguridad utilizando rsync.
- **[lamp-netdata.yml](lamp-netdata.yml):** Configuración para la pila LAMP con Netdata.
