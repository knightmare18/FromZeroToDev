#Bases de Datos Relacionales (RBD)

## Las 12 Reglas de CODD del modelo relacional
- [Link](https://bit.ly/3KWdQ0E)

## Nomenclatura 
- **Entidad**: Representa algo en el mundo real, un objeto. También conocida como Entidad Fuerte.
- **Atributos**: Son en sí, características de una entidad.
- **Atributo Multivaluado**: Es cuando la cantidad de ese atributo es mayor a 1.
- **Atributo Especial**: Es cuando no se calcula al igual que los anteriores.
- **Atributo Clave**: Es el dato que nos permite diferenciar a una entidad de otras.
    - **Naturales**: Cuando vienen con el objeto.
    - **Artificial**: Cuando nosotros le damos ese dato.
- **Entidades Débiles**: Son aquellas que no pueden existir sin una entidad fuerte. Pueden ser Débiles por dos motivos:
    - **Por Identidad**: Por que no se diferencian más que por la clave de su identidad fuerte
    - **Por existencia**: Cuando no depende del id de la entidad fuerte, sigue siendo una entidad débil por x motivos.
- **Relaciones**: Es cuando dos entidades tienen algo que los une.


![Nomenclature](https://static.platzi.com/media/user_upload/img-2e2fc1ba-ad77-4045-b7a5-f74a65e3f55e.jpg)

## Cardinalidad
![Cardinalidad](./images/unnamed.png)

## Diagrama ER
- [Página para hacer diagramas](https://app.diagrams.net)
## Diagrama Físico 
- Tipos de datos y Constraints (Restricciones)
![Tipos de Datos](./images/DiagramaF%C3%ADsico_tipo%20de%20datos%20y%20constraints-e18d3f34-6bb7-424b-8256-8212049045ce.jpg)
## Normalización
### Forma Normal
- **1FN Primera forma normal**: Atributos atómicos (Sin campos repetidos). Esto quiere decir que ningún campo puede tener el mismo tipo de valor como varios campos materia (materia1, materia2,…).
    - Todos los atributos son atómicos. Un atributo es atómico si los elementos del dominio son simples e indivisibles.
    - No debe existir variación en el número de columnas.
    - Los campos no clave deben identificarse por la clave (dependencia funcional).
    - Debe existir una independencia del orden tanto de las filas como de las columnas; es decir, si los datos cambian de orden no deben cambiar sus significados.

- **2FN Segunda forma normal**: Cumplir con 1FN y Cada campo de la tabla debe depender de una clave única. Es decir en las tablas no se puede repetir los campos primarios ya que los mismos son únicos por tanto si existe una relación uno a muchos se debe crear una tabla aparte donde cohabitaran la llave primaria de la primera tabla y la llave primaria de la segunda tabla de esta forma logramos relacionar de manera efectiva dos tablas respetando las llaves primarias.
    - Está en 1FN
    - Sí los atributos que no forman parte de ninguna clave dependen de forma completa de la clave principal. Es decir, que no existen dependencias parciales.
    - Todos los atributos que no son clave principal deben depender únicamente de la clave principal.

- **3FN Tercera forma normal**: Cumple 1FN y 2FN y los campos que NO son clave NO deben tener dependencias. Esto nos indica que todos los campos de la tabla deben estar estrechamente relacionados con el campo primario y no serlo de manera transitiva, por ejemplo, en una tabla torneos tenemos el código del torneo el nombre el ganador y la fecha de nacimiento del ganador, como observamos no podemos tener la fecha de nacimiento del ganador en dicha tabla ya que no está relacionada para nada con el torneo y además existe la posibilidad que en varios registros el mismo ganador tenga diferentes fechas de nacimiento por lo cual no mantendría la consistencia de los datos.
    - Se encuentra en 2FN
    - No existe ninguna dependencia funcional transitiva en los atributos que no son clave

- **4FN Cuarta forma normal**: Cumplir 1FN 2FN y 3FN. Los campos multivaluados se identifican por una clave única. Cuando relacionamos dos tablas totalmente independientes cada una de la otra debemos relacionarlas a través de una tabla aparte de las mismas donde solo colocaremos las llaves primarias de cada tabla. Esta FN trata de eliminar registros duplicados en una entidad, es decir que cada registro tenga un contenido único y de necesitar repetir la data en los resultados se realiza a través de claves foráneas. 
    - Se encuentra en 3FN
    - Los campos multivaluados se identifican por una clave única
 
## Ejercicio Platziblog
![Diagrama](./images/Diagrama%20ER%20de%20base%20de%20datos%20(pata%20de%20gallo).jpeg)