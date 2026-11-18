# Estado de validación

Comprobaciones locales realizadas el 18 de noviembre de 2026:

- El parche modifica ocho archivos y se aplica al commit `4ac201fdc56127de27de34567286885f4e75d194` sin conflictos.
- El resultado coincide con los archivos editados al normalizar los finales de línea de Windows. También pasa la comprobación de aplicación inversa.
- `git diff --check` pasa.
- Los menús XML en español e inglés se analizan correctamente.
- `actionlint` no encuentra errores en el flujo de GitHub Actions.
- Tree-sitter C++ no encuentra errores en los cuatro archivos modificados de cámara y herramientas. Los dos archivos grandes de menús y ventana conservan los diagnósticos que ya aparecen en el código original (16 y 9); esta comparación no equivale a compilar C++.

SHA-256 del parche: `7b0d66837bb51185557c9d3b64438ee7b4f412770268d55dc9e4011e9d507772`.

**Pendiente:** compilación y enlazado en Windows, generación del instalador y pruebas dentro de Second Life descritas en `TESTING.md`. No se ha comprobado todavía el funcionamiento en ejecución.
