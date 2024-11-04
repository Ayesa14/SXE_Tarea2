# Tarea 2
## 1. Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo
```bash
sudo docker image pull alpine
sudo docker image ls
```
## 2. Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre
```bash
//Crea un contenedor sin nombre
sudo docker container create alpine
//Listar contenedores
sudo docker ps -a
```
El nombre del contenedor se genera de manera aleatoria

