## Week 3.1 - ZK-Auth with Noir & Passport.js

En el programa la prueba de zk-SNARK para verificar la contraseña con el circuito de Noir se realiza dentro de la función verifyPassword. Esta función se encarga de tomar la contraseña proporcionada por el usuario y el hash almacenado de esa contraseña, y luego utiliza un circuito zk-SNARK implementado en Noir para verificar si la contraseña proporcionada genera el mismo hash.

### Flujo de la Verificación:

1. Generación del Archivo Prover.toml:
    * La función verifyPassword primero genera el archivo Prover.toml que contiene las entradas necesarias para el circuito Noir. Este archivo incluye la contraseña (password) y el hash de la contraseña (hash_password).
2. Ejecución del Circuito con nargo execute:
    * Una vez que el archivo Prover.toml está preparado, el comando nargo execute -p Prover se ejecuta. Este comando utiliza las entradas en Prover.toml para calcular el valor de retorno del circuito. El valor calculado es el resultado de la comparación entre el hash calculado dentro del circuito y el hash proporcionado.
3. Generación de la Prueba con nargo prove:
    * Después de ejecutar el circuito, el comando nargo prove se utiliza para generar una prueba zk-SNARK basada en el testigo (witness) que se ha calculado en el paso anterior.
4. Verificación de la Prueba con nargo verify:
    * Finalmente, el programa utiliza el comando nargo verify para verificar la prueba zk-SNARK. Si la prueba es válida, significa que la contraseña proporcionada por el usuario es correcta, y el programa devuelve true.

### ¿Cuándo se realiza la prueba zk?

La prueba zk se realiza inmediatamente después de la llamada a nargo prove en la función verifyPassword. Esto ocurre cuando un usuario intenta autenticarse (inicia sesión) y la función verifyPassword es llamada dentro de la estrategia de autenticación de Passport.js.
En resumen, la verificación zk-SNARK de la contraseña con el circuito de Noir se realiza cuando el usuario intenta iniciar sesión, y el proceso involucra la generación de entradas, la ejecución del circuito, la creación de la prueba zk-SNARK, y finalmente, la verificación de dicha prueba.
