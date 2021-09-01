# 04-port-forwarding

Este ejemplo muestra una combinación de la capacidad de Vagrant de aprovisionar máquinas y de hacer redirección de puertos.
De este modo, cuando se invoque el comando `vagrant up`, se creará una máquina virtual que tiene el servidor web de Apache2 corriendo por el puerto 80 de la máquina virtual pero que se podrá acceder desde el anfitrión (*host*) por el puerto 8080.
Ejecutar el comando

```
vagrant up
```

Una vez termine la ejecución de este comando, abra una ventana de su navegador y vaya al sitio `http://localhost:8080`.
Se deberá mostrar la página web principal del servidor web corriendo en la máquina virtual.
