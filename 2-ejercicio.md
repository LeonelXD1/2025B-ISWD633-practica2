### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
# COMPLETAR
docker run -d --name postgres -e POSTGRES_PASSWORD=leoxd1 postgres:15-alpine3.21
### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
docker run --name client_pos -e PGADMIN_DEFAULT_EMAIL=alessandro231r@gmail.com -e PGADMIN_DEFAULT_PASSWORD=leoxd1 -p 80:80 dpage/pgadmin4
# COMPLETAR

La figura presenta el esquema creado en donde los puertos son:
- a: 80
- b: 80
- c: 5432

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN
<img width="1131" height="509" alt="image" src="https://github.com/user-attachments/assets/c7f24a3a-6011-4bf2-a94a-a450d98ae2be" />

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
insert into public.personas(nombre)values('jonathan Pagual'),
('Leonel'),
('Naty'),
('Zoe');
```
## Desde el servidor postgresl
### Acceder al servidor
docker exec -it postgres bash
### Conectarse a la base de datos info
# COMPLETAR
### Realizar un select *from personas
psql -h localhost -U postgres -d info
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO}
<img width="675" height="324" alt="image" src="https://github.com/user-attachments/assets/78f5ec87-bdb4-4cd7-8e25-a774177d58c4" />

