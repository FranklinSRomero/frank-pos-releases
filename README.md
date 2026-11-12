# Frank POS — Versiones oficiales

Este repositorio se utiliza exclusivamente para distribuir **binarios compilados** de Frank POS mediante [GitHub Releases](../../releases). El codigo fuente de Frank POS y su actualizador no se publican aqui.

El mecanismo de actualizaciones de escritorio exige un manifiesto `latest.json`, su firma Ed25519 `latest.json.sig` y los archivos binarios indicados en el manifiesto. El cliente valida firma, version, plataforma, longitud y SHA-256 antes de activar una descarga.

**Estado:** canal preparado para las futuras versiones; aun no existe un paquete de produccion validado.

> Advertencia: los ejecutables sin una firma Authenticode reconocida pueden mostrar avisos de SmartScreen u otras protecciones de Windows, incluso descargados desde GitHub. No se pide desactivar esas protecciones.

El codigo privado, las claves de firma, los archivos de pruebas y el historial de desarrollo nunca deben subirse a este repositorio.
