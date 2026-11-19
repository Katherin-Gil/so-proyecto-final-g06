# Ficha de verificación · Grupo 06

## openSUSE Leap 16.1 (VM gráfica)

| Pregunta | Respuesta | Enlace donde lo comprobamos | 
| :--- | :--- | :--- |
| Versión elegida y fecha de lanzamiento | openSUSE Leap 16.1, lanzada el 3 de noviembre de 2026. | https://en.opensuse.org/Portal:16.1 |
| Hasta cuándo recibe actualizaciones de seguridad | Fin de vida (EOL) el 31 de octubre de 2028. | https://en.opensuse.org/openSUSE:Roadmap |
| Requisitos de hardware y si funciona en VirtualBox | Requiere CPU x86_64-v2 (fabricados desde ~2007-2008), mínimo 1024 MB de RAM mínimo y 10-16 GB de disco. Sí funciona en VirtualBox. | https://en.opensuse.org/Hardware_requirements_16.1 |
| ¿El instalador permite particionado manual? | Sí, el instalador Agama permite la configuración experta de particiones. | https://en.opensuse.org/Agama |
| Guía oficial para instalar Docker Engine | Docker no tiene guía oficial para openSUSE. Se instala desde los repositorios oficiales de openSUSE | https://en.opensuse.org/SDB:Docker |
| Imagen de base del DockerFile | La imagen oficial `opensuse/leap:16.1` existe en Docker Hub. | https://hub.docker.com/r/opensuse/leap/tags |

## Debian 13.7.0 "Trixie" (VM de consola)

| Pregunta | Respuesta | Enlace donde lo comprobamos | 
| :--- | :--- | :--- |
| Versión elegida y fecha de lanzamiento | Debian 13.7.0 "Trixie", lanzada el 12 de septiembre de 2026. | https://www.debian.org/releases/trixie/ |
| Hasta cuándo recibe actualizaciones de seguridad | Soporte completo hasta el 9 de agosto de 2028 y soporte LTS hasta el 30 de junio de 2030. | https://www.debian.org/security/ |
| Requisitos de hardware y si funciona en VirtualBox | Se recomienda al menos 1 GB de RAM y 25 GB de disco. Sí funciona en VirtualBox. | https://www.debian.org/releases/trixie/installmanual |
| ¿El instalador permite particionado manual? | Sí, el instalador permite seleccionar "Manual" en el particionado. | https://www.debian.org/releases/trixie/amd64/ch06s03 |
| Guía oficial para instalar Docker Engine | Docker proporciona una guía oficial para Debian 13 (Trixie). | https://docs.docker.com/engine/install/debian/ |
| Imagen de base del DockerFile | La imagen oficial `debian:trixie` existe en Docker Hub | https://hub.docker.com/_/debian |

## AlmaLinux 9.8 (Imagen base del Dockerfile)

| Pregunta | Respuesta | Enlace donde lo comprobamos | 
| :--- | :--- | :--- |
| Versión elegida y fecha de lanzamiento | AlmaLinux 9.8 "Olive Jaguar", lanzada el 26 de mayo de 2026. | https://almalinux.org/blog/2026-05-26-almalinux_98_and_102_stable/ |
| Hasta cuándo recibe actualizaciones de seguridad | Soporte de seguridad hasta el 31 de mayo de 2032. | https://wiki.almalinux.org/release-notes/9.8.html |
| Requisitos de hardware y si funciona en VirtualBox | Se recomienda al menos 2 GB de RAM y 20 GB de disco. Sí funciona en VirtualBox. | https://wiki.almalinux.org/documentation/installation-guide.html |
| ¿El instalador permite particionado manual? | Sí, el instalador Anaconda permite la configuración personalizada. | https://wiki.almalinux.org/documentation/installation-guide.html |
| Guía oficial para instalar Docker Engine | Docker proporciona una guía oficial para RHEL/CentOS que aplica a AlmaLinux. | https://docs.docker.com/engine/install/centos/ |
| Imagen de base del DockerFile | La imagen oficial `almalinux:9.8` existe en Docker Hub. | https://hub.docker.com/r/almalinux/almalinux/tags |
