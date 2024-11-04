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

## 3. Crea un contenedor con el nombre 'dam_alp1'. ¿Cómo puedes acceder a él?
```bash
//Crea un contenedor que se mantenga en ejecución
sudo docker run -d --name dam_alp1 alpine tail -f /dev/null
//Acceder al contenedor
sudo docker exec -it dam_alp1 sh
```
## 4. Comprueba que ip tiene y si puedes hacer un ping a google.com
```bash
//Comprobar la ip. En la sección "Networks" se puede ver la ip
sudo docker inspect dam_alp1
//Hacer ping
sudo docker exec -it dam_alp1 ping google.com
```
## 5. Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?
```bash
//Crea un contenedor que se mantenga en ejecución
sudo docker run -d --name dam_alp2 alpine tail -f /dev/null
//Hacer ping entre contenedores
sudo docker exec -it dam_alp1 ping
```
## 6. Sal del terminal, ¿que ocurrió con el contenedor?
```bash
//Salir del terminal opción 1
exit
//Salir del terminal opción 2
Ctrl + D
```
Al salir del terminal se cierra el contenedor

