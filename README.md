# Vagrant tutorial

[Video]() describiendo el material de este repositorio.

[Diapositivas](https://docs.google.com/presentation/d/1g9kRku-64QvUWoNkAD_3QZ4aqFud8xjtvd77z09Srbg/edit?usp=sharing) usadas en el video para presentar este contenido.

En este repositorio encontrará diferentes directorios donde verá algunos ejemplos donde se presentan algunas de las capacidades de la herramienta Vagrant.

Vagrant interactúa con diferentes hypervisors. 
Para los efectos de esta guía, se usará la herramienta [VirtualBox](https://www.virtualbox.org/). 
Una vez instalado se procede a instalar Vagrant.

Para llevar a cabo la instalación de Vagrant por favor visitar este [enlace](https://www.vagrantup.com/docs/installation).
Para validar que su herramienta está correctamente instalada ejecute el comando

```
vagrant -v
```

Para crear las máquinas virtuales se requiere de un box el cual es un archivo que contiene una plantilla de una máquina virtual preconfigurada. 
A partir de un box es que se generan o se construyen nuevas máquinas virtuales. 
Para listar las boxes disponibles se ejecuta

```
vagrant box list
```

Para adicionar una box a su entorno de trabajo, ejecutar

```
vagrant box add ubuntu/focal64
```

## IMPORTANTE

En los siguientes ejemplos que están en los correspondientes directorios, usted ejecutará el comando `vagrant up` para crear la máquina virtual.
Para ingresar a la máquina virtual ejecuta el comando

```
vagrant ssh
```

Estará usted al interior de la máquina y puede jugar en ella y explorar un poco al respecto.
Se sale de esta máquina con el comando `exit`, el comando usual para salir de una sesión de terminal.

Para destruir las máquinas creadas, ejecutar el comando

```
vagrant destroy -f
```

La opción `-f` es para indicarle a Vagrant que se está seguro del borrado de la máquina virtual.

---

## Ejemplos 

* [01-minimal](01-minimal) La versión mínima que necesita Vagrant para crear una máquina virtual.

* [02-customizing](02-customizing) En este directorio usted podrá encontrar como se puede personalizar la creación de una máquina virtual. Por ejemplo, cambiar la cantidad de RAM, el número de procesadores, el nombre de la máquina, entre otros. 

* [03-provisioning](03-provisioning) Vagrant permite que además de crear la máqiina virtual, una vez se termina de crear se proceda con la instalación de software adicional. En este directorio se ejemplifica esta capacidad de la herramienta Vagrant.

* [04-port-forwarding](04-port-forwarding) Vagrant permite que al momento de crear el ambiente virtual, un puerto de la máquina virtual quede asociado con un puerto del equipo anfitrión.

* [05-multiple-vms](05-multiple-vms) Vagrant tiene la posibilidad de crear múltiples máquinas definidas en el `Vagrantfile`.

---

## Otros comandos bastante útiles

* `vagrant halt` detiene la ejecución de la(s) maquina(s) virtual(es) definida(s) en el `Vagrantfile`.

* `vagrant snapshot push` saca una copia del estado actual de una máquina virtual, esté en ejecución o esté detenida.

* `vagrant snapshot pop` este comando se ejecuta exitosamente siempre y cuando se haya sacado previamente una copia del estado de una máquina virtual. El comando `vagrant snapshot pop` restaura el estado de la máquina al momento en el que se invocó el comando `vagrant snapshot push`.
