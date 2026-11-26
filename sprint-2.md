# Sprint 2 · Servicios

> Página del Sprint 2 del grupo 06. Aquí documentamos lo que hicimos, los comandos usados y las capturas. [Volver al inicio](./)

- **Qué se pide en este sprint (8 puntos):** Usuarios y grupos, sudo y permisos, Firewall, Llave SSH y actualización, Script gráfico, Procesos y Docker Engine.
- **Qué se entrega en el campus:** el enlace de este sitio.
- **Qué más:** el video de 4 minutos (el final de esta página), 2 commits por integrante y el archivo `codigo_sprint2.txt` en el home del usuario principal de la VM de consola. Todo se hace en la VM de consola, salvo lo que diga la guía.

## 1. Usuarios y grupo
creamos un usuario por integrante, el grupo `proyecto` y la carpeta `/srv/proyecto` con permisos de lectura/escritura solo para el grupo.

Comandos: `sudo groupadd proyecto`, `sudo useradd -m -g proyecto [usuario]`, `sudo mkdir /srv/proyecto`, `sudo chown root:proyecto /srv/proyecto`, `sudo chmod 770 /srv/proyecto`, `id [usuario]`, `getent group proyecto`, `ls -ld /srv/proyecto/`.

* **Acceso permitido y denegado:**
![Captura 1: id, getent y ls -ld, con acceso permitido y negado])()

## 2. sudo y permisos
Asignamos sudo a un usuario y se lo negamos a otro. Mostramos un ejemplo de `chmod` y `chown`. Indicamos que el grupo de administradores en Debian es `sudo`.

Comandos: `sudo usermod -aG sudo [usuario1]`, `sudo chmod 640 [archivo]`, `sudo chown [usuario2]:[grupo] [archivo]`, `sudo -l -U [usuario]`.

* **sudo permitido, sudo negado, chmod y chown:**
![Captura 2: pruebas de sudo y cambios de permisos]()

## 3. Firewall
Activamos el firewall (UFW en Debian) permitiendo SSH y negando lo demás. Levantamos un servidor en el puerto 8080 y probamos con `curl` desde la VM gráfica.

Comandos: `sudo ufw enable`, `sudo ufw allow ssh`, `sudo ufw status verbose`, `python3 -m http.server 8080` (en consola), `curl http://[IP-consola]:8080` (desde gráfica), `sudo ufw allow 8080/tcp`.

* **Estado del Firewall y los dos curl (falla y responde):**
![Captura 3: estado de ufw y curl fallido]()
![Captura 4: curl exitoso tras abrir el puerto]()

## 4. Llave SSH y actualización
Generamos el par de llaves en la VM gráfica, copiamos la pública a la consola y entramos sin contraseña. Actualizamos el sistema.

Comandos: `ssh-keygen -t ed25519`, `ssh-copy-id [usuario]@[IP-consola]`, `ssh [usuario]@[IP-consola]` (sin contraseña), `sudo apt update && sudo apt upgrade -y`.

* **Ingreso por llave y actualización terminada:**
![Captura 5: ssh sin contraseña y apt upgrade finalizado]()

## 5. Script gráfico
Creamos un script en Bash que hace una tarea útil con archivos (función, if, ciclo y comentarios). Lo ejecutamos desde un lanzador `.desktop` con ícono.

Comandos: `nano mi_script.sh`, `chmod +x mi_script.sh`, `nano ~/.local/share/applications/miscript.desktop`.

* **Código en el repositorio y ejecución desde el ícono:**
![Captura 6: script gráfico ejecutándose desde el menú de aplicaciones]()

## 6. Script de consola
Script con un argumento, validaciones, mensajes claros y código de salida distinto de cero cuando falle. Hace copia de seguridad de `/srv/proyecto`.

Comandos: `nano backup.sh`, `./backup.sh /srv/proyecto`, `./backup.sh` (caso que falla).

* **Caso que funciona y caso que falla:**
![Captura 7: ejecución exitosa y fallida del script de consola]()

## 7. Procesos
Mostramos `ps`, `top/htop`, `pstree`, `pgrep`; usamos `kill`, `pkill`, `nice`, `renice`; leemos `/proc`. Mostramos procesos en estado R, S, T y Z usando el programa `zombi.py`.

Comandos: `ps -eo pid,ppid,stat,comm`, `top`, `pstree -p`, `pgrep -l [proceso]`, `kill [PID]`, `pkill [nombre]`, `nice -n 10 [comando]`, `renice 5 -p [PID]`, `cat /proc/[PID]/status`, `python3 zombi.py`

* **Comandos de procesos y el zombi:**
![Captura 8: procesos en estado R, S, T y Z con ps]()

## 8. Docker Engine
* **Paso 1: Revision y desinstalación de paquetes en conflicto.**
Revisa la lista que muestra apt antes de confirmar.
<img width="1686" height="1051" alt="imagen" src="https://github.com/user-attachments/assets/12990098-6828-4bef-bbda-4f489ac3d1ac" />

* **Paso 2: Configurar repositorio oficial.**
* Primero, agrega la clave GPG de Docker:
<img width="1682" height="1051" alt="imagen" src="https://github.com/user-attachments/assets/e4395570-cf8b-484e-9ecf-399b21dafa38" />

* Luego se agrega el repositorio:



* **Docker funcionando sin sudo y hello-world:**
![Captura 9: docker version, hello-world y Docker Root Dir]()

## Código del sprint
El docente publicó el código en el campus 48 horas antes del cierre. Lo guardamos en la VM de consola y lo mostramos en el video.

Comandos: `echo "XX00-AB12" > codigo_sprint2.txt`, `cat codigo_sprint2.txt`, `date`.

## Video del sprint 
Pantalla continua y sin cortes. Cada integrante muestra su parte, dice su nombre y qué hizo en los primeros 10 segundos, y aparece su cara

[Enlace del video de YouTube aquí]

## Lo que hizo cada integrante en este sprint

| Integrante | Qué hizo | Commits |
| :--- | :--- | :--- |
| Katherin | Creó las páginas del sitio, la plantilla y revisó la ficha | 1 |
| Daniel | [Qué hizo] | [Número] |
| Dylan | [Qué hizo] | [Número] |
| Samuel | [Qué hizo] | [Número] |


