# Cómo instalar Quarto y ver la presentación

Esta guía explica, paso a paso, cómo instalar **Quarto** en **Windows** y en **Mac**, y cómo abrir la presentación (`.qmd`) para verla en el navegador.

No hace falta saber programar. Solo copiar y pegar algunos comandos.

---

## ¿Qué es Quarto y por qué lo necesitamos?

**Quarto** es una herramienta gratuita que convierte un archivo de texto (`.qmd`) en una presentación de diapositivas que se abre en el navegador (formato HTML).

El flujo es sencillo:

```
archivo.qmd  ──►  Quarto  ──►  presentación.html
```

Solo se instala **una vez** y después basta con un comando para generar la presentación.

---

## Windows

### Opción A — Instalador (la más fácil)

1. Entra a la página oficial: <https://quarto.org/docs/get-started/>
2. Haz clic en el botón azul **Download Quarto CLI**.
3. Abre el archivo descargado (`.exe`).
4. Sigue el asistente de instalación haciendo clic en **Next** hasta terminar. Deja todas las opciones por defecto.
5. Cierra el asistente al finalizar.

### Opción B — Con un comando (para usuarios técnicos)

Abre **PowerShell** o el **Símbolo del sistema** y escribe:

```powershell
winget install Posit.Quarto
```

### Comprobar que quedó instalado

Abre **PowerShell** o el **Símbolo del sistema** y escribe:

```powershell
quarto --version
```

Si aparece un número de versión (por ejemplo `1.5.57`), ¡todo está listo!

---

## Mac

### Opción A — Instalador (la más fácil)

1. Entra a la página oficial: <https://quarto.org/docs/get-started/>
2. Haz clic en el botón azul **Download Quarto CLI** (descargará un archivo `.pkg`).
3. Ve a la carpeta de **Descargas** y haz doble clic en el archivo `.pkg`.
4. Sigue las instrucciones del asistente y haz clic en **Close** al terminar.

### Opción B — Con Homebrew (para usuarios técnicos)

Si ya tienes [Homebrew](https://brew.sh) instalado, abre la app **Terminal** y escribe:

```bash
brew install --cask quarto
```

### Comprobar que quedó instalado

Abre la app **Terminal** (búscala con Spotlight: `Cmd + Espacio` y escribe "Terminal") y escribe:

```bash
quarto --version
```

Si aparece un número de versión, ¡todo está listo!

---

## Ver la presentación

Una vez instalado Quarto, sigue estos pasos (igual en Windows y en Mac):

1. Coloca el archivo de la presentación (`github-workshop-simple.qmd`) en una carpeta fácil de encontrar, por ejemplo el **Escritorio**.

2. Abre la terminal:
   - **Windows:** PowerShell o Símbolo del sistema.
   - **Mac:** la app Terminal.

3. Ubícate en la carpeta donde está el archivo. Por ejemplo, si está en el Escritorio:

   ```bash
   cd Desktop
   ```

4. Genera la presentación:

   ```bash
   quarto render github-workshop-simple.qmd
   ```

   Esto creará un archivo `github-workshop-simple.html` en la misma carpeta. Ábrelo con doble clic y se verá en el navegador.

### Alternativa: vista previa en vivo

Si prefieres que la presentación se actualice sola cada vez que se edita el archivo, usa:

```bash
quarto preview github-workshop-simple.qmd
```

Se abrirá automáticamente en el navegador. Para detenerla, presiona `Ctrl + C` en la terminal.

---

## Moverse dentro de la presentación

- **Flechas del teclado** (← →) o clic para avanzar y retroceder.
- Tecla **F** para pantalla completa.
- Tecla **Esc** para ver todas las diapositivas en miniatura.
- Tecla **S** para abrir la vista del ponente (notas y temporizador).

---

## Preguntas frecuentes

**¿Necesito instalar algo más?**
No para esta presentación. Quarto por sí solo genera el HTML. (Solo se necesitarían herramientas extra si se quisiera exportar a PDF, que no es el caso aquí.)

**¿Puedo compartir la presentación con alguien que no tenga Quarto?**
Sí. Una vez generado el archivo `.html`, se puede enviar por correo o subir a un servidor y se abre en cualquier navegador, sin instalar nada.

**¿Dónde consulto la documentación oficial?**
En <https://quarto.org/docs/get-started/> encontrarás guías para Windows, Mac y Linux.

---

*Cualquier duda con la instalación, con gusto la resolvemos juntos.*
