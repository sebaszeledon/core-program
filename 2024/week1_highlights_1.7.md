## Highlights Week 1.7 - Crytographic Commitments

### ¿Cuál es el objetivo principal de los Commitments?

Permiten ocultar y revelar información selectivamente. Esta característica garantiza la privacidad de los datos y al mismo tiempo permite los procesos de verificación.

### ¿Qué tipo de información oculta y revela un Compromiso Polinómico?

### Información oculta: 

1. El Polinomio Completo:
    * Definición: El polinomio P(x) en sí mismo permanece oculto para cualquier parte que solo tiene acceso al compromiso.
    * Importancia: Ocultar el polinomio completo asegura la privacidad de los datos subyacentes y evita que cualquier información sensible contenida en el polinomio sea revelada.

2. Coeficientes del Polinomio:
    * Definición: Los coeficientes del polinomio P(x) = a0 + a1 x + a2 x2 + ... están ocultos.
    * Importancia: Mantener los coeficientes en secreto previene que se pueda reconstruir el polinomio completo, preservando la confidencialidad de la información específica representada por esos coeficientes.

### Información revelada:

1. Evaluaciones del Polinomio en Puntos Específicos:
    * Definición: Se puede revelar P(x) para ciertos valores de x sin revelar el polinomio completo.
    * Importancia: Permite verificar la exactitud del polinomio comprometido en ciertos puntos específicos, lo cual es útil para aplicaciones donde solo es necesaria la validación en ciertos puntos.

2. Pruebas de Propiedades del polinomio:
    * Definición: Permite probar ciertas propiedades del polinomio, como si P(x) es de grado d o satisface alguna ecuación particular en puntos específicos.
    * Importancia: Estas pruebas pueden ser esenciales para protocolos criptográficos donde se necesita verificar la estructura o las características del polinomio sin revelarlo completamente.

### ¿Cómo contribuyen los Compromisos de Pedersen a la privacidad en la criptografía?

### Por medio de sus características de Hiding y Binding:

1. Ocultamiento (Hiding):
    * Definición: Un compromiso de Pedersen oculta completamente el valor comprometido. Nadie puede deducir el valor original del compromiso sin conocer el valor y el parámetro de aleatorización (blinding factor).
    * Importancia: Esta propiedad asegura que el valor comprometido permanezca privado, incluso si el compromiso se hace público.

2. Inmutabilidad (Binding):
    * Definición: Una vez que una parte se ha comprometido a un valor, no puede cambiarlo. El compromiso está vinculado de manera única al valor original y al parámetro de aleatorización.
    * Importancia: Esta propiedad garantiza la integridad de los datos comprometidos, evitando que una parte cambie su valor después de comprometerse.

### ¿Por qué son importantes los compromisos criptográficos en la tecnología blockchain?

* Privacidad y Confidencialidad: Ocultamiento de datos sensibles mientras se puede interactuar con los mismos.
* Integridad y consistencia de los datos: Los compromisos criptográficos permiten a las partes verificar la integridad de los datos comprometidos sin necesidad de revelar los datos mismos. 
* ZKPs: Permiten a una parte demostrar que conoce un valor sin revelar el valor del mismo.
* Eficiencia y escalabilidad: Ayudan a reducir la cantidad de datos que deben ser procesados y almacenados mejorando la eficiencia y escalabilidad.
* Seguridad: Brindad resistencia a las manipulaciones ya que los compromisos aseguran que los datos comprometidos no puedan ser alterados sin invalidar el compromiso.
