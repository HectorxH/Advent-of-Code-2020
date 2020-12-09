# Dia 9: Encoding Error

# Parte 1

Dado que el input era relativamente pequeño decidi simplemente utilizar fuerza bruta. Puede utilizar sets o dicts para buscar la diferencia y asi ahorrarme un loop.

# Parte 2

Aqui ya decidi utilizar el set para buscar la diferencia. La estrategia aqui fue crear una tabla de sumas acomuladas, asi para encontrar un intervalo que sume N, tan solo debo buscar 2 elementos que al restarlos me den N. 