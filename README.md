## Preguntas

¿la ruta protegida hace segura la aplicación? ¿Qué es lo que de verdad protege los datos?
no, la ruta protegida del front solo redirige, no hace la app segura. la seguridad real esta en el back con el jwt con la validacion del token y permisos en el servidor.

lo que protege los datos es la autentificación y la autorización del back  al comprobar que el token es valido ósea que no haya expirado y que el usuario tenga permisos para usar esta ruta
y pues las contraseñas se guardan con un hash

¿por qué no se manda el miembroId al inscribirse?
por que al inscribirse el servidor lo obtiene del token del usuario autentificado , el back confía en el cliente para decidir quien es el miembro

¿qué diferencia hay entre un 401 y un 403?

el 401 es cuando no estas autentificado ósea que el token es invalido o que esta ausente 
el 403 es cuando estas autentificado pero no tienes permisos para esa accion
