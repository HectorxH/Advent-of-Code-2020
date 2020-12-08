# Dia 8: Handheld Halting

# Parte 1

Una traduccion my directa del enunciado. Simulo las intstrucciones y si ya visite una linea entonces me detengo e imprimo `acc`

# Parte 2

Guarde la Parte 1 del problema en una funcion llamada `check` que me permita comprobar si se queda ene un loop infinito o no. Primero ejecuto check para generar un conjunto de candidatos a cambiar (las instrucciones visitadas antes de entrar en loop). Luego por fuerza bruta paso por todas las instrucciones candidatas y porbando si al cambiarlas se soluciona el loop.