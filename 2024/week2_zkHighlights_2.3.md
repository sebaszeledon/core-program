## Highlights Week 2.3 - STARKs & SNARKs

### Requisitos

El sistema de prueba requiere testigo, declaración inicial y un circuito.

zkSTARK y zkSNARK son en realidad adjetivos. Describen el tipo de sistema de prueba. No necesariamente tiene que ser zk.

- Zero-Knowledge: El verificador no puede saber qué se verifica excepto verdadero/falso.
- Succint: La prueba debe ser breve y poder verificarse rápidamente.
- Non-interactive: Prover y Verifier no necesitan interactuar de un lado a otro para verificar.
- ARgument: Es necesario coincidir con la naturaleza de la validez (Soundness), es casi imposible mentirle a un Verificador.
- (of) Knowledge: Se requiere conocimiento para producir pruebas.

### Proceso de generación de una prueba en un circuito zk-SNARK:

1. Representación del Problema como un Circuito
* Circuito Aritmético: El problema a resolver se representa como un circuito aritmético compuesto de puertas lógicas y aritméticas (suma, multiplicación).
* Constraints: El circuito define una serie de constraints que la solución debe satisfacer.

2. Trusted Setup (Configuración Confiable)
* Generación de Parámetros: Un Trusted Setup se realiza para generar parámetros públicos y secretos necesarios para la creación y verificación de pruebas.
* Destrucción de Secretos: Los parámetros secretos son destruidos después del setup para asegurar la integridad del sistema.

3. Compilación del Circuito
* R1CS (Rank-1 Constraint System): El circuito se convierte en un sistema de constraints en forma R1CS, que es una representación matemática de las operaciones del circuito.
* QAP (Quadratic Arithmetic Program): El R1CS se transforma en un QAP, que facilita la generación y verificación de pruebas.

4. Generación de la Prueba
* Asignación de Variables: El probador asigna valores a las variables de entrada y salida del circuito.
* Evaluación del Circuito: El circuito se evalúa utilizando estas asignaciones para asegurar que satisfacen todas las constraints.
* Construcción de la Prueba: Utilizando los parámetros públicos y las asignaciones, el probador genera una prueba criptográfica que contiene la información necesaria para verificar la correcta evaluación del circuito.

5. Verificación de la Prueba
* Verificación Eficiente: El verificador usa los parámetros públicos y la prueba generada por el probador para verificar que la prueba es válida sin necesidad de conocer las entradas originales del circuito.
* Prueba de Correctitud: La verificación asegura que el probador conoce una solución que satisface todas las constraints del circuito sin revelar dicha solución.

### Ejemplo Simplificado

1. Problema: Demostrar que conoces x tal que x^2 = y, sin revelar x.

2. Circuito:
    * Representación: y - x^2 = 0
    * Constraints: Una puerta que representa la operación x^2 y otra puerta que compara con y.

3. Trusted Setup:
    * Generación de parámetros públicos y secretos.
    * Destrucción de parámetros secretos.

4. Compilación:
    * Convertir y − x^2 = 0 en R1CS y luego en QAP.

5. Generación de la Prueba:
    * Probar que conoces x y que x^2 = y
    * Generar una prueba criptográfica con estas asignaciones.

6. Verificación:
    * El verificador usa la prueba y los parámetros públicos para verificar la validez sin conocer x.
