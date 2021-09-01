# 03-provisioning

En este directorio encontrará un archivo de Vagrant (`Vagrantfile`) que muestra como se especifica el aprovisionamiento de software adicional en la máquina virtual.
En este caso desde el `Vagrantfile` se procede a ejecutar las instrucciones que se encuentran en el archivo `script.sh`.
En `script.sh` se encuentran los pasos que permiten la instalación del servidor web de Apache.

Para crear la máquina virtual, ejecutar el comando

```
vagrant up
```

Una vez termina la ejecución del comando anterior, ingrese a la máquina virtual (`vagrant ssh`) y ejecutar el siguiente comando

```
wget http://localhost
```

El comando deberá acceder al servidor web corriendo en la máquina virtual y como evidencia se debió generar un archivo llamado `index.html`.
Este archivo contiene la página principal del servidor web de Apache.

Vagrant permite hacer el aprovisionamiento no solo con scripts sino que también soporta otras herramientas de aprovisionamiento como: Puppet, Chef y Ansible.
