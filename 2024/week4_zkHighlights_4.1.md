## ¿Cómo Funciona PLONK?

Imagina que quieres demostrar que has realizado correctamente un cálculo complejo, pero no quieres revelar los detalles de cómo lo hiciste. 
PLONK te permite hacerlo a través de un "prover" (quien hace la prueba) y un "verifier" (quien verifica la prueba) sin que el verifier necesite ver todos los detalles.

### 1. Preparación:
El prover crea un circuito que representa el cálculo que quiere demostrar. Este circuito es como un esquema que define cómo se deben hacer las operaciones para obtener un resultado.
Luego, el prover traduce este circuito en un sistema algebraico llamado un circuito aritmético, que representa el cálculo en términos de polinomios.
### 2. Compromiso:
El prover calcula ciertos valores sobre el circuito aritmético y se compromete a estos valores sin revelar los cálculos internos. Esto se hace utilizando algo llamado un commitment scheme, que es como poner los valores en una caja cerrada que el verifier puede comprobar más tarde, pero sin poder ver dentro de la caja.
### 3. Prueba de consistencia:
El prover necesita demostrar que los valores comprometidos realmente corresponden a una ejecución correcta del circuito aritmético. Aquí es donde entra en juego la "permutación sobre bases de Lagrange", un método matemático que garantiza que las permutaciones (cambios de orden de los valores) son consistentes con las reglas del circuito.
### 4. Prueba y Verificación:
Usando herramientas matemáticas como las transformadas de Fourier y polinomios, el prover crea una prueba que puede ser verificada rápidamente por el verifier. Lo más interesante es que el verifier no necesita hacer cálculos complejos, solo necesita hacer unas pocas verificaciones para estar seguro de que el cálculo fue correcto.

## Ventajas de PLONK

### Eficiencia: 
PLONK es más rápido y más eficiente que muchos otros protocolos de prueba de conocimiento cero, especialmente porque las pruebas son cortas y se verifican rápidamente.
### Universalidad: 
PLONK puede ser usado para cualquier circuito, lo que lo hace muy flexible.
### Tamaño pequeño: 
Las pruebas generadas por PLONK son muy pequeñas en comparación con otros sistemas, lo que es ideal para aplicaciones donde se necesita transmitir poca información.
