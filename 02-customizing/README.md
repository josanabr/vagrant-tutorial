# 02-customizing

En el archivo [Vagrantfile](Vagrantfile) se muestra la sintaxis para modificar las características de una máquina virtual creada con Vagrant pero que se gestiona con VirtualBox.

```
vagrant up
```

Una vez que termine la ejecución del comando y para validar la creación efectiva de la máquina virtual se puede ejecutar el comando

```
VBoxManage list vms
```

Allí debe aparecer el nombre de la máqina `mi-mv`.
Ingrese a la máquina y valide que efectivamente tiene las características descritas en el archivo [Vagrantfile](Vagrantfile).

**Nota** este [Vagrantfile](Vagrantfile) crea una máquina con unas características muy particulares. Cerciórese que su máquina física podrá cumplir con las expectativas declaradas en el [Vagrantfile](Vagrantfile).
