# CLASE-IWEB-8

## Para trabajar en una sola Base de Datos: (colocarlo en negrito)
Primero seleccionamos la Base de Datos y clic derecho

<img width="288" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/8ffdd7f8-e9ee-4142-8165-3bec3fe52695">

Segundo, clic en Set as Default Schema y aparecerá en negrito la db:

<img width="156" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/24de335a-7574-4d94-ba1e-4c6228cfc4d1">

## Instrucción SELECT
Empleamos el comando SELECT para seleccionar cierta porción de una tabla en la db

![image](https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/f5347917-b17d-4371-8cfb-e0f0eafa9e3d)

comando (cuando trabajamos sobre una base de datos como default schema):

    select first_name, last_name FROM <nombre_tabla>;

comando si no hemos colocado a la base de datos como default schema:

    select first_name, last_name FROM <db_name>.<nombre_tabla>;

## Instrucción SELECT - DISTINCT
Sirve para que al seleccionar una porción de la tabla, seleccione solo 1 de los muchos que existen

Empleamos SELECT y notamos que el job_id se duplica o triplica:

<img width="583" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/159fd172-0e8d-4e3c-82d8-b2c2053e416c">

Empleando SELECT - DISTINCT podemos filtrar y solo que aparezca un valor de job_id

<img width="518" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/4bbedd37-e7d8-4473-b9a8-f1365a128487">

## Instrucción SELECT - ORDER BY
Usamos el ORDER BY para poder ordenar nuestra info extraída como queramos

El orden ASCENDENTE para números es del menor ---> mayor

El orden ASCENDENTE para letras es de A ---> Z

El orden DESCENDENTE es lo contrario.

Ordenamos en orden ascendente los salarios:

<img width="583" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/2dc8c167-3fba-4ddf-8bb4-a6d9f78b76b9">

Ordenamos en orden descendente los salarios:

<img width="581" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/cb5b4915-a95b-4986-acb1-dd423d97c012">

CASO ESPECIAL DE ORDER BY:
en caso tengamos los mismos salarios en algunas personas, podemos ordenarlas también de otra forma:

Vemos que los que tienen mismo salario ahora están ordenados por first_name:

<img width="580" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/98d97a61-67f0-40a3-be0c-88140bea1f35">

## Instrucción SELECT WHERE
Empleamos SELECT WHERE para poder filtrar mediante condiciones

<img width="581" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/79d2b87d-2c18-41da-955f-4db868c34e98">

Filtrado por first_name (String):

Observamos que hay 2 Karen en la tabla

<img width="543" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/301140c1-3d74-4b4c-b86f-aa5cfa191b83">

-Sin embargo, ahora queremos tener a la Karen que tiene comisión (es decir comisión no nula)

<img width="586" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/cd97a4b4-798f-4c2e-a092-fabd138ce319">

-Ahora queremos a la Karen que no tiene comisión:

<img width="582" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/5a355375-4021-499a-8cf6-df0eee49f344">

NOTA: Primero empleemos los filtros necesarios (WHERE) para luego poder ordenarlos (ORDER BY):

<img width="537" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/83833871-9538-43d1-94ba-e4845ce2a6a6">

## CONCEPTO RECURSIVIDAD
Se usa cuando hay jerearquía en una misma tabla, por ejemplo en una tabla de Empleados tienen sus respectivos Jefes pero los propios Jefes son Empleados o pueden tener otros Jefes.

<img width="397" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/8f28caba-69cb-4997-98bc-4fad9d1d89dc">

## WHERE - BETWEEN

<img width="546" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/0f1050df-634c-4419-9888-d520742f81b4">

## WHERE - IN - NOT IN
Para en vez de colocar este comando:

<img width="493" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/356eceec-87aa-4c9f-94e3-3d2700a0b831">

Coloquemos con IN:

<img width="516" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/7e5910bd-029d-407f-98e0-07d5b627313f">

Coloquemos NOT IN:

<img width="528" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/5ac0f480-65de-4fd0-be13-86cce6db1698">

## LIKE
LIKE se utiliza para hacer búsquedas parciales

1) Buscamos todos los nombres tengas S% (El porcentaje indica 0 o más), es decir si piden que solo tenga 6 caracteres y letra del inicio S, no podríamos encontrarlo.

    <img width="541" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/f4cd2140-dab6-4f0f-a99f-c3d8af0e50f4">

2) Para buscar nombres con una cantidad de caracteres específicos se usa "_" por cada caracter posterior al S:

    <img width="536" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/686075c2-5684-4e43-a037-38c0763acfeb">

3) Para ubicar nombres que CONTENGAN la letra s

Primero pasamos todos los first names a minúsculas con lower

Luego usamos like "%s%" usando doble wildcard tanto izquierda para derecha

   <img width="536" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/de602883-f184-401b-9880-e6b4b76125ea">

4) Para buscar nombres con 3 caracteres exactos:

   <img width="538" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/cd795bcd-987a-4cf3-ae4a-29102d6194d0">

CUANDO TENEMOS UN PORCENTAJE EN EL NOMBRE:

Se buscan todos los nombres que tengan 0 o muchos a la izquierda y acaben en %

El escape "=" es un indicador para que lo de la derecha sea tomado en el sentido literal y no en la función.

En este caso, en el lado derecho de = podremos ver que quiere que acabe en % porque está en la ultima posicion dicho caracter.

<img width="531" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/8abe1ced-3da6-4e42-bd9a-4a18ca61451e">

Otro ejemplo:

<img width="404" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/c3eac3cb-9a2a-46ea-b8b2-0277f0622c54">

## GROUP BY
Cuando agrupo son solo relevantes la columna de agrupamiento y columnas con función de agrupamiento

Cuando se agrupa, no es necesario el asterisco ya que no representa nada, lo que sí son las 2 cosas de arriba

<img width="593" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/fe61ba6a-5acb-44c6-aa36-84bccc5394e2">

El Count(*) sirve para contar la cantidad de filas que contiene ese agrupamiento y el avg es el promedio: avg()

Diferencias entre count(*) y count(Department_id)

count(*) cuenta nulos

count(Department_id) no cuenta nulos

sum(salary) ---> suma todos los salarios por cada departament_id

<img width="601" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/f3718b2c-28d8-4648-bc8e-fd8034cea275">

Si queremos ordenar los máximos salarios de mayor a menor, lo hariamos con ORDER BY y agregado con "as" un alias para luego emplearlo:

## Instrucción HAVING
Sirve SOLAMENTE para filtrar resultados de agrupamiento

como no se puede hacer así:

<img width="471" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/f7d32edd-9dd5-4772-8512-189810440b4f">

Lo haremos con HAVING:

Aplicamos filtro como si fuera WHERE

<img width="460" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/7dc6c2bf-9760-42b5-88ad-a3e1bdf60285">


## PRACTICAS
NOTA: El asterisco significa TODA LA TABLA y con coma podemos agregar más columnas para una mejor visión, esto no tiene repercusiones en la Base de Datos.

1) Para agregar una columna en el SELECT (NO EN BASE DE DATOS):
   
   <img width="583" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-8/assets/134556600/b75d6065-a77c-40e8-9813-11e30c081228">

