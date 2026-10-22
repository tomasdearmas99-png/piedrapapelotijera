# Manual de Usuario — Piedra, Papel o Tijera v1.0.0

**LPR 2026 · Actividad 7 · E.E.S.T. N° 100 "Toy Story"**

## 1. ¿Qué es este programa?

Es un juego de consola donde jugás Piedra, Papel o Tijera contra la computadora (la "IA").
Cada partida que juegues queda **guardada en un archivo de texto**, así que el historial sigue
ahí aunque cierres el programa y lo vuelvas a abrir.

## 2. Requisitos

- Windows 10 u 11.
- Compilador `g++` instalado (MinGW / MSYS2) y Visual Studio Code con PowerShell.

## 3. Cómo iniciar el juego

Abrí la terminal de PowerShell en la **carpeta raíz del proyecto** (`piedrapapelotijera`) y ejecutá:

```
g++ -std=c++11 src/main.cpp -o src/piedrapapelotijera.exe
.\src\piedrapapelotijera.exe
```

> ⚠️ Es importante ejecutarlo desde la carpeta raíz. Si lo abrís desde otra carpeta, el programa
> no va a encontrar la ruta `src/historial_partidas.txt`.

## 4. Menú principal

| Opción | Acción |
|--------|--------|
| 1 | Jugar una partida contra la IA |
| 2 | Ver el historial de partidas guardadas en disco |
| 3 | Salir del programa |

Escribí el número de la opción y presioná **Enter**.

## 5. Jugar una partida (Opción 1)

1. Ingresá tu nombre o nickname y presioná Enter.
2. Elegí tu jugada: **1** Piedra, **2** Papel, **3** Tijera.
3. El programa muestra qué eligió cada uno y el resultado: **Victoria**, **Derrota** o **Empate**.
4. La partida se guarda automáticamente en el disco. Verás el mensaje `[DISCO] Partida resguardada con exito`.

### Reglas

- Piedra le gana a Tijera.
- Papel le gana a Piedra.
- Tijera le gana a Papel.
- Si ambos eligen lo mismo, es empate.

## 6. Ver el historial (Opción 2)

Muestra todas las partidas guardadas, con este formato:

```
Partida #1 | Jugador: Ana | Piedra vs Papel | Resultado: Derrota
```

Al final se indica el total de registros leídos. Si todavía no jugaste ninguna partida, aparece
el aviso `Aun no existen partidas guardadas en disco`.

## 7. Salir (Opción 3)

Cierra el programa. No hace falta "guardar": cada partida ya fue guardada al terminar.

## 8. Preguntas frecuentes

**Cerré la ventana, ¿perdí mis partidas?**
No. Se guardan en `src/historial_partidas.txt`, que es un archivo en el disco.

**¿Dónde está el archivo del historial?**
En la carpeta `src/`. Se crea solo la primera vez que jugás una partida.

**Se me saltea la pregunta del nombre.**
Es un problema del código (falta `cin.ignore()`); consultá el Manual del Programador.

**Ingresé una opción inválida.**
El programa muestra `[ERROR] Opcion invalida` y vuelve a mostrar el menú.

**Quiero borrar el historial.**
Cerrá el programa y borrá el archivo `src/historial_partidas.txt`.
