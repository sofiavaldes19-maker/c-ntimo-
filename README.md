# Céntimo

Juego de cartas de finanzas personales al estilo UNO, hecho a partir de la *Ficha de Diseño del Prototipo* del equipo FinTeam.

## Instalar como app

Céntimo es una app web instalable (PWA): una vez publicada en internet (por ejemplo con GitHub Pages), se instala desde el navegador, aparece con su ícono en la pantalla de inicio, se abre a pantalla completa y funciona sin internet.

- **iPhone / iPad (Safari):** botón Compartir → *Agregar a inicio*.
- **Android (Chrome):** menú ⋮ → *Instalar app*.
- **Computador (Chrome / Edge):** ícono de instalar en la barra de direcciones.

También hay un botón **Instalar app** en la pantalla de inicio del juego.

## Cómo jugar

1. Abre `index.html` en cualquier navegador (celular o computador). No necesita instalación.
2. Elige cuántos juegan (**de 2 a 10**) y escribe sus nombres.
   - **Persona**: se pasan el mismo dispositivo por turnos. Antes de cada turno aparece una pantalla "Pasa el dispositivo a…" para que nadie vea cartas ajenas.
   - **Compu**: un jugador automático, útil si son pocos.
3. Toca **Empezar partida**.

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
