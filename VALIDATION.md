# Estado de validación

Comprobaciones locales realizadas el 18 de noviembre de 2026:

- El parche modifica ocho archivos y se aplica al commit `4ac201fdc56127de27de34567286885f4e75d194` sin conflictos.
- El resultado coincide con los archivos editados al normalizar los finales de línea de Windows. También pasa la comprobación de aplicación inversa.
- `git diff --check` pasa.
- Los menús XML en español e inglés se analizan correctamente.
- `actionlint` no encuentra errores en el flujo de GitHub Actions.
- Tree-sitter C++ no encuentra errores en los cuatro archivos modificados de cámara y herramientas. Los dos archivos grandes de menús y ventana conservan los diagnósticos que ya aparecen en el código original (16 y 9); esta comparación no equivale a compilar C++.

SHA-256 del parche: `7b0d66837bb51185557c9d3b64438ee7b4f412770268d55dc9e4011e9d507772`.

## Compilación de Windows completada

- [GitHub Actions, ejecución 44327382990](https://github.com/endybell/firestorm-third-person-steering/actions/runs/44327382990): correcta.
- Commit del repositorio de parche compilado: `0f71bf88e5abc31b0623d62ce14a0f48e8652f19`.
- Aplicación del parche, configuración, compilación, enlazado y empaquetado completados. MSBuild informa 0 errores y 0 advertencias.
- Instalador: `Phoenix-Firestorm-ThirdPersonSteering_LEGACY-7-2-5-1_Setup.exe`, 225179943 bytes.
- SHA-256 del instalador verificado después de descargar: `1ba4fa84d6b58bab3e6adbd455ca3ae549de1cd1765e7cfac71e99b3444afb99`.
- SHA-256 del ZIP descargado coincide con el publicado por Actions: `9fc3c390f9dc633919540b530e82084ce8f6e318d58ddc9a41a24e709e7d3a8c`.
- El ZIP generado durante esta primera ejecución contiene las instrucciones anteriores a la confirmación del resultado; este documento refleja el estado posterior verificado.

**Pendiente:** instalación y pruebas dentro de Second Life descritas en `TESTING.md`. No se ha ejecutado el instalador ni se ha comprobado todavía la interacción de cámara en una sesión real.
