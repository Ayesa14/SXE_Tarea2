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