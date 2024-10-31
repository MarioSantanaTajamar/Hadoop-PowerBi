
Clonar repositorio donde esta el docker compose que tiene los contenedores con las imagenes de hadoop, de yarn y de hive
```bash
git clone https://github.com/PabloHerreraTajamar/Hadoop-hive
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
CREATE TABLE Empleados (
    nombre VARCHAR(50),
    apellidos VARCHAR(50)
);
```
Insertar datos
```bash
INSERT INTO Empleados (nombre, apellidos) VALUES ('Juan', 'Pérez');
INSERT INTO Empleados (nombre, apellidos) VALUES ('María', 'García');
INSERT INTO Empleados (nombre, apellidos) VALUES ('Carlos', 'López');
```
Consultas basicas
```bash
SELECT * FROM Empleados WHERE apellidos = 'Pérez';
```


