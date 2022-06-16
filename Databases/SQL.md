# SQL: Structure Query Language

SQL es un lenguaje de acceso a bases de datos que explota la flexibilidad y potencia de los sistemas relacionales y permite así gran variedad de operaciones.

## COMANDOS:

![Commands](./images/Comandos%20SQL-72cd96bf-3335-40a8-adaa-f5b444efcc4d.webp)

## DDL: Data definition Language

Es un lenguaje que nos ayuda a crear la estructura de una database

### Tres comandos importantes:

- Create
- Alter
- Drop

#### Create

Puedes crear:

- Bases de datos | Database
- Tablas (entidad) | Table
- Vistas |View

| Command                           | Description                   |
| --------------------------------- | ----------------------------- |
| CREATE DATABASE (nombre de la db) | Crea una base de datos        |
| USE DATABASE (nombre de la db     | Decide que base de datos usar |

#### Alter

Puedes alterar:

- Bases de Datos
- Tablas
- Vistas

#### Drop

(Sentencia peligrosa)
Puedes borrar:

- Bases de Datos
- Tablas
- Vistas

## DML: Data Manipulation Language

Trata del contenido de la base de datos.

### 4 comandos importantes

- Insert
- Update
- Delete
- Select

#### Insert

`INSERT INTO name_of_table (last_name, first_name) VALUES('Hernandez', 'Laura');`

#### Update

`UPDATE people`
`SET last_name = 'Chávez', city= 'Mérida'`
`WHERE person_id = 1;`

`UPDATE people`
`SET last_name = 'Juan'`
`WHERE city= 'Mérida'`

#### Delete

`DELETE FROM people`
`WHERE person_id = 1;`

#### Select

`SELECT first_name, last_name`
`FROM people;`

## FOREIGN KEYS

Las Foreing Key options son las siguientes:

1. On update: Significa qué pasará con las relaciones cuando una de estas sea modificada en sus campos relacionados, Por ejemplo, pueden utilizarse los valores:
   cascade: Si el id de un usuario pasa de 11 a 12, entonces la relacion se actualizará y el post buscará el id nuevo en lugar de quedarse sin usuario.
   \_ restrict: \_Si el id de un usuario pasa de 11 a 12, no lo permitirá hasta que no sean actualizados antes todos los post relacionados.
   set null Si el id de un usuario pasa de 11 a 12, entonces los post solo no estará relacionados con nada.
   no action: Si el id de un usuario pasa de 11 a 12, no se hará nada. Solo se romperá la relación.
2. On delete
   _ cascade: Si un usuario es eliminado entonces se borrarán todos los post relacionados.
   restrict: No se podrá eliminar un usuario hasta que sean eliminados todos su post relacionados.
   _ set null: Si un usuario es eliminado, entonces los post solo no estará relacionados con nada.
   no action: Si un usuario es eliminado, no se hará nada. Solo se romperá la relación.
