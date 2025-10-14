### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
```
docker run -d --name postgres -e POSTGRES_PASSWORD=leoxd1 postgres:15-alpine3.21
```
### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
```
docker run --name -d client_pos -e PGADMIN_DEFAULT_EMAIL=alessandro231r@gmail.com -e PGADMIN_DEFAULT_PASSWORD=leoxd1 -p 80:80 dpage/pgadmin4
```
La figura presenta el esquema creado en donde los puertos son:
- a: 80
- b: 80
- c: 5432

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
<img width="3840" height="2041" alt="image" src="https://github.com/user-attachments/assets/95b48ab1-b43c-474b-a4cd-c320b6354083" />


### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.
``` Creación de la tabla
CREATE DATABASE "info";
--database: info
create table PERSONAS( 
ID SERIAL PRIMARY KEY NOT NULL,
NOMBRE VARCHAR(20) NOT NULL);
```
Inserción de los datos
```sql
insert into public.personas(nombre)values('Leonel'),
('Naty'),
('Zoe');
```
## Desde el servidor postgresl
### Acceder al servidor
```
docker exec -it postgres bash
```
### Conectarse a la base de datos info
### Realizar un select *from personas
```
psql -h localhost -U postgres -d info
```

<img width="337" height="184" alt="image" src="https://github.com/user-attachments/assets/f8acca20-0a11-4a76-9286-e6a874a45bc9" />

