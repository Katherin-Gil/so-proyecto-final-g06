## Qué se pide en este sprint (DYLAN)

Instalar las herramientas básicas en la consola: `make`, `rsync`, `curl`, `git` y `wget`.

### 1. Actualizar la lista de paquetes

```bash
sudo apt update
```

Actualiza el índice de paquetes disponibles para que `apt` instale las versiones más recientes. Se ejecuta antes de instalar cualquier cosa.

![sudo apt update](img/Dylan-Caps-SO-Sprint1_Install/sudo%20apt%20update.png)

### 2. Instalar git

```bash
sudo apt install -y git
```

Instala Git, el sistema de control de versiones que usamos para trabajar en equipo y subir el proyecto a GitHub.

![instalar git](img/Dylan-Caps-SO-Sprint1_Install/supo%20apt%20install%20-y%20git%20.png)

### 3. Instalar make y rsync

```bash
sudo apt install -y make rsync
```

- **make**: automatiza la compilación y tareas del proyecto leyendo un archivo `Makefile`.
- **rsync**: copia y sincroniza archivos entre carpetas o equipos, transfiriendo solo lo que cambió.

![instalar make y rsync](img/Dylan-Caps-SO-Sprint1_Install/supo%20apt%20install%20-y%20make%20y%20rsync.png)

**make** (CAP individual):

![instalar make](img/Dylan-Caps-SO-Sprint1_Install/sudo%20apt%20install%20-y%20make.png)

**rsync** (CAP individual):

![instalar rsync](img/Dylan-Caps-SO-Sprint1_Install/sudo%20apt%20install%20-y%20rsync.png)

### 4. Instalar wget

```bash
sudo apt install -y wget
```

Descarga archivos desde internet directamente desde la terminal.

![instalar wget](img/Dylan-Caps-SO-Sprint1_Install/sudo%20apt%20install%20-y%20wget.png)

### 5. Instalar curl

```bash
sudo apt install -y curl
```

Transfiere datos desde o hacia un servidor usando URLs. Sirve para descargar archivos y probar APIs.

![instalar curl](img/Dylan-Caps-SO-Sprint1_Install/sudo%20apt%20install%20-y%20curl.png)



## VISUALIZACION DE VERSION Y FECHA. (CONFIRMACION DE INSTALACION)

Después de instalar cada herramienta, se verifica que quedó funcionando mostrando su versión (`--version`) y la fecha del sistema (`date`) como evidencia.

### 1. git

```bash
git --version && date
date
```

Muestra la versión de Git instalada y la fecha actual del sistema.

![git version y date](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/git%20date%20y%20version.png)

### 2. wget

```bash
wget --version && date
date
```

Confirma que `wget` está instalado y muestra su versión.

![wget version y date](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/wget%20date%20y%20version.png)

**git y wget** (captura conjunta):

![git y wget version y date](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/git%20y%20wget%20version%20y%20date.png)

### 3. make

```bash
make --version && date
date
```

Confirma que `make` está instalado y muestra su versión.

![make version y date](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/Make%20date%20y%20version.png)

### 4. rsync

```bash
rsync --version && date
date
```

Confirma que `rsync` está instalado y muestra su versión.

![rsync version y date](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/rsync%20date%20y%20version.png)

### 5. curl

```bash
curl --version && date
```

Confirma que `curl` está instalado y muestra su versión.

![curl version y date](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/curl%20date%20y%20version.png)

### 6. Confirmación general

Captura conjunta de make, rsync y curl con la fecha, como confirmación final de que todas las herramientas quedaron instaladas.

![make, rsync, curl, date y confirmacion](img/Dylan-Caps-SO-Sprint1_Vesion%3ADate/Make%2C%20rsync%20curl%20Date%20y%20confirmacion.png)



