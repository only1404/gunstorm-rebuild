# GunStorm 1.0.3 — análisis y reconstrucción

Este repositorio contiene una reconstrucción jugable independiente basada en recursos recuperados del APK de GunStorm 1.0.3. **No es el código fuente original ni un port exacto.**

## Generar APK Android ARM64
1. Abre la pestaña **Actions**.
2. Selecciona **Build Gunstorm Android ARM64**.
3. Pulsa **Run workflow** en la rama `main`.
4. Cuando termine correctamente, descarga el artefacto `Gunstorm-Rebuilt-Android-ARM64`.

El flujo extrae el ZIP del proyecto, configura el preset de exportación Android ARM64 y construye el APK.

## Límite del juego original
El APK original disponible contiene `lib/armeabi/libgame.so` (ARM de 32 bits) y no incluye una biblioteca `arm64-v8a` ni código fuente C/C++. Cambiar el manifiesto o firmar de nuevo el APK no convierte esa biblioteca a ARM64. La reconstrucción es una alternativa para dispositivos modernos, no el original exacto.
