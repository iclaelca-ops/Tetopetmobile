# Teto Pet Mobile — prototipo Android

**Estado:** codigo fuente inicial; el APK aun no esta compilado ni probado en un dispositivo.

## Que incluye este prototipo
- Servicio de mascota flotante con permiso Android `SYSTEM_ALERT_WINDOW`.
- Se puede arrastrar sobre otras aplicaciones.
- Al tocarla cambia entre cuatro etiquetas/estados y emite un pitido.
- Animacion de flotacion sencilla.
- Flujo de GitHub Actions para compilar y entregar un APK de depuracion.

## Lo que aun falta
- El dibujo actual es un marcador provisional, NO la Teto exacta del video.
- Faltan sprites transparentes reales, animaciones de caminar/bailar/dormir y voz grabada.
- Android puede ocultar overlays en algunas pantallas protegidas o seguras.
- La compilacion en GitHub Actions debe ejecutarse y revisarse antes de considerar el APK funcional.

## Compilar desde el telefono (sin PC)
1. Crea una cuenta en GitHub desde el navegador del telefono.
2. Crea un repositorio nuevo, por ejemplo `TetoPetMobile`.
3. Sube todos los archivos/carpetas de este ZIP manteniendo la estructura. GitHub web permite subir archivos; si te resulta dificil subir carpetas, usa la opcion de subir archivos multiples o crea primero el repositorio desde el navegador y sube el contenido de cada carpeta.
4. En el repositorio, abre **Actions**. Si aparece una advertencia para habilitar workflows, habilitalos.
5. Ejecuta **Build Teto Pet APK** con **Run workflow**, o espera al flujo automatico tras subir a la rama `main`.
6. Abre la ejecucion terminada y descarga el artefacto `TetoPetMobile-debug-apk`.
7. Extrae el ZIP descargado y abre `app-debug.apk`. Android puede pedir que autorices la instalacion desde el navegador/gestor de archivos; permite solo el instalador que tu elegiste y revisa los permisos.
8. Abre Teto Pet Mobile, pulsa activar y concede **Mostrar sobre otras apps** en Ajustes.

## Estructura
- `app/`: codigo Android.
- `.github/workflows/build-apk.yml`: compilacion automatica.
- `README-ES.md`: estas instrucciones.

No compartas contrasenas ni tokens de GitHub. No hace falta pagar ni dar acceso a cuentas externas para compilar este proyecto.
