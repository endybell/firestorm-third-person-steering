# Firestorm: cámara con ratón en tercera persona

Cambio nativo para Firestorm 7.2.5. Este paquete contiene el parche y el flujo de compilación de Windows; **no es todavía un instalador**.

## Uso previsto después de compilar

- **Ctrl + Alt + Y** activa o desactiva el modo sin pulsar sobre el avatar.
- También aparece en **Avatar → Cámara con ratón en tercera persona** (en inglés: **Third-Person Mouse Steering**).
- El ratón gira la vista horizontal y verticalmente. El avatar permanece visible y gira con la cámara, como en el control normal al arrastrar el avatar.
- Con las teclas de movimiento habilitadas, W/S avanzan y retroceden; A/D se desplazan lateralmente mientras el modo está activo.
- **Esc**, un clic izquierdo o un clic derecho liberan el cursor. El clic que libera el cursor no toca objetos ni inicia la marcha.
- Cambiar de aplicación, enfocar un campo de texto, entrar en edición, cambiar de modo de cámara, sentarse o teleportarse interrumpen el modo. No se reactiva automáticamente.
- La primera versión se limita a la cámara normal en tercera persona, de pie o volando. No sustituye la cámara de vehículos, cámaras de scripts, flycam ni mouselook.

El modo no depende de RLV y conserva el recorrido normal de rotación y las restricciones de cámara del visor. No genera pulsaciones artificiales de ratón.

## Compilación en GitHub Actions

El repositorio de compilación solo necesita estos archivos, incluido `.github/workflows/build-windows.yml` y `third-person-steering.patch`.

1. Usar un repositorio privado propio para estos archivos.
2. Abrir **Actions → Build Firestorm Third Person Steering → Run workflow**.
3. Cuando finalice correctamente, descargar **Firestorm-ThirdPersonSteering-Windows-x64** en la sección **Artifacts** de esa ejecución.
4. Extraer el ZIP y ejecutar el archivo `*_Setup.exe`. El nombre del canal personalizado distingue esta instalación de Firestorm Release.
5. Completar las pruebas de `TESTING.md` antes de considerarlo validado para uso habitual.

El flujo se ejecuta únicamente de forma manual, en un único equipo Windows de GitHub. No publica una release ni sube archivos a Marketplace. Se aplican la cuota y los límites de Actions de tu cuenta.

## Base y diferencias de la compilación

- Código oficial: https://github.com/FirestormViewer/phoenix-firestorm
- Rama de referencia: `Firestorm_7.2.5`.
- Commit exacto: `4ac201fdc56127de27de34567286885f4e75d194`.
- Variables de compilación: `FirestormViewer/fs-build-variables`, commit `c17312d38377c003977cf5b6dcc83c6042eba194`.
- Canal: `Firestorm-ThirdPersonSteering`.
- Plataforma: Windows x64, Visual Studio 2022, configuración `ReleaseFS_open`.

Es una compilación personal sin firma digital del equipo de Firestorm. Usa OpenAL y OpenJPEG; no incluye las bibliotecas privadas FMOD, Kakadu ni Havok de la distribución oficial. El audio por streaming y ciertas herramientas de creación pueden diferir de la versión oficial. Esto es una diferencia del proceso de compilación abierta, no del parche de cámara. La compatibilidad del instalador y del modo dentro de Second Life todavía debe comprobarse.

## Archivos

- `third-person-steering.patch`: cambios sobre el commit indicado; se aplica con `git apply` desde la raíz del código oficial.
- `.github/workflows/build-windows.yml`: compilación y empaquetado en GitHub.
- `build-requirements.txt`: herramientas Python fijadas por versión.
- `TESTING.md`: pruebas de comportamiento pendientes dentro del visor.
- `VALIDATION.md`: comprobaciones realizadas y límites de la validación.
- `LICENSE-source.txt`: licencia del código base y del parche derivado.

El parche mantiene las cabeceras de licencia originales. No es un producto ni una actualización oficial de Firestorm.
