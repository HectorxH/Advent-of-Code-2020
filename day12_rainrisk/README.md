# Dia 12 Rain Risk

# Parte 1

Mantengo la posicion actual y una direccion, cada vez que se ejecuta un `'L'` o un `'R'` utilizo una `dict` para buscar donde estaria la nueva direccion al rotarla en 90. Esta solucion esta bastante hardcodeada, pero como son solo angulos multiplos de 90 funciona bien para este problema.

# Parte 2

La solucion no funcionaba tan bien para este problema, por lo que borre todos los diccionarios y recorde que una forma facil de representar coordenadas y poder rotarlas es utilizando numeros complejos. Por lo demas la solucion se mantiene muy similar.