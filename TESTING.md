# Pruebas dentro del visor

Estado: compilación completada correctamente; estas pruebas siguen pendientes en una sesión real de Second Life.

## Cámara y movimiento

1. Iniciar sesión, permanecer de pie en tercera persona y colocar el puntero sobre el cielo o el suelo, lejos del avatar. Pulsar Ctrl+Alt+Y. La cámara debe responder al ratón sin mantener botones; no debe entrar en mouselook.
2. Mirar hacia arriba y caminar con W: la cámara debe conservar la inclinación. A/D deben desplazar lateralmente. Soltar W debe detener el avance.
3. Repetir mientras se vuela. Verificar que la cámara no añade el retraso que el visor normalmente desactiva al arrastrar el avatar.
4. Repetir después de seleccionar órbita y desplazamiento en el panel de cámara. Esas selecciones no deben cambiar el funcionamiento del modo nuevo.
5. Mantener Ctrl+Alt+Y pulsado: no debe alternar repetidamente. Soltar y pulsar de nuevo debe liberar el cursor.
6. Activar desde el menú Avatar; comprobar la traducción española y el menú inglés.

## Salida y recuperación del cursor

7. Pulsar Esc. El cursor debe reaparecer y poder salir de la ventana. El ratón debe dejar de girar la cámara.
8. Repetir con clic izquierdo y derecho. El primer clic solo libera el cursor; no toca un objeto, abre su menú ni inicia marcha automática.
9. Cambiar de aplicación con Alt+Tab y volver. El modo debe estar apagado, con el cursor libre.
10. Abrir chat o inventario por teclado. Al recibir el foco, la ventana debe ser utilizable con el cursor y la cámara debe detenerse.
11. Entrar en edición, apariencia, mouselook o flycam. El modo debe apagarse sin impedir el cambio de herramienta.
12. Sentarse, teleportarse y desconectarse con el modo activo. El cursor debe liberarse; volver a caminar no debe reactivar el modo.
13. Después de salir, probar Alt+arrastrar y el clic mantenido sobre el avatar: ambos controles anteriores deben seguir funcionando.

## Configuración y restricciones

14. Repetir a escalas de interfaz 100 % y 150 %, y después de redimensionar la ventana. No debe haber saltos al activar ni al liberar el cursor.
15. Verificar con los ajustes habituales de suavizado y MouseWarpMode. El modo usa el sistema de centrado del visor; desactivar el centrado puede limitar el giro al borde de pantalla.
16. Con un objeto propio de prueba, activar restricciones RLV de distancia/cámara; el nuevo modo debe conservarlas. Si una restricción fuerza mouselook, el modo debe salir.
17. Intentar activarlo en la pantalla de acceso, sentado, en una cámara de vehículo o durante edición: debe estar deshabilitado.
18. Confirmar audio, voz y reproducción multimedia por separado: la compilación abierta usa bibliotecas distintas de la distribución oficial.

Registrar versión, resultado y cualquier error. Un flujo de GitHub verde confirma compilación y empaquetado; no confirma estas pruebas de interacción.
