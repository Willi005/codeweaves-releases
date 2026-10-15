# CodeWeaves Studio — versiones

**CodeWeaves Studio** es una app de escritorio para diseñar interfaces junto a agentes de IA. Cada diseño es un frame del lienzo guardado como un archivo HTML legible (`design.cw.html`), y tiene su propio agente: **Claude Code, Codex, OpenCode o Antigravity**. Lo que cambias en el lienzo y lo que escribe el agente se ve al instante, en los dos sentidos.

Este repositorio solo publica los paquetes; el código no está aquí.

**Versión actual: [0.2.0-beta.6](https://github.com/Willi005/codeweaves-releases/releases/tag/v0.2.0-beta.6)** (15-10-2026), para Linux x86_64 y Windows 11 x64.

## Qué puedes hacer

- **Diseñar con agentes:** describe lo que quieres y elige 1, 2 o 3 direcciones en paralelo, cada una con su agente, modelo y nivel de esfuerzo. El agente puede preguntarte antes de empezar, leer otros frames que nombres en el pedido y usar las imágenes que adjuntes.
- **Editar a mano en vivo:** seleccionar, mover y redimensionar, texto y estilos en el inspector (Simple, Pro, Code y Tweaks), capas, dibujo, deshacer y rehacer. Cada cambio se guarda solo y cada diseño tiene su historial de versiones.
- **Aplicaciones de varias pantallas:** un diseño puede declarar sus vistas (inicio, precios, contacto…) y el lienzo muestra un frame por vista sobre el mismo documento.
- **Tus propios archivos:** el panel **Assets** sube imágenes, GIF y vídeos al diseño y los inserta, renombra o borra. El agente sabe cuáles hay y los usa.
- **Comentar y presentar:** comentarios anclados a elementos y **Present** a pantalla completa, interactivo y en vivo.
- **Exportar e importar:** HTML legible con su runtime, que se abre en cualquier navegador; ZIP con el diseño, el runtime y los assets; PNG y JPEG. **Import** vuelve a abrir esos HTML y ZIP, y también los `.dc.html` de Claude Design.
- **Llevar el diseño a tu código:** «Send to a coding agent…» copia un prompt para que Claude Code, Codex, Gemini CLI u OpenCode lean el diseño por **MCP** (solo lectura) y lo pasen a tu proyecto.
- **Settings:** apariencia y tema, proveedores y cuentas, permisos de los agentes, personajes, skills de diseño, servicios de imágenes, conexión MCP y actualizaciones.

## Instalar

Descarga la última versión desde [Releases](https://github.com/Willi005/codeweaves-releases/releases).

| Sistema | Archivo | Cómo |
| --- | --- | --- |
| Linux x86_64 | `CodeWeaves-Studio-<versión>-x86_64.AppImage` | `chmod +x` y ábrela; la primera vez crea su entrada en el menú de aplicaciones |
| Debian / Ubuntu | `codeweaves-studio_<versión>_amd64.deb` | `sudo apt install ./codeweaves-studio_<versión>_amd64.deb` (instala también git) |
| Windows 11 x64 | `CodeWeaves-Studio-<versión>-x64-Setup.exe` | Ejecútalo; se instala por usuario, sin permisos de administrador |

**Requisitos:**
- **git** (en Windows, [Git for Windows](https://git-scm.com/download/win)).
- Al menos un agente con su cuenta. La bienvenida y **Settings → Providers** detectan cuáles tienes y te ofrecen instalar los que falten con su instalador oficial (te enseñan el comando antes de ejecutarlo) e iniciar sesión. Los modelos de otros proveedores llegan a través de OpenCode.
- No hace falta Node.js, salvo para instalar OpenCode en Windows (va por npm).

**El instalador de Windows no está firmado**, así que Windows puede avisar de «editor desconocido». Para comprobar cualquier descarga, compara su suma con la de `SHA256SUMS.txt` de su release:
- Linux: `sha256sum <archivo>`.
- Windows (PowerShell): `Get-FileHash <archivo>`.

Al desinstalar en Windows, el desinstalador te pregunta aparte si borra la configuración y la caché y si borra la carpeta de proyectos. «No» es la respuesta por defecto en las dos.

## Actualizaciones

La app busca versiones nuevas en este repositorio al abrirse y cada seis horas, y avisa con las novedades. Solo descarga e instala cuando tú lo pides:
- **Update** descarga la versión.
- **Restart to update** la instala y vuelve a abrir la app.
- **Settings → Updates** busca en el momento.

La AppImage, el `.deb` y el instalador de Windows se actualizan desde la app. Hasta la 0.2.0-alpha.4 también se publicaba un `.tar.gz`, que no se actualiza solo; si aún tienes esa copia, instala una vez la AppImage o el `.deb`.

Cada release incluye los paquetes, los archivos `.yml` que lee la app (`beta*.yml`, `latest*.yml`) y `SHA256SUMS.txt`.

## Estado

CodeWeaves Studio está en **beta** (`0.2.0-beta.N`) y cada versión se publica como prerelease. Las novedades de cada una están en las notas de su [release](https://github.com/Willi005/codeweaves-releases/releases).

Límites conocidos:
- No hay versión para macOS ni para ARM.
- El instalador de Windows no está firmado.
- La página exportada solo se ha probado en navegadores Chromium.
- Los proyectos se guardan en `~/CodeWeavesProjects` (en Windows, `%USERPROFILE%\CodeWeavesProjects`) y cada uno tiene su propio repositorio git.
