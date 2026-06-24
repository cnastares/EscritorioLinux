# EscritorioLinux - Instalador Automatizado de Niri + DankMaterialShell (DMS)

Este proyecto está diseñado para usuarios que migran de Windows a Linux y desean una interfaz de alto rendimiento, moderna y visualmente atractiva en **Ubuntu 26.04 (Wayland)** sin tener que configurar nada desde la terminal.

El instalador empaqueta el compositor de ventanas **Niri** (un gestor de ventanas tipo mosaico horizontal infinito) y la suite de escritorio **DankMaterialShell** (que añade paneles, widgets, notificaciones y centro de control estilo *Material You*).

---

## ¿Qué hace este instalador?

Al instalar el paquete `.deb`, el sistema de manera automática en segundo plano:
1. Agrega los repositorios PPA oficiales de Niri (`ppa:avengemedia/danklinux`) y DMS (`ppa:avengemedia/dms`).
2. Descarga e instala Niri y DMS a través del gestor de paquetes de Ubuntu (`apt`).
3. Copia un perfil preconfigurado de atajos de teclado y comportamiento (`config.kdl`) directamente a la carpeta de configuración de Niri (`~/.config/niri/`) de todos los usuarios actuales y futuros en el sistema.
4. Genera una bitácora de progreso de la instalación en `/var/log/escritoriolinux-install.log`.

---

## Instrucciones de Instalación

Puedes instalar el paquete utilizando la terminal de la siguiente manera:

1. Abre una terminal en la carpeta donde descargaste el archivo `.deb`.
2. Ejecuta el comando de instalación:
   ```bash
   sudo apt install ./escritoriolinux_1.0.0_all.deb
   ```
3. La instalación se iniciará en segundo plano. Puedes monitorear el progreso leyendo el archivo de registro:
   ```bash
   tail -f /var/log/escritoriolinux-install.log
   ```

---

## Cómo Iniciar Sesión en tu Nuevo Escritorio

Una vez terminada la instalación:

1. Guarda tu trabajo y **cierra tu sesión actual** (Log Out).
2. En la pantalla de inicio de sesión de Ubuntu, haz clic en tu nombre de usuario.
3. Antes de introducir tu contraseña, busca el **icono del engranaje** en la esquina inferior derecha de la pantalla.
4. Haz clic en el engranaje y selecciona **"Niri"** en la lista.
5. Introduce tu contraseña e inicia sesión. ¡Bienvenido a tu nuevo escritorio!

*Nota: Si deseas volver a tu escritorio de Ubuntu clásico, simplemente vuelve a cerrar sesión, haz clic en el engranaje y selecciona "Ubuntu".*

---

## Guía de Atajos de Teclado (Keyboard Shortcuts)

Para facilitar la transición desde Windows, se han configurado los siguientes atajos de teclado principales:

### Aplicaciones y Búsqueda
*   **`Super + Enter`**: Abre la Terminal del sistema (`gnome-terminal`).
*   **`Super + Espacio`** o **`Super + D`**: Abre el buscador Spotlight y lanzador de aplicaciones (DMS).

### Gestión de Ventanas
*   **`Super + Q`**: Cierra la ventana activa actual.
*   **`Super + F`**: Maximiza la columna de la ventana seleccionada.
*   **`Super + Shift + F`**: Pone la ventana en pantalla completa.
*   **`Super + R`**: Alterna entre anchos de columna preestablecidos (1/3, 1/2 y 2/3 de pantalla).

### Navegación (Tiling horizontal)
*   **`Super + Flecha Izquierda / Derecha`** (o **`Super + H / L`**): Desplazarse por el tapiz horizontal de ventanas.
*   **`Super + Flecha Arriba / Abajo`** (o **`Super + K / J`**): Desplazarse de forma vertical (si hay ventanas apiladas).

### Mover Ventanas
*   **`Super + Ctrl + Flecha Izquierda / Derecha`** (o **`Super + Ctrl + H / L`**): Mueve la columna de la ventana hacia los lados.

### Áreas de Trabajo (Workspaces)
*   **`Super + [1 al 9]`**: Cambia al área de trabajo correspondiente.
*   **`Super + Shift + [1 al 9]`**: Envía la ventana seleccionada al área de trabajo correspondiente.

### Salir
*   **`Super + Shift + E`**: Cierra la sesión de Niri (vuelve a la pantalla de login).

---

## Personalización de Colores Dinámica (Material You)

La barra de estado, el centro de control y los menús de DankMaterialShell adaptan sus colores de forma dinámica según tu fondo de pantalla actual.
*   Para cambiar los colores del sistema, simplemente cambia tu imagen de fondo de pantalla habitual desde la terminal o el configurador, y el motor de temas (`matugen`) recalculará el espectro de colores automáticamente.
