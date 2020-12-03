# Dia 3: Toboggan Trajectory

# Parte 1

A medida que leo el archivo voy revisando si la posicion actual es un arbol, luego avanzo hacia la derecha en base a la pendiente, utilizo `%` para simular el efecto de que el mapa se repite infinitamente.

# Parte 2

Aqui se podia implementar de la misma que el anterior pero con varios "punteros" a distintas posiciones actuales y varios contadores, pero creo que es mas legible y mas simple hacerlo un poco mas fancy y cree una funcion que calcula las colisiones dada una pendiente.

Primero converti el input en una matriz booleana que almacena si hay o no un arbol en una posicion dada. Luego la funcion `checkCollisions(r, d, G)` se encarga de contar con cuantos arboles se colisiona, de forma casi identica a la de la parte 1, la unica diferencia es que aqui ademas puede avanzar multiples linas (para la pendiente vertical `d`).

Finalmente multiplico todos los `checkCollisions(r, d, G)` solicitados.