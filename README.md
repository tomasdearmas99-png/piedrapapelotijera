Piedra, Papel o Tijera + Persistencia en Disco

**Materia:** Laboratorio de Programación (LPR) — 5° Año
**Institución:** E.E.S.T. N° 100 "Toy Story" — Vicente López
**Actividad 7:** Mini juego contra la IA de la consola con registro de partidas en un archivo de texto.
**Versión:** 1.0.0 · **Grupo:** G03 · **Ciclo lectivo:** 2026

Integrantes

| Apellido y Nombre | Rol                                                                                             |
|Sofia Mojica       | Lógica del juego: menú, jugada de la IA y reglas de victoria, derrota y empate                  |
|Gabriel Zacarias   | Persistencia en disco: struct Partida, escritura con ofstream (ios::app) y lectura con ifstream |
|Mateo Roberts      |Documentación: manuales de usuario y del programador, informe APA v7 y cuestionario técnico      |
|Leonel De Armas    | Control de versiones (GitHub), pruebas de compilación y capturas de evidencia                   |


Descripción

El programa permite jugar Piedra, Papel o Tijera contra la computadora. Cada partida se guarda en una
estructura (`struct Partida`) y se persiste en `src/historial_partidas.txt` (formato CSV) usando `ofstream`
con el modo `ios::app`. El historial completo se recupera del disco con `ifstream` desde la Opción 2 del menú.

Estructura del repositorio

```
piedrapapelotijera/
├── .gitattributes
├── .gitignore
├── LICENSE
├── README.md
├── docs/
│   ├── InformeEEST1_LPR2026_ACT07_G03_Informe_v1.0.0.pdf   (pendiente)
│   ├── CHANGELOG.md
│   └── manuales/
│       ├── manual_programador_v1.0.0.md / .pdf
│       └── manual_usuario_v1.0.0.md / .pdf
├── src/
│   ├── main.cpp
│   └── historial_partidas.txt   (se genera al jugar)
└── capturas/
    ├── jugada_consola.png        (pendiente)
    └── archivo_disco.png         (pendiente)
```

Compilación y ejecución (Windows 10/11 · PowerShell)

Ejecutar **siempre desde la raíz del repositorio** (el programa usa la ruta relativa `src/historial_partidas.txt`).

```powershell
# 1. Compilar con C++11
g++ -std=c++11 src/main.cpp -o src/piedrapapelotijera.exe

# 2. Ejecutar
.\src\piedrapapelotijera.exe
```

Documentación

- [Manual de Usuario](docs/manuales/manual_usuario_v1.0.0.md)
- [Manual del Programador](docs/manuales/manual_programador_v1.0.0.md)
- [Historial de versiones](docs/CHANGELOG.md)

Licencia

Distribuido bajo licencia MIT escolar. Ver [LICENSE](LICENSE).
