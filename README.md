# Base-de-datos
Proyecto del grupo 371 

Primero descargue e instale Docker Desktop y DBeaver 26.0.0.
En Docker cree un servidor de PostgreSQL usando el puerto `5432` y estas variables:

POSTGRES_USER=postgres
POSTGRES_PASSWORD=contrasena
POSTGRES_DB=mi_base

<img width="1550" height="407" alt="dockerfoto" src="https://github.com/user-attachments/assets/76a7ab8f-92a2-44a1-bd72-c0d6343468c2" />

Despues de iniciar el servidor de PostgreSQL, abri DBeaver y cree una conexion nueva.

Use el puerto 5432 y los datos del usuario que configure en Docker para poder entrar a la base de datos.
Una vez conectado pude ver la base de datos mi_base y empezar a hacer pruebas con comandos de PostgreSQL.

<img width="571" height="82" alt="posgresserver" src="https://github.com/user-attachments/assets/d96ac109-8577-4eb0-9e5c-2675609e3f1e" />



### Crear un usuario

```sql
CREATE USER hola WITH PASSWORD 'contrasena';
```

### Dar todos los permisos sobre una base de datos

```sql
GRANT ALL PRIVILEGES ON DATABASE mi_base TO hola;
```

### Dar permisos para crear tablas

```sql
GRANT ALL ON SCHEMA public TO hola;
```

### Quitar permisos

```sql
REVOKE ALL PRIVILEGES ON DATABASE mi_base FROM hola;
```

### Eliminar un usuario

```sql
DROP ROLE hola;
```

### Dar permisos de administrador

```sql
ALTER ROLE hola WITH SUPERUSER;
```

### Quitar permisos de administrador

```sql
ALTER ROLE hola WITH NOSUPERUSER;
```

<img width="1335" height="495" alt="comandos" src="https://github.com/user-attachments/assets/268c50cc-26ca-47cd-87cf-4d81623ba343" />


## Lo que sigue

El siguiente paso es hacer pruebas para guardar informacion y conectarla con otro servidor. Todavia no se ha realizado esta parte.

