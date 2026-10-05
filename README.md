# CodeWeaves Studio — versiones

Aquí se publican las versiones de **CodeWeaves Studio**, un entorno de escritorio para diseñar en HTML con agentes de IA de distintos proveedores (Claude Code, Codex, Antigravity y OpenCode) en un mismo lienzo.

Este repositorio solo contiene los paquetes: el código no está aquí.

## Instalar (Linux x86_64)

Descarga la última versión desde [Releases](https://github.com/Willi005/codeweaves-releases/releases):

- **AppImage:** `chmod +x CodeWeaves-Studio-*-x86_64.AppImage` y ábrela.
- **Debian y Ubuntu:** `sudo apt install ./codeweaves-studio_*_amd64.deb`.
- **Otros:** descomprime el `.tar.gz` y abre `codeweaves-studio`.

Necesita **git**. La propia app instala y conecta los programas de los proveedores.

## Actualizaciones

Desde la 0.2.0-alpha.2, la app busca aquí las versiones nuevas y avisa cuando hay una. Con **Update** la descarga, y con **Restart to update** se instala y se vuelve a abrir. `latest-linux.yml` es el archivo que lee la app.

Las sumas SHA-256 de cada versión van en su `SHA256SUMS.txt`.
