# MGP-VM

Entorno de trabajo para la Metodología de Geolocalización Pericial (MGP), basado en Trace Labs OSINT VM.

Desarrollado como parte del Trabajo Fin de Máster *Diseño e implementación de una metodología OSINT para la geolocalización de contenidos digitales* (Máster Universitario en Seguridad de las Tecnologías de la Información y las Comunicaciones, Universidad Europea, 2026).

## Descarga

| | |
|---|---|
| Versión | 1.1 |
| Archivo | `MGP-VM-v1.1.ova` |
| Enlace | [Google Drive] (https://drive.google.com/file/d/1gVENQYbAFRbaNQhimZ53BmeGpKP0BxtC/view?usp=drive_link) |
| SHA-256 | `5cc2434792dd381c3d5ee3b302151272c1da2c8e12d0652287765293762c41fb` |

## Comprobar la integridad

Antes de importar la máquina, calcula el hash del archivo descargado y compáralo con el de la tabla. Si no coinciden, el archivo está dañado o fue modificado: no lo uses.

Windows (PowerShell):

```
Get-FileHash .\MGP-VM-v1.1.ova -Algorithm SHA256
```

Linux:

```
sha256sum MGP-VM-v1.1.ova
```

macOS:

```
shasum -a 256 MGP-VM-v1.1.ova
```

## Importar

En VirtualBox: **Archivo → Importar servicio virtualizado** y selecciona el `.ova`. Requisitos recomendados: procesador de 64 bits, 8 GB de RAM y 40 GB libres en disco.

## Contenido

Sobre la base de Trace Labs OSINT VM 2026.7, la máquina añade:

- **Plantillas de la MGP**: una plantilla por fase (F1 a F6) y un documento completo, en `Plantillas-MGP`.
- **Estructura de casos**: instrucciones para abrir y organizar cada caso, en `Plantillas-MGP/Casos-MGP`.
- **Herramientas**: SingleFile, InVID-WeVerify 0.89.1, SimpleScreenRecorder 0.4.4 y ffmpeg 7.1.5.
- **Marcadores** de servicios de verificación y geolocalización, incluido WasItAI.
- **Documentación de herramientas** en `LEEME-herramientas.txt`, incluidas las instrucciones para instalar Whisper, que no viene instalado.

Las plantillas y la documentación también están en este repositorio, para consultarlas sin descargar la máquina.

## Licencia

Las aportaciones propias de este proyecto (plantillas, configuración, marcadores y documentación de la MGP) se distribuyen bajo la licencia [Creative Commons Atribución 4.0 Internacional (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.es). Ver [`LICENSE`](LICENSE).

Cita sugerida:

> Martínez Aguilera, I. F. (2026). *MGP-VM: entorno de trabajo para la Metodología de Geolocalización Pericial* (v1.1). https://github.com/IvanMar19/MGP-VM

### Componentes de terceros

La máquina virtual se basa en la [Trace Labs OSINT VM](https://github.com/tracelabs/tlosint-vm) 2026.7, distribuida bajo GPL v3, que a su vez es una versión modificada de [Kali Linux](https://www.kali.org/docs/policy/kali-linux-open-source-policy/). Estos componentes y las herramientas instaladas (SingleFile, InVID-WeVerify, SimpleScreenRecorder, ffmpeg y demás) conservan sus propias licencias. La licencia CC BY 4.0 no se aplica a ellos.
