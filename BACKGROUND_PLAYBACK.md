# Reproducción en segundo plano

Se añadió un servicio Android de primer plano (`mediaPlayback`) y un `PARTIAL_WAKE_LOCK` para mantener activo el proceso mientras la app está reproduciendo.

Importante: la app sigue usando el YouTube IFrame Player como fuente de reproducción. Android puede mantener vivo el WebView, pero esto no elimina las restricciones de reproducción en segundo plano que pueda imponer YouTube. Para una reproducción garantizada con pantalla apagada, la fuente de audio debe permitir explícitamente ese uso.

El workflow de GitHub Actions ya no borra la carpeta `android`, por lo que conserva estos cambios nativos al compilar la APK.
