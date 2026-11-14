# Frank POS — Versiones oficiales

Este repositorio se utiliza exclusivamente para distribuir **binarios compilados** de Frank POS mediante [GitHub Releases](https://github.com/FranklinSRomero/frank-pos-releases/releases). El codigo fuente de Frank POS y su actualizador no se publican aqui.

El mecanismo de actualizaciones de escritorio exige un manifiesto `latest.json`, su firma Ed25519 `latest.json.sig` y los archivos binarios indicados en el manifiesto. El cliente valida firma, version, plataforma, longitud y SHA-256 antes de activar una descarga.

## Instalacion y actualizaciones

Descarga los paquetes desde [la ultima release](https://github.com/FranklinSRomero/frank-pos-releases/releases/latest).

- **Windows x64:** extrae el paquete `bootstrap-windows-x86_64.zip` y abre `Instalar-FrankPOS.cmd` o el updater incluido. La instalacion es por usuario y crea accesos directos.
- **Linux x64:** extrae `bootstrap-linux-x86_64.tar.gz` y ejecuta `bash install-frank-pos.sh`. La build 0.3.1 requiere glibc 2.44 o posterior.

Los paquetes bootstrap incluyen el updater. Este descarga y verifica el ejecutable firmado del POS antes de activarlo. El primer inicio permite crear la cuenta administradora local. Los siguientes arranques solo comprueban novedades; instalar requiere la accion del administrador en Ajustes > Actualizaciones.

`latest.json` y `latest.json.sig` son los metadatos que consume automaticamente el updater. Los assets `linux-x86_64` y `windows-x86_64` son los ejecutables individuales del POS; los assets `bootstrap-*` son los paquetes de primera instalacion.

**Validacion:** build y ventana real en Linux; updater Windows probado bajo Wine, incluido el contrato JSON y rollback. El renderizado del POS, accesos directos y perifericos requieren validacion adicional en Windows real. Wine no implementa los recursos DirectX que necesita GPUI.

> Advertencia: los ejecutables sin una firma Authenticode reconocida pueden mostrar avisos de SmartScreen u otras protecciones de Windows, incluso descargados desde GitHub. No se pide desactivar esas protecciones.

El codigo privado, las claves de firma, los archivos de pruebas y el historial de desarrollo nunca deben subirse a este repositorio.
