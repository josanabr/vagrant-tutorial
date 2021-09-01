# 05-multiple-vms

En el archivo `Vagrantfile` se describen dos máquinas virtuales `web` y `db`.
Para crear las dos máquinas solo se ejecuta el comando

```
vagrant up
```

Al finalizar la ejecución del comando usted tendrá dos máquinas virtuales en ejecución.

Para acceder a la máquina via SSH deberá especificar la máquina a la cual quiere acceder, por ejemplo 

```
vagrant ssh web
```

Ingresará por SSH a la máquina virtual `web`. 

Usted podrá borrar todas las máquinas virtuales ejecutando el comando

```
vagrant destroy -f
```

O puede borrar solo una máquina virtual

```
vagrant destroy -f db
```

Así mismo usted puede crear nuevamente dicha máquina a través del comando

```
vagrant up db
```
