# Dia 7: Handy Haversacks

# Parte 1:

No voy a comentar mucho respecto a la lectura del input ya que ya hice mucho de esto en los dias anteriores del advent. Lo unico destacable es que utilize `rsplit` que es como `split` pero cuando limitas la cantidad de splits selecciona desde derecha a izquierda.

Ahora entrando a la resolucion del problema: Modele el problema como un grafo en donde A->B si y solo si la bolsa de color A esta contenida en la bolsa de color B. Esta forma de ordenar el grafo hace que sea mucho mas facil buscar desde una bolsa interior ("shiny golden") a todas las bolsas exteriores. Una vez modelado como un grafo realizo una busqueda en anchura (BFS), aunque esto es solo preferencia y una busqueda en profundidad (DFS) habria sido una opcion valida. Ahora escribiendo esto me doy cuenta que mantener una variable `total` es _totalmente_ inutil ya que pude utilizar `len(visitados)` para lograr el mismo resultado y de forma mas _pythonica_.

# Parte 2:

Aqui bastaba con realizar cambios menores a la implementacion de la parte 1. Primero que nada inverti el orden del grafo, de A->B si A esta contenido en B paso a ser A->B si A *contiene* a B. Esto es por la misma razon que antes ya que ahora queremos buscar de la bolsa mas exterior hacia adentro.

Tambien ahora en vez de guardar en la lista de vecinos solo el identificador (color) tambien ahora guardamos la cantidad de veces que se encuentra esa bolsa.

En la implementacion de BFS ahora la modificacion es que ya no me interesa revisar si esta visitado o no, ya que ahora _si quiero considerar los repetidos_. Cada vez que añadimos una bolsa a la cola de busqueda incluimos su cantidad multiplicada por la cantidad de veces que aparece su bolsa padre, esto nos guardara la cantidad de veces que aparece la bolsa en total. Esta forma de almacenar una cantidad acomulada es muy similar a lo que se hace en Dijkstra, es solo que aqui no ordenamos la cola por esta cantidad. Finalmente cada vez que pasamos por un elemento de la cola añadimos a un total la cantidad de veces que aparece la bolsa.