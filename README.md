# Mario Tennis (Nintendo 64) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/nintendo-64/mario-tennis-64)**.

Traducción al **español de España** de *Mario Tennis* (Nintendo 64, 2000), el juego
de tenis de Camelot y Nintendo con Mario, Luigi, Peach, Bowser, Waluigi y compañía,
que nunca salió en castellano.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia
copia de la versión **USA** para aplicarlo.

## Estado

Versión **[v1.0](../../releases/tag/v1.0)**: primera versión publicada.

| Parte | Estado |
|---|---|
| Ayudas de Toad, avisos, reglas y mensajes | **Completos**: 258 mensajes |
| Rótulos de los menús | **Completos**: 142 rótulos |
| Créditos | Cargos traducidos; los nombres de personas y empresas no cambian |
| Texto dentro de imágenes | **139 imágenes rehechas**: títulos de pantalla, llamadas del partido (FALTA, DOBLE FALTA, IGUALES, Vent., BOLA DE SET…), nombres y datos de las pistas, tipos de jugador, dificultad, menú de pausa, marcadores, resultados, guardado y créditos |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿** en las dos fuentes del juego |
| Revisión durante una partida | Parcial (ver abajo) |

Se ha traducido **desde el inglés de la versión USA**, no del japonés, con una biblia
de términos fija. Los nombres de los personajes son los oficiales de Nintendo España
(Bebé Mario, Planta Piraña, Shy Guy…) y los términos de tenis son los habituales en
España: saque, resto, volea, globo, dejada, remate, iguales, ventaja, falta, tie-break.
La terminología está alineada con la traducción de
[Mario Tennis de Game Boy Color](https://github.com/johanderohan/mario-tennis-traduccion-es).

Las letras españolas se han añadido a las dos fuentes del juego con el mismo dibujo,
color y contorno que el resto. Los rótulos dibujados como imagen se han rehecho con
las propias letras del juego; solo se han dibujado a mano las que faltaban (Ñ, tildes,
¡, ¿, J…).

### Qué se ha dejado como en el original

- El logotipo **MARIO TENNIS**, la cinta inferior de los menús y el copyright.
- Palabras que en España se usan igual: **Ring Shot** (nombre del modo), **GAME OVER**,
  **REPLAY**, **LET**, **SET/SETS**, **START**, **Tie-break**, y los indicadores 1P/2C.
- Los **logotipos de las copas** del torneo (Mushroom Cup…), con letras en arco sobre la
  pelota. El nombre de cada copa sí sale en castellano en las listas y en las ayudas.
- Los iconos redondos con letras curvas (5/7 POINTS, SINGLES/DOUBLES, las iniciales
  de los tipos de Ring Shot, MENU/EXIT/CANCEL) y algunas imágenes pequeñas:
  **DIFFICULTY** en la selección de personaje (queda casi oculto por el panel), **REST**
  en la placa de Ring Shot por bolas, la plaquita «Code Entry» y la etiqueta NEW.
- Los nombres de los torneos por código, que eran promociones de revistas de EE. UU.

Algunos rótulos van condensados para caber en su sitio: «CAMBIO / CAMPO» (el juego
coloca las letras en dos filas de 6 y 5), «RESTOS GANAD.», «Estér.», «Ptdo.»…

### Comprobaciones y limitaciones

Todo se ha probado en emulador (parallel-n64 con el renderizador angrylion).

- **Jugado desde partida nueva** con la ROM publicada y las candidatas anteriores:
  menús, opciones, récords, selección de jugador, dificultad y pista, partidos de
  Exhibición completos con faltas, juegos, cambio de campo y resultados, el menú de
  pausa, guardar y continuar la partida tras reiniciar, Torneo (primer partido),
  Ring Shot en sus cuatro tipos, Desafío Piraña, Escenario Bowser con objetos y los
  juegos especiales.
- **Vistas con pruebas dirigidas** (forzando la memoria o la escena): los créditos,
  las pantallas del Transfer Pak con sus avisos, los mensajes con nombres y cifras
  insertados, y las llamadas IGUALES, Vent., TIE BREAK, BOLA DE JUEGO/SET/PARTIDO.
- **No se ha visto en el juego**: la final del último torneo (BOLA DE CAMPEONATO), los
  resultados con estrellas de Ring Shot (¡SUPERADO!, ¡PERFECTO!), los modos de 2 a 4
  jugadores ni el Transfer Pak con personajes reales de Game Boy. Sus textos e
  imágenes están traducidos y medidos, pero solo se han comprobado fuera del juego.
- **No se ha probado en consola real, flashcart ni otros emuladores.**
- La traducción y las revisiones se han hecho con ayuda de modelos de IA. No ha
  habido una revisión humana independiente.

Si encuentras un error, abre una incidencia indicando la pantalla y, si puedes,
una captura.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **USA**, en formato **.z64** (big-endian).
   Si tienes un `.n64` o un `.v64`, conviértelo antes a `.z64` (por ejemplo con Tool64).
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Mario Tennis (USA).z64` |
   | Tamaño | 16.777.216 bytes (16 MB) |
   | MD5 | `759358fad1ed5ae31dcb2001a07f2fe5` |

   ```bash
   md5sum "Mario Tennis (USA).z64"     # Linux
   md5 "Mario Tennis (USA).z64"        # macOS
   CertUtil -hashfile "Mario Tennis (USA).z64" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Mario Tennis (USA).z64" Mario.Tennis.N64.ES.v1.0.xdelta "Mario Tennis (ES).z64"`
5. Comprueba que la ROM resultante tiene **32 MB** (33.554.432 bytes) y MD5
   **`37c6fa4f2936b8bd4f469a5c07894fb2`**. Crece porque los textos e imágenes nuevos
   se guardan en una zona ampliada.
6. Cárgala en tu emulador o flashcard.

### Guardado

El juego guarda en **EEPROM de 16 Kbit**. La ROM traducida conserva la suma de
comprobación de la cabecera original, así que los emuladores que reconocen el juego
por ella (mupen64plus, RetroArch, Project64) le aplican la misma configuración que al
original. Además lleva la **cabecera avanzada de homebrew** (identificador «ED»,
EEPROM 16K) para ares, simple64 y EverDrive.

Si tu emulador no guarda la partida o el juego se queda en negro, cambia a mano el
tipo de guardado a **EEPROM 16K (16 Kbit)**.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin
relación alguna con Nintendo ni Camelot. Aquí no se distribuye el juego ni ninguna
parte de él: solo un parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia
y lo hago.
