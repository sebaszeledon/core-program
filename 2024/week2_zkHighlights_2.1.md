## Highlights Week 2.1 - Tornado Cash & Semaphore

### Tornado Cash: ¿Qué es y cómo funciona?

Es un protocolo descentralizado de privacidad en Ethereum que permite a los usuarios realizar transacciones anónimas en la blockchain. Utiliza criptografía avanzada para romper los enlaces entre las direcciones de envío y recepción, proporcionando un alto grado de anonimato para las transacciones.

#### Depósitos:
* Los usuarios depositan una cantidad específica de criptomonedas en un contrato inteligente de Tornado Cash. Este depósito se asocia con una clave secreta generada por el usuario.
* El contrato inteligente acepta depósitos en denominaciones fijas, por ejemplo, 0.1 ETH, 1 ETH, 10 ETH, etc.

#### Generación de comprobante (Note):
* Al realizar el depósito, el usuario recibe una "note", que es una combinación de la clave secreta y un hash del valor depositado. Esta note es esencial para la fase de retiro.

#### Retiros:
* Para retirar los fondos, el usuario debe proporcionar la note al contrato inteligente, junto con una prueba criptográfica de conocimiento cero (zk-SNARK).
* La prueba zk-SNARK permite al contrato verificar que el solicitante es legítimo sin revelar la clave secreta ni los detalles de la transacción.
* El usuario puede retirar los fondos a una dirección de Ethereum diferente, lo que rompe el enlace entre la dirección de depósito y la de retiro, asegurando el anonimato.

#### Protección de la privacidad:
* Al permitir depósitos y retiros anónimos, Tornado Cash garantiza que las transacciones no puedan ser rastreadas en la blockchain.
* Utiliza contratos inteligentes inmutables y pruebas zk-SNARK para asegurar la privacidad de las transacciones sin requerir intermediarios.

### ¿Qué es y cómo funciona Semaphore?

Semaphore es una biblioteca y protocolo de Ethereum que permite a los usuarios generar pruebas criptográficas que demuestran la pertenencia a un grupo sin revelar la identidad del usuario ni los detalles de la transacción. Esto se logra mediante los siguientes componentes y pasos:

### Componentes

#### Identidad del Usuario:
* Definición: Cada usuario tiene una identidad única que se representa mediante un hash de su clave privada.
* Importancia: La identidad del usuario es la base para generar pruebas anónimas.

#### Árbol Merkle:
* Definición: Las identidades de los usuarios se almacenan en un árbol Merkle, que permite verificar la pertenencia de un usuario a un grupo sin revelar su identidad.
* Importancia: Utilizado para eficientemente probar la pertenencia a un grupo de manera anónima.

#### Pruebas zk-SNARK:
* Definición: Las pruebas zk-SNARK permiten verificar ciertas afirmaciones (como la pertenencia a un grupo) sin revelar ninguna información adicional.
* Importancia: Proporciona anonimato y privacidad en las transacciones.

### Pasos del funcionamiento

#### Registro de Identidad:
* Proceso: Un usuario registra su identidad (hash de la clave privada) en un contrato inteligente, que actualiza el árbol Merkle con la nueva identidad.
* Resultado: El usuario ahora está incluido en el grupo y puede generar pruebas de pertenencia.

#### Generación de Pruebas:
* Proceso: Cuando el usuario desea realizar una acción anónima, genera una prueba zk-SNARK que demuestra su pertenencia al grupo sin revelar su identidad.
* Resultado: La prueba se envía junto con la transacción a la red.

#### Verificación de Pruebas:
* Proceso: El contrato inteligente de Semaphore verifica la prueba zk-SNARK utilizando la raíz del árbol Merkle.
* Resultado: Si la prueba es válida, la acción se ejecuta, y la identidad del usuario permanece oculta.

### Aplicaciones de Semaphore

1. Votación Anónima:
    * Ejemplo: Permite a los usuarios emitir votos de manera anónima y verificar que solo los usuarios registrados puedan votar sin revelar su identidad.

2. Foros y Comentarios Privados:
    * Ejemplo: Facilita la participación anónima en foros y secciones de comentarios, asegurando que solo los miembros del grupo puedan publicar.

3. Privacidad Financiera:
    * Ejemplo: Utilizado en aplicaciones financieras para realizar transacciones sin revelar la identidad del remitente o el destinatario.
