BFS - Breadth First Search

-------------------------------
-----PSEUDOCODIGO----------

    crear conjunto visitados
    crear cola

    agregar inicio a la cola
    agregar inicio a visitados

    imprimir "Orden de exploración empezando desde inicio"

    mientras la cola no esté vacía hacer

        nodo_actual ← sacar el primer elemento de la cola
        imprimir nodo_actual

        para cada vecino en grafo[nodo_actual] hacer

            si vecino no está en visitados entonces
                agregar vecino a visitados
                agregar vecino al final de la cola

            fin si

        fin para

    fin mientras

Fin algoritmo

----------------------------

------Descripción del codigo BFS---------

Este programa implementa el algoritmo BFS (Breadth First Search) o búsqueda en anchura para recorrer un grafo.
BFS es un algoritmo que explora los nodos nivel por nivel, visitando primero todos los vecinos cercanos antes de continuar con los más lejanos.

En Inteligencia Artificial, BFS es importante porque se usa para buscar soluciones en espacios de estados, por ejemplo:

Encontrar la ruta más corta en un mapa sin pesos.

Explorar grafos o redes.

El algoritmo es completo (encuentra solución si existe) y óptimo cuando todas las aristas tienen el mismo costo.

Funcionamiento del código

El programa utiliza:
set() para registrar los nodos visitados.
deque (cola) para mantener el orden de exploración FIFO (First In, First Out).
Esto permite que los nodos se exploren por niveles, característica principal de BFS.

Explicación del algoritmo
Se define el nodo inicial desde el cual comenzará la búsqueda.
Se crea una cola donde se almacenan los nodos por explorar.
Se marca el nodo inicial como visitado.

Mientras la cola tenga nodos:
Se extrae el primer nodo de la cola.
Se imprime (o procesa).
Se revisan sus vecinos.
Si un vecino no ha sido visitado:
Se marca como visitado.
Se agrega a la cola.