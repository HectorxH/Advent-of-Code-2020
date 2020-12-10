# Dia 10: Adapter Array

# Parte 1

Leo los numeros y añado un 0 (joltaje base). Ordeno los numeros y calculo las diferencias entre numeros adjacentes y agrego un 3 (dif entre maximo y dispositivo). Finalmente cuento los 1 y 3. Una solcion muy directa.

# Parte 2

Decidi utilizar DP y recursion para contar. Sumo las formas que hay de contar los posibles prefijos del problema. Tambien pudo ser posible ahorrar memoria con un aproach bottom up O(1), pero considerando que ya se utiliza espacio O(N) para almacenar los numeros ordenados lo considere inecesario.