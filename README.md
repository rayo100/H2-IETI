

Llegamos a ésta página despues de iniciar la aplicación, navegamos en http://localhost:8080/h2-console, que nos presentará una página de inicio de sesión.

![image](https://github.com/rayo100/H2-IETI/assets/89558695/60343d4d-5a2c-4a6f-8270-852e5a025dbb)

En la página de inicio de sesión, proporcionaremos las mismas credenciales que usamos en application.properties y cambiamos la URL por la nuestra.

![image](https://github.com/rayo100/H2-IETI/assets/89558695/d6448903-978a-4f58-bae5-a079e33a6f17)

Una vez que nos conectemos, veremos una página web completa que enumera todas las tablas en el lado izquierdo de la página y un cuadro de texto para ejecutar consultas SQL

![image](https://github.com/rayo100/H2-IETI/assets/89558695/b2b68fa0-8a03-44d0-9e01-e2323a117dcf)

La consola web tiene una función de autocompletar que sugiere palabras clave SQL. El hecho de que la consola sea liviana la hace útil para inspeccionar visualmente la base de datos o ejecutar SQL sin procesar directamente.

Además, podemos configurar aún más la consola especificando las siguientes propiedades en application.properties del proyecto con nuestros valores deseados:

  spring.h2.console.path=/h2-console
  spring.h2.console.settings.trace=false
  spring.h2.console.settings.web-allow-others=false

configuramos la ruta de la consola para que sea /h2-console, que es relativa a la dirección y el puerto de nuestra aplicación en ejecución. Por lo tanto, si nuestra aplicación se ejecuta en http://localhost:9001, la consola estará disponible en http://localhost:9001/h2-console.

Además, establecemos spring.h2.console.settings.trace en false para evitar la salida de rastreo, y también podemos deshabilitar el acceso remoto configurando spring. h2.console.settings.web-allow-others a false.
