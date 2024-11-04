
# Actividad 3
# Levantar un clúster de Hadoop + YARN + Hive. Visualizar en PowerBi


Clonar repositorio donde esta el docker compose que tiene los contenedores con las imagenes de hadoop, de yarn y de hive
```bash
git clone https://github.com/MarioSantanaTajamar/Hadoop-PowerBi
```
Levantar contenedores
```bash
docker-compose up -d
```
Ejecutar hive
```bash
docker-compose exec hive-server bash
```
Usar hive para usar bases de datos con hadoop
```bash
hive
```
Crear tabla
```bash
CREATE TABLE pokes (foo INT, bar STRING);
```
Insertar datos
```bash
LOAD DATA LOCAL INPATH '/opt/hive/examples/files/kv1.txt' OVERWRITE INTO TABLE pokes;
```
Instalar PowerBi en local (mantener el cluster de hive arrancado con los datos)
```bash
Una vez dentro de PowerBi, en la primera pestaña darle a Obetenr datos de otros orígenes
```
```bash
En la siguiente pestaña buscar Hive LLAP
```
Configurar PowerBI con hive
```bash
En la configuración de Hive LLAP:
Servidor: localhost:10000
Base de datos: default
Protocolo: Standart
Modo de conectividad: Importar
```
Cargar datos
```bash
Elegir la tabla pokes (o la que hayamos creado) y cargarla
```
Visualización
```bash
En datos seleccionamos los dos datos de pokes y en visualización elegimos un gráfico que queramos 
```



