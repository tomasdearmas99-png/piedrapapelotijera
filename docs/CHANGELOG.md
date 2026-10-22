# CHANGELOG

Todos los cambios relevantes de este proyecto se documentan en este archivo.
Se sigue el versionado semántico (MAJOR.MINOR.PATCH).

## [1.0.0] - 2026-10-11

### Agregado
- Programa principal `src/main.cpp` con menú de tres opciones (jugar, ver historial, salir).
- Estructura `Partida` (ID, jugador, elección del jugador, elección de la IA, resultado).
- Persistencia en disco con `ofstream` en modo `ios::app` (`src/historial_partidas.txt`, formato CSV).
- Lectura del historial con `ifstream` y `getline` delimitado por comas.
- Estructura de repositorio: `.gitattributes`, `.gitignore`, `LICENSE`, `README.md`, `docs/`, `src/`, `capturas/`.
- Manual de Usuario y Manual del Programador (v1.0.0) en Markdown y PDF.

### Pendiente
- Capturas de evidencia (`capturas/`).
- Informe APA v7 en PDF (`docs/`).
