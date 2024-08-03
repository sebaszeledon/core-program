## Highlights Week 2.4 - Groth16, STARKs & FRI

### Groth16

Un algoritmo que permite que un probador calcule un programa aritmético cuadrático sobre puntos de curva elíptica derivados en una configuración confiable y que un verificador lo verifique rápidamente. Utiliza puntos de curva elíptica auxiliares de la configuración confiable para evitar pruebas falsificadas.

#### Ventajas:

- Pruebas compactas: Groth16 produce pruebas extremadamente pequeñas, generalmente de solo unos pocos cientos de bytes, independientemente de la complejidad del circuito.
- Verificación rápida: La verificación de una prueba en Groth16 es extremadamente rápida, generalmente requiriendo un tiempo constante (constante en la cantidad de multiplicaciones de par) independientemente del tamaño del circuito.
- Eficiencia en generación de pruebas: Aunque la fase de configuración inicial (trusted setup) puede ser compleja, una vez completada, la generación de pruebas es relativamente eficiente en términos de tiempo y recursos computacionales.

### STARKs: Scalable Transparent Argument of Knowledge

#### Ventajas:

- Escalabilidad: son altamente escalables y pueden manejar grandes cantidades de datos y operaciones complejas. Los hace adecuados para aplicaciones que requieren manejar grandes volúmenes de información o realizar cálculos complejos, como la verificación de transacciones en blockchains.
- Transparencia: No requieren una configuración inicial de confianza, lo que elimina la necesidad de una ceremonia de configuración segura. Aumenta la seguridad y la confianza en el sistema, ya que no hay necesidad de confiar en una entidad centralizada para la configuración inicial.
- Tamaño de pruebas: Las pruebas STARK son más grandes en comparación con SNARKs, pero son más rápidas de generar y verificar. La eficiencia en la generación y verificación de pruebas es crucial para aplicaciones en tiempo real y para mantener la usabilidad y adopción en sistemas prácticos.

### FRI: Fast Reed-Solomon Interactive Oracle

#### Ventajas: 

- Eficiencia: FRI Permite verificar la proximidad de un polinomio a un código Reed-Solomon de manera eficiente. Esto reduce el costo computacional y el tamaño de las pruebas en los STARKs, haciendo que las pruebas sean más prácticas para aplicaciones reales.
- Robustez y seguridad: FRI es robusto frente a ataques criptográficos y ofrece fuertes garantías de seguridad. Asegura que las pruebas sean confiables y resistentes a manipulaciones.
- Aplicaciones en STARKs: FRI se utiliza como parte de la construcción de STARKs para mejorar la eficiencia y reducir el tamaño de las pruebas. La combinación de FRI con STARKs permite crear pruebas que son prácticas tanto en términos de tamaño como de eficiencia de verificación.

