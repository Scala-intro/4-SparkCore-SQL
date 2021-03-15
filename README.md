# 4 Spark Core y SQL

![scala](./images/001.png)

![scala](./images/002.png)
![scala](./images/003.png)
![scala](./images/004.png)


## Tipo de datos con los que trabajamos, RDD
![scala](./images/005.png)
![scala](./images/006.png)

Son distribuidas porque los datos estan distribuidos por los clusters

![scala](./images/007.png)

Son inmutables porque cada vez que hacemos una operación sobre el RDD creamos un nuevo RDD. Nunca manipulamos el origen de los datos.

![scala](./images/008.png)

Resiliente porque estan alojados los mismos datos en varios nodos por lo cual si se cae uno estan los demás con los mismos datos.

![scala](./images/009.png)

## Operaciones a un RDD
### Transformaciones

![scala](./images/010.png)
![scala](./images/011.png)

Filter
![scala](./images/012.png)
Map
![scala](./images/013.png)

Operaciones de conjuntos
![scala](./images/014.png)
![scala](./images/015.png)

### Acciones
![scala](./images/016.png)
collect: Recogeme todos los datos que tengo en el RDD

count: Cuentamelos todos.

countByValue: Cuentame cuantas valores tengo.

take: Da un conjuto limitado de datos, take(10)

saveAsTextFile: guardar el RDD filtrado o mapeado guardarlo como un archivo de texto

reduce: 
![scala](./images/017.png)

### Caching 

Los datos se almacenan en caché automáticamente cada vez que se debe capturar un archivo desde una ubicación remota. Las lecturas sucesivas de los mismos datos se ejecutan de forma local, lo que resulta en una velocidad de lectura significativamente mejor.
![scala](./images/018.png)

Donde guardamos la información siempre que se pueda hay que guardarlo en memoria, aunque podemos alternar entre memoria y disco. El disco como útlima opción.

También se pueden guardar los datos de forma serializada, ya que ocupan menos espacio.


![scala](./images/019.png)

### Pair RDD
Es un RDD que contiene elementos clave-valor, se pueden hacer las mismas transformacione que con RDD normal.

Nos interasa este tipo de datos por que Scala tiene varias transformaciones que trabajan con clave-valor.

También se pueden hacer acciones de conjuntos.

![scala](./images/020.png)
