# Dia 5: Binary Boarding

# Parte 1

En este problema decidi ir con la opcion que me requeria escribir menos. Para esto decidi remplazar todos los `'F'` o `'L'` con `'0'` y los `'B'` o `'R'` con `'1'`. Posterior a esto tomo los primeros caracteres (los que indicaban `'F'` o `'L'` y los converti de binario a entero) para obtener la fila. Analogamente para las columnas.

Finalmente obtener el maximo con `maximo = max(maxi, id_actual)`

# Parte 2

Ya que estabamos pensando en binarios, decidi utilizar un metodo un poco mas fancy, el metodo obvio seria guardar todo en un arreglo, ordenarlo y buscar el que falta en O(NlgN). 

Mi estrategia aqui fue aprovecharme de las propiedades del `xor` para deducir en O(N) el valor del id faltante.

La funcion `xorToN` calcula el resultado de hacer `xor` entre todos los numeros de `0` a `N`. El porque exactamente funciona, para mi aun sigue siendo magia negra de `xor`, solo se que funciona.

La funcion `xorRange` calcula el resultado de hacer `xor` entre todos los numeros de `a` a `b`. Esto lo realizo calculando de `0` a `b` y cancelandolo con los de `0` a `a`.

Ahora si hacemos `xor` de todos los id que tenemos con el `xorRange` desde el minimo id hasta el maximo, se cancelaran todos los numeros ya utilizados, dejandonos asi, solo nuestro id.