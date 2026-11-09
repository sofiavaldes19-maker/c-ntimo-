# Céntimo

Juego de cartas de finanzas personales al estilo UNO, hecho a partir de la *Ficha de Diseño del Prototipo* del equipo FinTeam.

## Instalar como app

Céntimo es una app web instalable (PWA): una vez publicada en internet (por ejemplo con GitHub Pages), se instala desde el navegador, aparece con su ícono en la pantalla de inicio, se abre a pantalla completa y funciona sin internet.

- **iPhone / iPad (Safari):** botón Compartir → *Agregar a inicio*.
- **Android (Chrome):** menú ⋮ → *Instalar app*.
- **Computador (Chrome / Edge):** ícono de instalar en la barra de direcciones.

También hay un botón **Instalar app** en la pantalla de inicio del juego.

## Cómo jugar

### Cada jugador en su celular (en línea)

1. Una persona abre Céntimo y toca **Crear sala**. Su celular será el anfitrión: debe mantener Céntimo abierto mientras juegan.
2. Aparece un código de 4 letras, un QR y un link. Los demás escanean el QR, abren el link o tocan **Unirme a una sala** y escriben el código.
3. Cuando estén todos (de 2 a 10), el anfitrión toca **Empezar**. Si son pocos, puede agregar jugadores de la compu.

Cada uno ve solo sus propias cartas. Si alguien pierde la conexión, la compu juega sus turnos hasta que vuelva; al abrir de nuevo el link, vuelve solo a su sala.

La conexión es directa entre los celulares (PeerJS, incluido en `lib/`), así que no hace falta ningún servidor propio. Necesita internet y que el juego esté publicado en una dirección `https://` (por ejemplo, GitHub Pages).

### Un solo dispositivo

Toca **Un solo dispositivo**, elige cuántos juegan y si cada uno es **Persona** o **Compu**. Las personas se pasan el celular por turnos; antes de cada turno aparece "Pasa el dispositivo a…" para que nadie vea cartas ajenas. Este modo funciona sin internet.

Las cartas que puedes jugar aparecen resaltadas en dorado. Si no puedes jugar ninguna, toca el mazo o **Robar carta y pasar**.

## Reglas (según la ficha)

1. **Combina**: juega una carta del mismo color (categoría) o mismo número (monto). Si no puedes, robas una y pasas.
2. **Necesidades primero**: si juegas un Gusto (rojo) teniendo una Necesidad (azul) jugable, robas 2 de castigo. El juego te avisa antes.
3. **Escudo de ahorro**: al jugar una carta verde quedas protegido del próximo Imprevisto o Deuda.
4. **Especiales**: Imprevisto (+2 y pierde turno), Congelar cuenta (salta turno), Cambio de plan (reversa), comodín Sueldo extra (elige color) y comodín Deuda (+4, elige color).
5. **¡Último gasto!**: toca el botón cuando te queden 2 cartas, antes de jugar la penúltima. Si lo olvidas, el siguiente jugador puede acusarte y robas 2.

Al terminar, los demás suman los puntos de su mano: cada carta vale su número, las rojas el doble, las especiales 10 y los comodines 15. 0 = presupuesto cerrado, 1–25 = vas justo, 26 o más = en rojo. Los puntos se acumulan si juegan varias rondas.

## Más de 5 jugadores

La ficha original es para 2 a 4 jugadores con un mazo de 56 cartas. Para que jueguen hasta 10, con 6 o más jugadores el juego usa automáticamente dos mazos (112 cartas). Cuando el mazo se acaba, se baraja la pila de descarte.
