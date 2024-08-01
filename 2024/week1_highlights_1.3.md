## Highlights Week 1.3 - Hashing

### 1. ¿Qué es una función hash y cuáles son sus usos principales en criptografía?
Toma una entrada de datos y devuelve un string con una longitud fija. En criptografía su principal uso es la verificación de datos, al comparar los valores hash se verifica la integridad de los archivos o mensajes.

### 2. ¿Cómo funciona el algoritmo hash SHA-256, en términos simples?
Es una función hash que toma una entrada de datos y produce un string con una longitud de 256 bits.

### 3. ¿Qué es la función hash de Poseidon y por qué es particularmente útil en ZKPs?
Es una función hash diseñada para ser utilizada en ZKPs ya que eficiencia en hashing y complejidad de circuitos. 
Poseidon logra esa eficiencia a través de la reducción de operaciones y condiciones que se necesitan para verificar una prueba criptográfica dentro de un circuito. Esto quiere decir que al haber menos operaciones y la verificación es más rápida, entonces las pruebas y los costos de gas son más pequeños.
