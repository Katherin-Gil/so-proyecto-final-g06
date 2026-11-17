# Sprint 1 · Montaje

> Página del Sprint 1 del grupo 06. Aquí documentamos lo que hicimos, los comandos usados y las capturas. [Volver al inicio](./)

- **Qué se pide en este sprint (5 puntos):** VM gráfica, VM de consola, red, SSH e instantáneas.
- **Qué se entrega en el campus:** el enlace de este sitio.
- **Qué más:** el video de 3 minutos (al final de esta página), 2 commits por integrante y el archivo `codigo_sprint1.txt` en el home del usuario principal de las dos VMs.

## 1. VM gráfica (g06-grafica) 

Instalamos **openSUSE Leap** con particionado manual: `/`, swap y `/home`. No usamos «borrar el disco».

| Partición | Tamaño | Por qué |
| :--- | :--- | :--- |
| / | 15 GB | El sistema y los programas de openSUSE, con margen para actualizar |
| swap | 2 GB | Igual a la RAM de la VM, por si falta memoria |
| /home | 8 GB | Los archivos de los usuarios, separados del sistema |

Dos navegadores y dos editores instalados: [Ej: Firefox y Chromium, nano y gedit - *Daniel debe confirmar cuáles instaló*].

Comandos: `lsblk`, `df -h`, `cat /etc/fstab`

**[Captura 1: editor de particiones durante la instalación]**

**[Captura 2: lsblk, df -h y cat /etc/fstab, con el prompt usuario@g06-grafica y la salida de date]**

**[Captura 3: los dos navegadores y los dos editores abiertos]**

## 2. VM de consola (g06-consola)

Instalamos **Debian** con particionado manual: `/`, swap, `/home` y `/var`. Disco de 25 GB y 2 CPU.

| Partición | Tamaño | Por qué |
| :--- | :--- | :--- |
| / | 5 GB | El sistema base de Debian, sin entorno gráfico |
| /var | 12 GB | Docker guarda sus imágenes en /var/lib/docker (necesita espacio) |
| swap | 2 GB | Para evitar problemas de memoria |
| /home | 6 GB | Para los archivos de los scripts y el usuario principal |

Herramientas instaladas: make, rsync, curl, git y wget.

Comandos: `lsblk`, `df -h`, `cat /etc/fstab`, `make --version`, `rsync --version`, `curl --version`, `git --version`, `wget --version`

**[Captura 4: lsblk, df -h, y cat /etc/fstab de g06-consola, con prompt y fecha]**

**[Captura 5: las cinco herramientas mostrando su versión]**

## 3. Red

Cada VM tiene dos adaptadores: el 1 en NAT (internet) y el 2 en red solo-anfitrión (para verse entre ellas).

Comandos: `ip a` en cada VM y `ping` en los dos sentidos.

**[Captura 6: ip a en las dos VMs, mostrando una dirección en cada interfaz]**

**[Captura 7: ping de la gráfica a la consola y de la consola a la gráfica]**

## 4. SSH

Entramos por SSH desde la VM gráfica a la VM de consola.

Comando: `ssh usuario@direccion-de-la-consola`

**[Captura 8: la sesión SSH abierta, con el prompt de la consola]**

## 5. Instantáneas

Una por VM, llamada `instalacion-limpia`, tomada con la VM apagada y la instalación terminada.

**[Captura 9: pestaña de instantáneas de g06-grafica]**

**[Captura 10: pestaña de instantáneas de g06-consola]**

## Código del sprint

El docente publicó el código en el campus 48 horas antes del cierre. Lo guardamos en las dos VMs y lo mostramos en el video.

Comandos: `echo "XX00-AB12" > codigo_sprint1.txt`, `cat codigo_sprint1.txt` y `date`

## Video del sprint (3 minutos)

Pantalla continua y sin cortes. Cada integrante muestra su parte, dice su nombre y qué hizo en los primeros 10 segundos, y aparece su cara.

[Enlace del video de YouTube aquí]

## Lo que hizo cada integrante en este sprint

| Integrante | Qué hizo | Commits |
| :--- | :--- | :--- |
| Katherin | Creó las páginas del sitio, la plantilla y revisó la ficha | 1 |
| Daniel | Instaló openSUSE Leap y Debian, configuró la red, SSH y las instantáneas | [Número] |
| Dylan | Instaló las herramientas en Debian, grabó el video y subió las capturas al sitio | [Número] |
| Samuel | [Qué hizo] | [Número] |



