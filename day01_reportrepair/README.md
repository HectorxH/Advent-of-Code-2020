# Dia 1: Report Repair

Para esta solucion estoy asumiendo que los numeros en el input no se repiten por simplicidad, sin asumir esto la solucion presentada en Parte 2 no aplica y debiese ser ligeramente distinta (Ordenar y busqueda binaria en vez de `set` o `dict` con la cantidad de repeticiones y unos checkeos adicionales).

## Parte 1

Utilizo `set` de python ya que considero que es la forma mas expresiva de resolver el problema. El input es almacenado en un archivo, cada vez que leo un numero en el archivo compruebo si su complemento en 2020 se encuentra en el conjunto (El conjunto solo incluye los numeros anteriormente leidos).

Como utilizo `set` la complejidad de comprobar si algo esta en el conjunto es O(1) en caso promedio, por lo que la complejidad total es O(n) en el caso promedio y O(n^2) en peor caso (Colisiones en el hash)

## Parte 2

Muy similar al anterior, la mayor diferencia es que por cada par de numeros leidos reviso si el complemento de su suma se encuentra en el conjunto.

Para este caso la complejidad promedio es O(n^2/2) y O(n^3) en peor caso.