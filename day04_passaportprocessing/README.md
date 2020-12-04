# Dia 4: Passaport Processing

# Parte 1

El problem completo consistia en ser capaz de leer el input. Lo primero que decidi, fue que la mejor idea seria leer el input completo de inmediato y separarlo en `\n\n`, de esta froma puedo tener una lista en donde cada elemento es un pasaporte.

Para el parsing de cada pasaporte individual lo divido por whitespace `\s` usando `re.split()`. Ahora tengo una lista en donde cada elemento es una string de la forma `"campo:valor"`. Finalmente un `map` para separar por `':'` y un poco de magia de `zip()` con el operador de listas `*` y puedo acceder a una tupla con todos los campos.

Ahora con la lista de campos tan solo checkeo que existan todos y que no hayan campos de mas. En esta parte asumo que los campos no se repiten, tan solo para ahorrarme muchas lineas extra.

# Parte 2

Para evitar el tener que escribir muchas cosas de nuevo, decidi simplemente crear una funcion que valide pasaportes y añadir el checkeo al mismo `if`. Nuevamente con la magia de `zip()` puedo formar un `dict` que represente el pasaporte. El proceso de validacion es una traduccion bastante literal de lo que pide el enunciado y no es muy interesante, lo unico rescatable es que utilizo un `try-except` para la validacion de algunos campos y nuevamente utilizo `re` para validar otros.