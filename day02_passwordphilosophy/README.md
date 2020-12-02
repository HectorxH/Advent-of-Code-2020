# Dia 2: Password Philosophy

## Parte 1

No mucho que explicar, la mayor parte del codigo es leer la entrada y el resto es comprobar que la cantidad de veces que se repite la letra este en el rango.

## Parte 2

Aqui hay 2 detalles, el primero es que creo una funcion `xor`, que simplemente es como utilizar `^`, pero en mi mente al menos es mas claro de leer, ya que `^` es un operador de bits, no booleano. Lo segundo es que utilizo `try`-`except` para asegurarme que las posiciones esten dentro del string.