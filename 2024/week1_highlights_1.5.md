## Highlights Week 1.5 - Digital Signature

### ¿Qué son y por qué son esenciales en la comunicación digital?

Es una firma electrónica que asegura que un documento digital es auténtico y no ha sido alterado. Son esenciales para brindar integridad, seguridad y autenticidad.

### ¿Cómo funciona la firma digital?

1. Generación de la Firma:
    * Hash del Mensaje: Se calcula un hash del documento (o mensaje) usando una función hash.
    * Encriptación del Hash: Este hash se encripta usando la clave privada del firmante. El resultado es la firma digital.

2. Verificación de la Firma:
    * Hash del Mensaje Recibido: El receptor también calcula un hash del documento recibido.
    * Descifrado de la Firma: La firma digital se descifra usando la clave pública del firmante.
    * Comparación de Hashes: Se comparan ambos hashes. Si coinciden, la firma es válida y el documento no ha sido alterado. 
