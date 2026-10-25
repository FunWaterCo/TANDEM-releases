<div align="center">

# TANDEM

### *For Access Controller*

Usa tus [**PlayStation Access Controller**](https://www.playstation.com/es-mx/accessories/access-controller/) en la PC como un mando de Xbox, o como teclado y ratón.

[![Última versión](https://img.shields.io/github/v/release/FunWaterCo/TANDEM-releases?label=%C3%BAltima%20versi%C3%B3n&color=1f6feb&style=for-the-badge)](../../releases/latest)
[![Windows 10 y 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0f766e?style=for-the-badge&logo=windows&logoColor=white)](#cómo-empezar)
[![Descargas](https://img.shields.io/github/downloads/FunWaterCo/TANDEM-releases/total?label=descargas&color=7c3aed&style=for-the-badge)](../../releases)

### [Descargar la última versión](../../releases/latest)

</div>

---

## ¿Qué es TANDEM?

TANDEM es un pequeño software que permite a tu PC identificar y remapear hasta **dos Access Controller** al mismo tiempo, conectados por USB, para que funcionen **juntos como un solo control**. 
Está pensado para personas con discapacidad motriz (daño medular, tetraplejia, etc)

TANDEM cuenta con 3 modos de uso predeterminados:
<table>
<tr>
<td width="33%" valign="top">

### Un solo mando
Tus dos controles se fusionan en **un mando de Xbox** que los juegos reconocen.

</td>
<td width="33%" valign="top">

### Uno por control
Cada Access es **su propio mando**: ideal para jugar dos personas.

</td>
<td width="33%" valign="top">

### Teclado y ratón
Tus botones y stick mandan **teclas, clics y cursor**: macros, atajos y mucho más.

</td>
</tr>
</table>

## Cómo empezar

**Necesitas:** Windows 10 u 11 (no he probado compatibilidad con Win8 o inferiores), tus Access Controller con **un cable USB de datos para cada uno** (asegurate de usar USB de datos y no de carga) e **internet la primera ejecución**.

1. **Descarga** [`TANDEM.zip`](../../releases/latest).
2. **Descomprímelo** donde quieras, por ejemplo en *Documentos*.
3. **Conecta** tus Access Controller por cable. (No he probado compatibilidad con Bluetooth).
4. Dale **doble clic a `INICIAR.bat`**.
5. Si tu PC no tiene Python, se descarga el **oficial** de python.org y lo instala **solo para TANDEM**.
6. Windows te pregunta **una sola vez** si permites realizar cambios como administrador: elige **Sí**. Así se instalan los dos controladores que hacen falta (ver sección de dependencias).
   Al terminar, TANDEM **se vuelve a abrir solo** y ya está listo.

Las siguientes veces abre en segundos, y el mando Xbox se enciende solo.

> **Si Windows dice «Windows protegió tu PC»:** elige **Más información → Ejecutar de todas formas**. Sale porque el programa es nuevo y Windows todavía no lo conoce.

> **Si Windows 11 lo bloquea** (*Control inteligente de aplicaciones*): desactiva el control inteligente de aplicaciones xd, en teoría ya NO debería saltar ese bloqueo pero con Windows uno nunca sabe.


<details>
<summary><b>Qué instala TANDEM en tu PC</b></summary>

| Qué | Para qué | Dónde |
|---|---|---|
| **Python 3.12** (oficial, de python.org) | TANDEM está programado en Python. Se descarga solo si tu PC no tenía uno; se instala solo para tu usuario | `%LOCALAPPDATA%\AccessXInput\python-oficial` |
| **ViGEmBus** (Nefarius) | Crea el mando de Xbox que ven los juegos | Controlador de Windows |
| **HidHide** (Nefarius) | Esconde los Access Controller de los juegos mientras TANDEM los usa, para que no lean el control dos veces | Controlador de Windows |
| **Tus ajustes** | Tu configuración de botones | `Documentos\PS5 ACCESS CONTROLLER SETTINGS` |
| **Copias de respaldo** | La versión anterior, por si una actualización sale mal | `%LOCALAPPDATA%\AccessXInput\respaldo` |

Los dos controladores se instalan con el permiso de Windows de la primera vez. Son los originales de Nefarius: TANDEM comprueba su huella digital antes de ejecutarlos. Solo si tú lo eliges, TANDEM crea un acceso directo y se abre al iniciar Windows.
</details>

<details>
<summary><b>Desinstalar TANDEM por completo</b></summary>

1. En TANDEM, abre **Ajustes** y en **Abrir con Windows** elige **No** (si lo tenías prendido).
2. **Cierra TANDEM del todo:** clic derecho en su icono junto al reloj (a veces dentro de la flechita ^) → **Salir de TANDEM**. Tus controles siguen escondidos de los demás programas hasta que desinstales HidHide (el paso siguiente).
3. En **Configuración → Aplicaciones → Aplicaciones instaladas** (en Windows 10: *Aplicaciones y características*), desinstala:
   - **HidHide**
   - **ViGEm Bus Driver** (puede aparecer como *Nefarius Virtual Gamepad Emulation Bus Driver*)
   - **Python 3.12.10 (64-bit)**, solo si lo instaló TANDEM y no lo usas para nada más

   Si usas HidHide o ViGEmBus con otro programa (DS4Windows, por ejemplo), no los desinstales.
4. **Reinicia** la PC.
5. Borra estas carpetas:
   - la carpeta donde descomprimiste TANDEM;
   - `%LOCALAPPDATA%\AccessXInput` (escríbelo tal cual en la barra del Explorador de archivos);
   - `Documentos\PS5 ACCESS CONTROLLER SETTINGS` (**ahí están tus configuraciones de botones**: guarda una copia de `mapeo.json` si las quieres conservar).
6. Borra los accesos directos **TANDEM** del Escritorio y del menú Inicio, si los creaste.
</details>

## Seguridad y privacidad

| | |
|---|---|
| **Actualizaciones firmadas** | TANDEM solo instala una versión nueva si trae la firma digital de quien la publica. |
| **Sin telemetría** | No manda tus datos a nadie. Solo pregunta aquí si hay una versión nueva (y lo puedes apagar). |
| **Instaladores verificados** | Los controladores que necesita (ViGEmBus y HidHide) solo se ejecutan si son *exactamente* los originales. |
| **Todo es opcional** | Acceso directo, abrir con Windows, segundo plano y permisos de administrador: nada pasa sin que tú lo pidas. |

## Preguntas frecuentes

<details>
<summary><b>¿Para quien está hecho TANDEM?</b></summary>

Francamente, para mi hermano, quien tiene lesión medular.
El ya contaba con dos Access Controller con los que juega en la Play, pero usar la PC con periféricos convencionales le es muy difícil, y las alternativas que hemos visto de periféricos para personas con lesión medular o motricidad limitada son bastante caros y difíciles de conseguir si no vives en EEUU.
Por otra parte, me sorprende que SONY no haya creado ya algún controlador oficial que garantice la compatibilidad de los Access Controller en PC, no solo por el hecho de tener algo con que jugar sino por todo el **POTENCIAL** que tienen estos aparatos para el uso real y productivo en computadoras, y que allá afuera hay MUCHAS personas con discapacidad motriz que tienen que solucionarse la vida con programas y controladores no oficiales.
Además, a pesar que en PC ya existen soluciones como reWASD y JoyToKey, el motivo por el cual nos decidimos por crear TANDEM fue simplemente porque queríamos una solución bastante más sencilla y personal. Ahora queremos compartirlo con el mundo, como una opción más para facilitar el uso de estos cachivaches en PC.
</details>


<details>
<summary><b>¿Qué controles funcionan?</b></summary>

Los **PlayStation Access Controller**, conectados **por USB**. Puedes usar uno o dos. No he probado a conectar más de dos Access Controller pero si consigo otro les haré saber, por si a alguien se le hiciera útil tener más de dos.
De momento solo he probado con los mandos conectados por USB, no he podido revisar si funcionan igual por bluetooth.
Y bueno, TECNICAMENTE cualquier mando DINPUT es compatible con TANDEM, la cosa es que toda la interfaz y funcionamiento están diseñados **ESPECÍFICAMENTE** con los Access Controller en mente.
</details>

<details>
<summary><b>¿Compatibilidad con Linux / MacOS?</b></summary>

Sí estoy en planes de lanzar una build para linux pronto, sin embargo la quiero testear bien, y de momento preferí darle prioridad a la versión de Windows porque es lo que usa mi hermano.
Respecto a MacOS, lo veo complicado, NO tengo una Mac y tampoco tengo a alguien que me preste una.
</details>

<details>
<summary><b>¿Compatibilidad con los puertos externos? (E1 - E4) </b></summary>

No he podido probarlo. No cuento con periféricos que pueda conectar a los puertos externos y por lo que he visto son algo caros. Estoy pensando fabricarme unos, al menos para verificar el funcionamiento con botones y sticks, y espero tambien poder conseguir un trigger para poder garantizar que los 3 tipos de input funcionen a la perfección. Atentos a las próximas actualizaciones.
</details>

<details>
<summary><b>¿Necesito instalar algo antes?</b></summary>

No. `INICIAR.bat` consigue todo lo que falta (Python y los dos controladores) la primera vez que lo ejecutas.
</details>

<details>
<summary><b>El teclado en pantalla de Windows no responde con TANDEM</b></summary>

Windows no deja que un programa normal le mande teclas a ventanas «de administrador». En TANDEM toca **Reiniciar como administrador** (aparece en el aviso amarillo, en *Ajustes* y en el menú del icono) y acepta el permiso de Windows.
</details>

<details>
<summary><b>¿Cómo se actualiza?</b></summary>

TANDEM te avisa solo y te cuenta qué cambia. Si prefieres hacerlo a mano, descarga el `TANDEM.zip` nuevo y úsalo en otra carpeta: tu configuración vive en *Documentos* y no se pierde.
</details>

<details>
<summary><b>NO FUNCIONA EN VALORANT</b></summary>

:/
Limitaciones del Vanguard Anticheat para protegerse de programas que remapean inputs. No quise indagar más al respecto para ver si podíamos forzarlo a funcionar por miedo a que nos baneen la cuenta, así que de momento no creo que sea posible utilizarlo en juegos que usen Vanguard. 
</details>

<details>
<summary><b>¿TANDEM tiene algún costo?  ¿Aceptan donativos?</b></summary>

TANDEM como tal ES TOTALMENTE GRATIS, creemos que los Access Controller ya son lo suficientemente caros como para encima COBRAR por un software que básicamente solo remapea los inputs a algo que una PC pueda reconocer.
Pero si nos quieren apoyar de alguna manera, pueden hacerlo a través de nuestro [GoFundMe](https://www.gofundme.com/f/ayudame-a-reconstruir-mi-vida-despues-de-un-accidente)
Si en algún momento abrimos más canales de comunicación y donativos lo haré de conocimiento aquí.
Atentos también a nuesto otro proyecto, [TRENDIT LABS](https://www.instagram.com/trenditlab/), más información pronto.
</details>

---

<div align="center">

**TANDEM - For Access Controller**

<sub>Proyecto independiente: no está afiliado ni respaldado por Sony ni por Microsoft. «PlayStation» y «PS5» son marcas de Sony Interactive Entertainment; «Xbox» y «Windows» son marcas de Microsoft. Se mencionan solo para indicar con qué funciona.</sub>

</div>
