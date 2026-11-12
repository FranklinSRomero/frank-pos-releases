# Seguridad de actualizaciones

El origen publico de descargas es GitHub Releases, pero la autenticidad de los archivos depende de la **firma Ed25519 del manifiesto**, verificada por el actualizador, no de una URL ni de un SHA-256 publicado por separado.

Nunca distribuyas una version sin manifiesto firmado. Nunca publiques claves privadas. No se recomienda desactivar Microsoft Defender, SmartScreen, ni modificar configuraciones de seguridad del sistema para ejecutar una version.

Si una release presenta comportamientos anormales, suspender la distribucion y verificar el canal y las firmas antes de restaurarla.
