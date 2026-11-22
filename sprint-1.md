# Sprint 1 · Montaje

> Página del Sprint 1 del grupo 06. Aquí documentamos lo que hicimos, los comandos usados y las capturas. [Volver al inicio](./)

- **Qué se pide en este sprint (5 puntos):** VM gráfica, VM de consola, red, SSH e instantáneas.
- **Qué se entrega en el campus:** el enlace de este sitio.
- **Qué más:** el video de 3 minutos (al final de esta página), 2 commits por integrante y el archivo `codigo_sprint1.txt` en el home del usuario principal de las dos VMs.

## 1. VM gráfica (g06-grafica)

Instalamos **openSUSE Leap 16.1** con particionado manual: `/`, swap y `/home`. No usamos «borrar el disco».

| Partición | Tamaño | Por qué |
| :--- | :--- | :--- |
| / | 15 GB | El sistema y los programas de openSUSE, con margen para actualizar |
| swap | 2 GB | Igual a la RAM de la VM, por si falta memoria |
| /home | 8 GB | Los archivos de los usuarios, separados del sistema |

Dos navegadores y dos editores instalados: **Firefox** y **Chromium** (navegadores), **nano** y **Kate** (editores de texto).

Comandos: `date`, `lsblk`, `df -h`, `cat /etc/fstab`

* **Particionado durante la instalación (`g06-grafica`):**
  ![Captura 1: editor de particiones durante la instalación](img/Caps%20de%20g06-grafica/01-particiones-grafica-sprint01.png)

* **Verificación de particiones (`daniel@g06-grafica`):**
  ![Captura 2.1: lsblk, df -h y cat /etc/fstab con prompt y date](img/Caps%20de%20g06-grafica/02.1-particiones-grafica-sprint01.png)
  ![Captura 2.2: salida de df -h y cat /etc/fstab](img/Caps%20de%20g06-grafica/02.2-particiones-grafica-sprint01.png)
  ![Captura 2.3: continuación de cat /etc/fstab](img/Caps%20de%20g06-grafica/02.3-particiones-grafica-sprint01.png)

* **Navegadores y editores abiertos al mismo tiempo:**
  ![Captura 3: los dos navegadores y los dos editores abiertos](img/Caps%20de%20g06-grafica/03-navegadores-editores-grafica-sprint01.png)

## 2. VM de consola (g06-consola)

Instalamos **Debian 13.7** con particionado manual: `/`, `/var`, swap y `/home`. Disco de 25 GB y 2 CPU.

| Partición | Tamaño | Por qué |
| :--- | :--- | :--- |
| / | 5 GB | El sistema base de Debian, sin entorno gráfico |
| /var | 12 GB | Docker guarda sus imágenes en /var/lib/docker (necesita espacio) |
| swap | 2 GB | Para evitar problemas de memoria |
| /home | 6 GB | Para los archivos de los scripts y el usuario principal |

Herramientas instaladas: make, rsync, curl, git y wget.

Comandos: `date`, `lsblk`, `df -h`, `cat /etc/fstab`, `make --version`, `rsync --version`, `curl --version`, `git --version`, `wget --version`

* **particion durante la instalación (`g06-consola`):**
  ![Particionado manual en instalador de Debian](img/caps%20de%20g06-consola/04-particiondiscos-consola-sprint01.png)

* **Verificación de particiones en terminal (`daniel@g06-consola`):**
  ![Captura 4: lsblk, df -h y cat /etc/fstab de g06-consola](img/caps%20de%20g06-consola/05-particiones-consola-sprint01.png)

**[Captura 5: las cinco herramientas mostrando su versión]**

## 3. Red

Cada VM tiene dos adaptadores: el 1 en NAT (internet) y el 2 en red solo-anfitrión (para verse entre ellas).

Comandos: `ip a` en cada VM y `ping` en los dos sentidos.

* **Direcciones IP en ambas VMs (`ip a`):**
  ![Captura 6a: ip a en g06-grafica](img/Caps%20de%20g06-grafica/06-direccionesIP-grafica-sprint01.png)
  ![Captura 6b: ip a en g06-consola](img/caps%20de%20g06-consola/06-direccionesIP-consola-sprint01.png)

* **Pruebas de red (`ping`):**
  ![Captura 7a: ping desde g06-grafica hacia g06-consola](img/Caps%20de%20g06-grafica/07-paquetes-grafica-sprint01.png)
  ![Captura 7b: ping desde g06-consola hacia g06-grafica](img/caps%20de%20g06-consola/07-paquetes-consola-sprint01.png)

## 4. SSH

Entramos por SSH desde la VM gráfica (`g06-grafica`) a la VM de consola (`g06-consola`).

Comando: `ssh daniel@192.168.56.102`

![Captura 8: sesión SSH abierta con el prompt de g06-consola](img/Caps%20de%20g06-grafica/08-hostname-grafica-sprint01.png)

## 5. Instantáneas

Una por VM, llamada `instalacion-limpia`, tomada con la VM apagada y la instalación terminada.

![Capturas 9 y 10: pestaña de instantáneas instalacion-limpia en g06-grafica y g06-consola](img/09-instantaneas-virtualbox-sprint01.png)

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
| Daniel | Instaló openSUSE Leap y Debian, configuró la red, SSH, las instantáneas y subió las capturas | 3 |
| Dylan | Instaló las herramientas en Debian, grabó el video y completó las validaciones | [Número] |
| Samuel | [Qué hizo] | [Número] |
