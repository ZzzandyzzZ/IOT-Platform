# IOT-Platform

----

## Ejecucion
1. Iniciamos el container:

```
    docker-compose up
```

2. Ingresamos a la terminal del mysql:

```
 docker exec -it iot-platform_mysql_1 bash
```

* Ingresamos a mysql:
```
 mysql -u root -p
 password: root
```

* Creamos la tabla thingData:
thingData
```
use tSeriesDB;

CREATE TABLE thingData (
    id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
    topic varchar(1024),
    payload varchar(2048),
    timestamp varchar(15),
    deleted binary(1)
);
```
* Podemos comprobar si se creo correctamente en [phpmyadmin](localhost:8080) (usuario:**user**, contraseña:**password**) . Ingresando a la estructura de la tabla thingData, veremos lo siguiete:

![Estructura de tabla](/images/Estructura_mysql.png)



