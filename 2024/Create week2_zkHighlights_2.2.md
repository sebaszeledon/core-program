## Highlights Week 2.2 - KZG & Trusted setups

### ¿Qué son los compromisos KZG?

Un compromiso KZG es un esquema de compromiso polinomial utilizado para vincular un “prover” a un conjunto específico de datos.

El compromiso actúa como un ancla, una prueba implica una rápida división polinomial y la verificación es una comprobación sencilla. 

El verificador puede saber con certeza matemática que el probador está cumpliendo con su compromiso; cualquier dato existente es el mismo que creó el compromiso.

Los compromisos de KZG también tienen una característica muy útil: se pueden abrir (auditar) en cualquier posición sin revelar ningún dato no relacionado.

### ¿Qué es un Trusted Setup?

Un Trusted Setup es un proceso criptográfico crucial en la generación de pruebas de conocimiento cero (ZKPs), particularmente en sistemas como zk-SNARKs. 

### Fases del Trusted Setup

1. Ceremonia de Configuración:
    * Un grupo de participantes colabora para generar los parámetros iniciales.
    * Cada participante contribuye con su parte de la generación de los parámetros y, idealmente, si al menos uno de ellos actúa de manera honesta y destruye su parte secreta, el proceso es seguro.
2. Generación de Parámetros Públicos y Privados:
    * Se crean parámetros públicos que son utilizados por todos los participantes para crear y verificar pruebas.
    * Los parámetros privados son destruídos después de la configuración para asegurar que no puedan ser reutilizados o comprometidos.
3. Destrucción de Secretos:
    * Es crucial que cualquier información secreta generada durante el setup sea destruida.
    * Se utilizan diversas técnicas para asegurar que los participantes no puedan conservar los secretos.
