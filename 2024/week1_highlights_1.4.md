## Highlights Week 1.4 - Merkle Trees

### 1. ¿Qué es un árbol Merkle, cuál es su estructura?

Es un árbol binario donde los nodos almacenan hashes en las hojas, los nodos padre son el resultado de concatenar estos hashes y aplicarles la función hash. Se aplica el mismo procedimiento en los nodos padre para obtener la raíz (Root Hash).

Se utilizan para verificar de manera eficiente la integridad de los datos de un conjunto.

### 2. ¿Cómo se usan los árboles Merkle en blockchain?

Forman parte de cada bloque de la mayoría de blockchains, aquí se encuentran los encabezados del bloque.

### 3. ¿Por qué son seguros y eficientes para verificar grandes estructuras de datos?

Porque cada vez que se inserta una nueva hoja en el árbol o se modifica, el root hash va a cambiar. Por lo que no es necesario ir a verificar todos los hashes, ya que el root hash es una “representación” de todas las hojas en el árbol. 
