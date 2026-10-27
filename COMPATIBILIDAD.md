# Juegos y problemas conocidos

Lo que ya sabemos de juegos concretos y de problemas que ya nos tocó ver, con la forma de resolverlos. Esta página se va poniendo al día: TANDEM la abre desde **Ajustes → Juegos y problemas conocidos** y desde el menú de su icono, junto al reloj.

*[English version](COMPATIBILITY.md)*

## Juegos

| Juego | ¿Funciona? | En corto |
|---|---|---|
| [FiveM y GTA V (Legacy)](#fivem-y-gta-v-legacy) | Sí, con dos ajustes del juego | Pantalla completa exclusiva y ratón en «DirectInput» |
| [No More Heroes](#no-more-heroes) | Sí | La primera vez, cierra el juego y vuelve a abrirlo |
| [Valorant](#valorant) | No | Su antitrampas bloquea lo que manda TANDEM |

### FiveM y GTA V (Legacy)

**Con «Teclado y ratón» de TANDEM.** Si el juego no tiene los ajustes de abajo, el cursor se va a la esquina de arriba a la izquierda, aparece un segundo cursor y la cámara se desacomoda sola, sobre todo cuando salen avisos de FiveM.

**Qué hacer** (dentro del juego: el launcher de FiveM no tiene estos ajustes):

1. Abre el juego y, en los ajustes de **gráficos avanzados**, pon la pantalla en **pantalla completa exclusiva** (no en ventana ni en ventana sin bordes).
2. En los ajustes del ratón, pon **«Método de entrada del ratón»** en **«DirectInput»**.

Con esos dos ajustes el ratón y la cámara funcionan normal. Con «Windows» parece que funciona, pero la cámara sigue brincando de vez en cuando.

### No More Heroes

La primera vez que abres el juego después de instalar TANDEM, puede que no responda al mando aunque TANDEM diga que está encendido.

**Qué hacer:** cierra el juego y vuelve a abrirlo, con TANDEM abierto. Solo pasa esa primera vez: el juego alcanzó a ver tus Access Controller antes de que TANDEM terminara de esconderlos.

**Consejo para cualquier juego:** abre TANDEM y enciende el mando Xbox **antes** de abrir el juego. Muchos juegos solo buscan mandos al arrancar.

### Valorant

**No funciona.** Su antitrampas (Vanguard) bloquea a propósito las teclas y el ratón que manda cualquier programa, y TANDEM te avisa cuando Valorant está al frente. Lo único que lo lograría es un controlador propio y firmado (como el que usan programas de pago como reWASD), pero eso cuesta dinero que no podemos cubrir y no podemos garantizar que funcione. No intentes forzarlo: podrías arriesgar tu cuenta.

## Problemas conocidos

| Qué pasa | Qué hacer |
|---|---|
| El teclado en pantalla de Windows (u otra ventana «de administrador») no responde | En TANDEM, toca **Reiniciar como administrador** (en el aviso amarillo, en Ajustes o en el menú del icono) y acepta el permiso de Windows. |
| Windows dice «Windows protegió tu PC» al abrir TANDEM | Elige **Más información → Ejecutar de todas formas**. Sale porque el programa es nuevo y Windows todavía no lo conoce. |
| El juego no responde, o tu mando es el jugador 2 o más | TANDEM te dice qué mando tiene el lugar del jugador 1. Desconecta ese mando unos segundos (o toca **Pasar a jugador 1**) y, si el juego ya estaba abierto, ciérralo y vuelve a abrirlo. |
| TANDEM no encuentra tus Access Controller | Cierra Steam, DS4Windows u otro programa que los pueda estar usando, y revisa que el cable USB sea de datos (no solo de carga). |
| TANDEM dice que un juego todavía podría ver tu Access directamente | Desconecta ese control y vuelve a conectarlo una vez. |

## Sin probar todavía

- Conexión por **Bluetooth** (solo lo hemos probado por USB).
- Lo que se conecta a los puertos de expansión **E1 a E4**.
- Más de dos Access Controller a la vez.
- Windows 8 o anterior.

## ¿Un juego no funciona bien?

Cuéntanos en la pestaña [**Issues**](../../issues) de este repositorio: qué juego es, qué modo de TANDEM usas («Un solo mando», «Uno por control» o «Teclado y ratón») y qué pasa. Si lo resolvemos, lo agregamos aquí.
