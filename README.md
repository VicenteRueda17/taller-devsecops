# taller-devsecops

## Solución a las preguntas planteadas  

1. *Trazabilidad:* ¿Por qué es un riesgo de seguridad dejar la configuración de user.name y user.email vacía o utilizar datos genéricos en un entorno empresarial?
   
   *Respuesta:* El riesgo mayor es que al dejar en blanco o con datos genéricos se perdería la trazabilidad de poder identificar quién hizo algún cambio en el repositorio, por ende, sería imposible responsabilizar a alguien en caso tal de un incidente.
   Aparte dejaría una brecha para posibles ataques internos

2. *Cifrado asimétrico:* En el caso de usar SSH, ¿cuál es la diferencia funcional entre la llave privada y la pública? ¿Qué pasaría si un tercero obtiene acceso a tu llave privada?

   *Respuesta:*
   - La diferencia es que la llave privada se guarda en mi equipo y no se comparte con nadie más ya que es con la que solemos descifrar información o realizar firmas digitalmente y la pública es la que está montana en un servidor remoto o GitHub para permitir accesos de manera eficiente, cifrar datos y verificar firmas.
   - Si alguien nos robara la llave privada podría clonar todos nuestros repositorios, realizar push con códigos maliciosos, tener acceso a los servidores que tengan esa llave y demás.

  3. *Principio de Mínimo Privilegio:* Si decides usar un Token de Acceso Personal (PAT), ¿qué riesgos conlleva asignarle permisos de "Administrador" (Full Control) en lugar de solo permisos de "Lectura/Escritura"?

  *Respuesta:* El riesgo de asignar todo los privilegios de administrador a un usuario o token ya que como dice el principio mínimo de privilegios dice que solo se le debe asignar los permisos necesarios, si esto no se cumple, este usuario o token puede borrar repositorios, cambiar las configuraciones, si el token es robado impactaría más los riesgos de que tenga full control.  

  4. *Higiene del Repositorio:* ¿Para qué sirve el archivo .gitignore desde una perspectiva de seguridad? (Menciona al menos dos tipos de archivos que nunca deberían subirse al repositorio remoto).

     *Respuesta:* El archivo .gitignore sirve para decirle a Git qué archivos o carpetas deben ser excluidos para no subir al repositorio, evita exposición de secretos, subir dependencias innecesarias y mantiene el repositorio más limpio.

     Los dos tipos de archivos serían:
     - Archivos de credenciales y secretos como el .env o .env.local
     - Archivos del sistema como el de .DS_Store para MacOS o el Thumbs.db para Windows
    
  5. *Exposición de Secretos:* Si accidentalmente subes una llave de API o una contraseña al repositorio en GitHub, ¿es suficiente con borrarla y hacer un nuevo commit? Justifica tu respuesta.

     *Respuesta:* No es suficiente ya que GitHub es un repositorio de datos históricos, se podría encontrar la llave o lo que se haya subido en commits anteriores o ver el historial para recuperar lo que se haya subido.


*Vicente Rueda*

   
