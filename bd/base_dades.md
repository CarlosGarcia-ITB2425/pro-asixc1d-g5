# Base de dades

Aquest apartat descriu el disseny i implementació de la base de dades

En esta parte del proyecto hemos diseñado y creado una base de datos orientada a la gestión de clientes, cumpliendo con los requisitos establecidos.

### Modelo Entidad-Relación

Como punto de partida, elaboramos el **modelo Entidad-Relación** a partir de las entidades:

- Empleados  
- Niveles de Grupo  
- Departamentos  

En cada entidad hemos definido su *clave primaria*, los *atributos* necesarios y las *relaciones* correspondientes entre ellas.

![Entidad-Relación](Entidad-Relación.png)

### Transformación a modelo relacional

A continuación, realizamos la **transformación del modelo Entidad-Relación al modelo relacional**, como paso previo a su implementación en un sistema gestor de bases de datos. Esta transformación permitió definir las tablas, claves primarias y foráneas, así como los tipos de datos apropiados.

Con la estructura definida y los datos necesarios disponibles (por ejemplo, los convenios correspondientes), procedimos a la **implementación en el gestor de bases de datos MySQL**.


### Implementación de los datos en MySQL 

Para hacer la implementación de los datos se instaló MySQL Server en una máquina Ubuntu 24.04 utilizando _sudo apt install mysql-server_ y se accedió al cliente de MySQL con _sudo mysql_.

Seguidamente, hemos creado la base de datos con el nombre de _ProjG5_ usando el comando _CREATE DATABASE ProjG5;_ y la hemos seleccionado para trabajar con ella con _USE ProjG5;_.

Una vez dentro de esta base de datos se creó las tres tablas necesarias: _Departament_, _GrupNivell_ y _Empleat_. Cada tabla se diseñó con sus respectivas claves primarias y relaciones necesarias mediante claves foráneas.


![CreaciónDeTablas](CreaTables.png)


Posteriormente, se insertaron los datos en cada tabla utilizando sentencias _INSERT INTO_, asegurando que los valores correspondieran con las relaciones establecidas entre las entidades.


![InserciónDeDatos](InsertTables.png)


Después, hemos verificado la creación de las tablas y la inserción de los datos utilizando los comandos _SHOW TABLES;_ para ver las tablas creadas y _SELECT * FROM nombre_tabla;_ para visualizar los datos insertados en cada una de las tablas que hemos creado.


![VisualizaciónDeTablas](SelectTables.png)


Para finalizar, hemos creado 3 diferentes usuarios para la base de datos y les hemos asignado distintos roles con permisos diferentes.

![CreaUSer1](CreateUsers1.png)

![CreaUser2](CreateUsers2.png)

- El usuario *Prueba* simplemente podia visualizar las tablas con el comando _SELECT * FROM nombre_tabla;_
- Otro usuario era el *Admin*, este usuario tenia acceso total a las tablas de la base de datos, sin ninguna limitación o restricción.
- Por ultimo teniamos al usuario *Supervisior*, este usuario solamente tenia acceso a visualizar las tablas y a actualizarlas.

Cada uno de estos usuarios tenia acceso a la base de datos con su propia contraseña.

![CreaRol1](CreateRoles1.png)

![CreaRol2](CreateRoles2.png)

### Pruebas de usos de Usuarios / Permisos

Por último, hicimos diferentes comprobaciones de sentencias (*Insert, Select, Update...*) para poner a prueba las restricciones de los roles de cada usuario creado.

En esta imagen vemos que el usuario *Prueba* puede consultar las tablas pero no tienen permiso para insertar nuevos datos.

![PruebaUsu](UsuPrueba.png)

El usuario *Admin* podemos ver que no tiene ningún tipo de restricción y puede visualizar e insertar datos en las tablas sin problema.

![AdminUsu](UsuAdmin.png)

Y por otra parte el usuario *Supervisor* puede ver las tablas y actualizarlas, pero no es capaz de insertar nuevos datos en ellas.

![SuperUsu](UsuSuper.png)
