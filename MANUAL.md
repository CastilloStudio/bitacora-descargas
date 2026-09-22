# Bitácora · guía de uso

Para Carmen. Va en el orden en que se hacen las cosas: primero instalar, luego
dejar la consulta configurada, y después el día a día.

No hace falta leerla entera de una vez. Las tres primeras secciones son de una
sola vez; a partir de «El día a día» está lo que se usa siempre.

---

## 1. Instalar

1. Descargar el instalador desde este enlace, que siempre apunta a la última
   versión:
   <https://github.com/CastilloStudio/bitacora-descargas/releases/latest/download/Bitacora-win-Setup.exe>
2. Ejecutarlo. Sale una ventanita de progreso y, al terminar, la aplicación se
   abre sola.

> Si el enlace no funcionara, abrir
> <https://github.com/CastilloStudio/bitacora-descargas/releases> y descargar
> **Bitacora-win-Setup.exe** de la versión de arriba. En esa lista hay más
> archivos (uno acabado en `.nupkg`, otro llamado `RELEASES`…); no hacen falta.

**Windows dirá que no reconoce el programa.** Aparece una pantalla azul,
«Windows protegió tu PC». Es lo normal en un programa sin firma de empresa, no
es un aviso de virus. Hay que pulsar **Más información** y luego **Ejecutar de
todas formas**.

No pregunta dónde instalar ni dónde guardar los datos: eso ya está decidido. El
programa se instala en la carpeta del usuario y los datos van a `Documentos\Bitacora`
(si Documentos estuviera sincronizado con OneDrive, van a una carpeta local del
equipo, para no corromper la base). La ruta exacta se ve luego en
**Administración**, debajo del título; conviene saberla para las [copias en
USB](#7-copias-de-seguridad-y-recuperación).

Después, la aplicación se actualiza sola. Cada vez que se abre comprueba si hay
versión nueva; cuando la hay, aparece un botón **Actualizar y reiniciar** al pie
de la barra de la izquierda, y al pulsarlo se reinicia ya actualizada.

Al volver a entrar, una ventana cuenta lo que ha cambiado en esa versión. Se cierra
al pulsar **Aceptar**, no antes: da tiempo a leerla entera. Sale una sola vez por
versión.

---

## 2. Crear la consulta (solo la primera vez)

Al abrirla por primera vez sale **«Vamos a preparar la consulta»**.

1. Elegir un **nombre de usuario** y una **contraseña**. Mínimo doce
   caracteres.
2. Repetirla y pulsar **Crear la consulta**.
3. Aparece una última pantalla, **«Conectar con Google»**. Se puede hacer ahora
   —hace falta el archivo `client_secret.json`, explicado en
   [Conectar Google](#35-conectar-google)— o pulsar
   **Ahora no** y dejarlo para más tarde. En los dos casos se entra a
   continuación en **Administración**.

**Sobre la contraseña, que esto importa de verdad.** Todo va cifrado con ella:
la base de datos y también las copias de seguridad. No se guarda en ninguna
parte, ni siquiera cifrada, así que **nadie puede recuperarla**: ni yo, ni
Google, ni reinstalando. Si se pierde la contraseña y no hay clave de
recuperación, los datos no se abren nunca más.

La clave de recuperación se genera en el paso siguiente y es el único seguro
que existe contra eso.

> Si ya hubiera una consulta en otro ordenador, aquí abajo están **Buscar en
> Drive…**, **Desde una carpeta…** y **Desde un archivo…**. Están explicados en
> la sección 7.

---

## 3. Dejar la consulta lista

Al entrar se aterriza en **Administración**, repartida en pestañas: *Consulta*,
*Tarifas*, *Mensajes al paciente*, *Cuestionarios*, *Seguridad y copias*,
*Conexiones*, *Diagnóstico* y *Tema*.

Para dejar la consulta lista hay que pasar por cuatro, y ya no se vuelven a
tocar salvo que cambie algo: [**Consulta**](#31-consulta),
[**Tarifas**](#32-tarifas), **Seguridad y copias** —[la clave de
recuperación](#33-la-clave-de-recuperación) y [la verificación en dos
pasos](#34-verificación-en-dos-pasos-opcional-recomendable)— y
[**Conexiones**](#35-conectar-google). *Cuestionarios* solo hace falta si se van
a pasar [test](#cuestionarios), *[Mensajes al
paciente](#38-mensajes-al-paciente)* trae el texto ya escrito,
*[Diagnóstico](#36-informes-de-diagnóstico)* no se toca y *[Tema](#37-tema)* es
cuestión de gusto.

![Pantalla de Administración, abierta por la pestaña Consulta con los datos de la profesional](imagenes/administracion.png)

### 3.1 Consulta

Tres cosas en esta pestaña:

- **Datos de la profesional**: nombre y apellidos, NIF, número de colegiada,
  dirección. Salen en las facturas y en los informes. **El número de colegiada es
  obligatorio** en la factura de un servicio sanitario. Pulsar **Guardar datos**.
- **Consentimiento vigente**: una etiqueta con la versión del documento de
  consentimiento que se está haciendo firmar (por ejemplo `2026-01`). No es el
  documento en sí —el consentimiento firmado de cada paciente se guarda en su
  ficha, ver [Registrar el consentimiento](#registrar-el-consentimiento)—, solo
  sirve para saber quién firmó qué: al cambiar la versión, las fichas que habían
  firmado la anterior quedan marcadas para volver a firmar.
- **Logotipo de la consulta**: se estampa como marca de agua muy atenuada en las
  facturas, informes y expedientes que se exporten. Opcional.

### 3.2 Tarifas

- **Tipos de terapia**: la lista de lo que ofrece la consulta. Vienen dos puestas,
  **Terapia individual** y **Terapia de pareja**, y se pueden añadir las que hagan
  falta con **Añadir**: se le pone nombre (por ejemplo, «Individual online») y se
  marca **De pareja** si necesita dos personas. Cada una lleva su propio precio,
  que es el que se aplica a las sesiones de los casos abiertos con esa terapia.
- **Enlace del consentimiento**: debajo de cada terapia, la dirección de la página
  donde se rellena su consentimiento (cada terapia tiene la suya, porque el documento
  anuncia su precio y sus condiciones). **Copiar** lo deja en el portapapeles para
  pegárselo a la persona por WhatsApp o por correo; **Abrir** lo abre en el navegador
  para comprobarlo. Se guarda con **Guardar tarifas**, como todo lo demás de esta
  pestaña. Es lo que se le manda *antes* de darla de alta: cuando llegue el PDF
  firmado, se adjunta en el alta y la ficha se rellena sola.
- **Retirar una terapia**: el interruptor de cada línea. Una terapia retirada deja
  de ofrecerse al abrir casos nuevos, pero **no se borra nada**: los casos que ya
  la usaban siguen igual y su historial de precios se conserva. Se puede volver a
  activar cuando se quiera.
- **Aviso para cancelar**: horas. Por debajo de ese margen, la sesión cancelada
  se cobra entera. Vienen 24 puestas.
- **Recordar al paciente**: horas antes de la sesión para enviarle el correo de
  recordatorio. Un 0 significa no enviar ninguno.
- **Aviso de Google Calendar**: minutos antes de cada sesión para que el propio
  calendario te avise, en el móvil o en el ordenador. Vienen 15; un 0 significa sin
  aviso. Es para ti, no para el paciente, y vale para las sesiones que se agenden o
  se toquen a partir de ese momento.
- **Plazo para recuperar una sesión**: días que se dan por defecto cuando el
  pago de una sesión cancelada se deja como crédito. El consentimiento anuncia
  un mes (30); se puede ampliar caso por caso, con un motivo.

Pulsar **Guardar tarifas**.

Cambiar una tarifa **solo afecta a lo que se agende a partir de ese momento**.
Las sesiones ya agendadas conservan el importe que tenían.

### 3.3 La clave de recuperación

En la pestaña **Seguridad y copias** hay cuatro apartados: el registro de accesos
y las copias de seguridad (los dos explicados en [Copias de seguridad y
recuperación](#7-copias-de-seguridad-y-recuperación)), la clave de recuperación y
la verificación en dos pasos. Los dos últimos se dejan puestos ahora.

Esto es lo más importante de toda la guía.

1. En **Administración › Seguridad y copias**, bajar hasta **Clave de recuperación**.
2. Escribir la contraseña en **Confirma tu contraseña**.
3. Pulsar el botón de generar.
4. Aparece un código de ocho grupos, tipo `4KWQ-9M2T-…`. Pulsar **Guardar en un
   archivo…**, imprimirlo, y **guardar el papel fuera del ordenador**: una
   carpeta física, una caja fuerte, en casa.
5. Pulsar **Ya la he guardado** para que desaparezca de pantalla.

Es lo único que permite entrar si se olvida la contraseña. No sirve de nada
guardarlo en el mismo ordenador, ni en el correo. Generar una clave nueva
invalida el papel anterior.

### 3.4 Verificación en dos pasos (opcional, recomendable)

Añade un segundo candado: además de la contraseña, un código de seis dígitos que
va cambiando y que sale de una app en el móvil (Google Authenticator, Aegis,
1Password, la que sea).

1. En la misma pestaña, bajar hasta **Verificación en dos pasos**.
2. Escribir la contraseña y pulsar **Activar…**.
3. Aparece un código QR. Abrir la app de verificación en el móvil, darle a añadir
   cuenta y escanearlo. Si no se puede escanear, teclear a mano el texto que sale
   debajo del QR.
4. La app empieza a mostrar un código de seis dígitos. Escribirlo en la casilla y
   pulsar **Activar**.

A partir de ahí, cada vez que se entre se pedirá la contraseña y después ese
código. Para desactivarlo hacen falta la contraseña y un código válido.

**Si se pierde el móvil.** Se entra con la clave de recuperación en papel (la de
[La clave de recuperación](#33-la-clave-de-recuperación), ahora sí): al hacerlo,
la verificación en dos pasos se apaga y hay que volver a configurarla con el
móvil nuevo. Por eso el papel sigue siendo
imprescindible aunque se use el segundo factor.

**La hora tiene que estar bien.** El código depende del reloj: si el del ordenador
o el del móvil va desajustado más de medio minuto, el código se rechaza. Con la
hora automática activada en ambos no hay problema.

### 3.5 Conectar Google

Sirve para meter las sesiones en el calendario, crear los enlaces de Meet, subir
las copias de seguridad a Drive y dejar en Drive los papeles del mes para la
gestoría.

**Cómo se ven las sesiones en Google Calendar.** Cada una lleva un color según el
cobro: **amarillo** si está pendiente, **verde** si está pagada y **morado** si es
una recuperación cubierta con crédito. Cambia sola al marcar o anular el pago. Y
cada una avisa unos minutos antes (ver [Tarifas](#32-tarifas)).

Se conecta desde **Administración › Conexiones** (o en la pantalla del primer
arranque, [Crear la consulta](#2-crear-la-consulta-solo-la-primera-vez))
cargando el archivo de credenciales `client_secret.json`. Se abre el navegador,
se acepta con la cuenta de la consulta, y ya queda.

**El icono de la nube.** Arriba en la barra lateral, junto a «Bitácora», hay un
icono que dice cómo está la conexión, estés en la sección que estés:

- **Gris**: hay internet y Google funciona.
- **Ámbar** (nube tachada): hay internet, pero Google no está operativo — la
  cuenta está sin conectar, hay que volver a conectarla o Google no responde.
- **Rojo** (wifi tachada): no hay internet.

Al pulsarlo se ve el detalle —Internet, Calendar y Meet, Drive— con dos botones:
**Comprobar ahora** e **Ir a Conexiones**, que lleva a la pestaña donde se conecta
la cuenta. Si dice «Hay que volver a conectar», es que Google ha retirado el
permiso (pasa al cambiar la contraseña de la cuenta): basta con pulsar otra vez
**Conectar con Google**.

**Si se va la conexión.** Al perderla —o al abrir la aplicación sin ella— sale
una franja encima de la sección con lo que no va a funcionar mientras dure:
lo que se agende, mueva o cancele no llegará a Google Calendar, no se pueden
crear enlaces de Meet ni enviar correos, y las copias no suben a Drive. Se
cierra con el aspa y no vuelve a salir hasta el siguiente corte; cuando vuelve
la conexión se va sola.

Se puede seguir trabajando: todo se guarda en el ordenador. Una sesión que se
agenda, se mueve o se cancela sin conexión queda **marcada**: en la agenda lleva
una nube tachada junto a la hora, y en su detalle lo dice («El último cambio de
esta sesión no ha llegado a Google Calendar»). Lo único que no se puede hacer
sin conexión es agendar una sesión **con Meet**: el enlace lo crea Google.

Mientras haya alguna marcada, encima de la agenda sale una línea que dice
cuántas son, sea cual sea su fecha. Cuando vuelva la conexión, su botón
**Pasar a Google Calendar** las deja todas al día de una vez; no hace falta
acordarse de cuáles eran. Si Google vuelve a fallar a mitad, se para ahí y
dice cuántas quedan: basta con pulsarlo otra vez más tarde. El mismo botón
está también en el detalle de cada sesión, para pasar solo esa.

Mientras se sepa que no va a funcionar —sin internet, con Google sin responder
o con la cuenta sin conectar—, el botón no aparece y en su lugar se dice por
qué. Vuelve solo en cuanto el indicador de conexión ve que todo va bien.

**Si se mueve o se borra una sesión desde Google Calendar.** Bitácora mira, al
abrir la agenda y como mucho cada dos minutos, si alguna de sus sesiones se ha
movido o borrado en Google (por ejemplo, desde el móvil). **No lo aplica solo**:
moverla o borrarla allí se salta el aviso de 24 horas, el crédito de sesión y el
aviso al paciente. Encima de la agenda sale una línea con cuántas hay, y
**Revisar** lleva a la primera y la deja elegida. En su detalle:

- Si **se movió**: **Aceptar la hora de Google** la reprograma también aquí y
  ofrece avisar al paciente del cambio, como al reprogramar. **Dejarla en Google
  como estaba** la devuelve a su hora en el calendario.
- Si **se borró** y de verdad no se va a dar: se cancela con los botones de
  siempre (con cargo, con crédito o devolviendo el pago), y la línea desaparece.
  Si se borró sin querer: **Volver a ponerla en Google**.

Si en Google se vuelve a dejar a su hora, el aviso se quita solo. Alargar o acortar
el evento allí no cuenta: solo la hora de inicio, que es la que tiene el paciente.

**Qué ve Google y qué no.** En el calendario solo aparece una etiqueta del tipo
`Sesión · AR-3f9c1b`: nunca el nombre del paciente ni el motivo. El paciente no
se añade como invitado del evento. Bitácora solo mira sus propias sesiones: las
citas personales del mismo calendario no se leen. Las copias que suben a Drive van
cifradas: Google recibe bytes que no puede leer. Lo único que queda legible en Drive
es la carpeta de la gestoría, con el resumen de cobros y las facturas (ver
[Subir a Drive para la gestoría](#subir-a-drive-para-la-gestoría)).

### 3.6 Informes de diagnóstico

En **Administración › Diagnóstico** está el registro de fallos técnicos que la
aplicación recoge sola: una copia que no se pudo hacer, Google que no responde,
un error inesperado. En cada arranque se manda un informe con lo nuevo al
correo de quien mantiene la aplicación, **sin que haya que pulsar nada**.

El informe **no lleva datos de pacientes**: solo el tipo de fallo, la traza
técnica y datos del equipo (versión, sistema, espacio en disco). Desde esa
misma pestaña se puede **desactivar el envío automático**, mandar uno en el
momento con **Enviar informe ahora** —útil si te pido que me lo envíes al
contarme un problema— y marcar cada incidencia como revisada. El registro no se
borra.

### 3.7 Tema

En **Administración › Tema** se elige el aspecto de la aplicación: **Claro**,
**Oscuro** o **Automático**. Cambia en cuanto se pulsa —no hay que guardar ni
volver a entrar— y así se queda para los siguientes arranques.

**Automático** es lo que viene de fábrica: la aplicación sigue al sistema, de
modo que si Windows se pone oscuro al anochecer, Bitácora también.

El tema es de **este ordenador**, no de la consulta: no viaja con los datos ni
con las copias de seguridad, así que el portátil puede ir en oscuro y el
ordenador de la mesa en claro.

### 3.8 Mensajes al paciente

Bitácora escribe sola cuatro correos: el de **dar una cita**, el de **cambiarla
de hora**, el **recordatorio** de unas horas antes y el de **enviar una
factura**. En **Administración › Mensajes al paciente** se elige cuál en el
desplegable de arriba y se reescribe a gusto: el asunto y el mensaje.

Vienen escritos de fábrica, así que **no hay que tocar nada** para empezar a
usar la aplicación. Y esto es solo el borrador: el correo se puede seguir
retocando en el momento de enviarlo, en la ventana **Enviar la cita** ([ver
Avisar al paciente](#avisar-al-paciente)) o **Enviar la factura** ([ver
Facturación](#8-facturación)).

**Los datos se ponen con los botones.** La fecha, la hora, el nombre del
paciente, el enlace de la videollamada y las horas de aviso cambian en cada
cita, así que en el texto van como un hueco. No hay que escribirlos a mano: se
pone el cursor donde se quiere que salgan, se pulsa el botón —*fecha*, *hora*,
*paciente*, *enlace*, *horas de aviso*— y el hueco aparece ahí. En pantalla se
ven entre llaves (`{fecha}`); al paciente le llega ya el dato de su cita.

**Cada mensaje tiene los suyos.** El de la factura no lleva hora ni enlace, sino
*número de factura* e *importe*; los botones cambian solos al elegir el mensaje.
Poner el hueco de otro mensaje se considera una errata y no deja guardar:
saldría en el correo con las llaves y todo.

Lo que **no** hay, ni ahí ni en el impreso, es la fecha de la sesión: cruzada con
un nombre cuenta que esa persona fue a consulta y qué día, y eso no hace falta
para cobrar.

Una regla, la única: **la línea que lleve el enlace desaparece entera cuando la
cita no es online**. Por eso el enlace conviene dejarlo en su propia línea, y no
metido en mitad de un párrafo que haga falta.

A la derecha, **Así le llegará** enseña el correo terminado con datos de
ejemplo, según se escribe. La casilla **Verlo como una cita online** sirve para
comprobar cómo queda con enlace y sin él.

Si algo no cuadra —un hueco mal escrito, una cita sin fecha o sin hora, una
factura sin su número— sale avisado en rojo y **Guardar el mensaje** no deja
pulsarse hasta arreglarlo: más vale verlo aquí que en el correo que ya ha
salido. **Volver al texto original** deja el mensaje como venía de fábrica.

Lo que no debe ir en estos correos: **nada de lo que se habla en sesión**. Un
correo acaba leído por quien no debe más veces de lo que uno cree, y por eso el
texto de fábrica solo dice día, hora y enlace.

---

## 4. El día a día

Cinco secciones a la izquierda: **Agenda**, **Pacientes**, **Facturación**,
**Cuentas** y **Administración**.

![Listado de pacientes, con la rueda de lo que se enseña y los botones de Abrir ficha y Dar de alta](imagenes/pacientes.png)

En la primera columna del listado aparece una **tarta** junto a quien cumple años
ese día, para poder felicitarle al entrar por la puerta. Sale solo el día del
cumpleaños y no hace nada más: no cambia la ficha ni avisa a nadie. A quien nació
un 29 de febrero se le marca el 28 los años que no son bisiestos.

### Qué se enseña en el listado

De entrada, **Pacientes** enseña solo a quien tiene un caso abierto: lo normal es
buscar a alguien que está en terapia, no repasar a todos los que han pasado por la
consulta. El botón de la **rueda dentada**, junto a la lupa, despliega dos casillas
que añaden más gente a la lista:

- **Pacientes sin caso abierto**: quien está dado de alta pero no tiene ninguna
  terapia en curso, porque terminó o porque todavía no se le ha abierto el caso.
- **Pacientes archivados**: las fichas archivadas (ver abajo), tengan caso abierto
  o no. Salen con una **caja** en la primera columna para distinguirlas.

A diferencia de las de la agenda, estas dos casillas no se recuerdan: cada vez que
se abre la aplicación el listado vuelve a empezar por la gente en terapia.

### Archivar una ficha

Con los años se acumulan fichas de gente que ya no viene y que estorba al buscar.
**Botón derecho** sobre su fila → **Archivar**, y deja de salir en el listado.

Archivar es solo una manera de ordenar la lista. No cierra sus casos, no borra
nada, no le quita el correo y no tiene nada que ver con **suprimir** la ficha, que
es el derecho del RGPD y va por otro sitio. Por eso no pide confirmación: se
deshace igual de rápido. Para volver a verla, se marca **Pacientes archivados** en
la rueda; y sobre su fila, el mismo botón derecho ofrece **Desarchivar**.

Si alguien archivado vuelve a terapia, basta con abrirle un caso (o reabrir el que
tenía): sale solo del archivo, para que no quede escondido justo cuando más se le
busca. Y si se intenta darlo de alta otra vez, la ventana avisa de que ya existe y
de que su ficha está archivada.

### Dar de alta a un paciente

**Pacientes** → **Dar de alta**. Se abre una ventana: arriba, el consentimiento
firmado, si ya lo trae (ver [Registrar el consentimiento](#registrar-el-consentimiento):
si viene de la web de la consulta, rellena él solo lo demás); debajo, DNI o NIE,
nombre, apellidos, fecha de nacimiento, teléfono y correo (el correo es opcional,
pero sin él no se le pueden enviar avisos de cita).

Debajo va el **domicilio**, también opcional. Se puede dejar en blanco y
completarlo después desde la ficha, pero hace falta para poder facturarle: la
factura lleva la dirección del destinatario. Va todo junto —calle, código
postal, municipio y provincia—: media dirección no vale, y la ventana avisa si
se rellenan unos campos y otros no.

![Ventana de dar de alta a un paciente](imagenes/dar-de-alta.png)

### Abrir un caso

Una persona dada de alta todavía no tiene terapia. Hay que abrirle un caso:
**Abrir ficha** y, arriba a la derecha, el botón **+ Abrir caso**. Se abre una
ventana donde se elige el **tipo de terapia**; si la terapia elegida es de
pareja, pide también a la otra persona con **Elegir…**, y esa persona tiene que
estar dada de alta antes.

El botón está fuera de la ficha, junto al nombre, y no dentro: ahí abajo hay ya
un desplegable de **Caso** que es para *cambiar de caso en curso*, y los dos
juntos se confundían.

También se puede abrir en el mismo momento del alta, marcando **Abrirle un caso al
darlo de alta**. Ahí, si la terapia es de pareja, la otra persona no hace falta
que exista antes: **Darla de alta a la vez** la da de alta en la misma ventana (ver
[Registrar el consentimiento](#registrar-el-consentimiento), donde se cuenta con
la pareja).

Las sesiones y los informes cuelgan del caso, no de la persona. Una misma
persona puede tener a la vez un caso individual y uno de pareja, y cada uno
lleva su historia y su facturación por separado.

### Cerrar un caso

Cuando la terapia termina, en la tarjeta del caso de la ficha se pulsa **Cerrar
caso** y se indica la fecha de cierre. Un caso cerrado no admite citas nuevas,
pero su historia, sus informes y sus facturas se conservan. Si hay que retomarlo,
**Reabrir** lo vuelve a activar.

Cerrar los casos hace falta, además, para poder **suprimir** la ficha más
adelante, ver [Cosas que conviene saber](#10-cosas-que-conviene-saber): una ficha
con casos abiertos no se puede suprimir.

### Registrar el consentimiento

Si el paciente trae ya el consentimiento firmado, lo más cómodo es adjuntarlo en
el propio **Dar de alta**: la tarjeta de arriba del todo, **Consentimiento
informado firmado**, admite el PDF con **Adjuntar PDF firmado…** o arrastrándolo
sobre el recuadro. No se guarda nada hasta pulsar **Dar de alta**; si el alta no
sale (un DNI repetido, por ejemplo), el PDF tampoco se queda guardado. Si se
adjunta el que no era, **Quitar**.

Si el consentimiento se firmó en la web de la consulta, **sus datos se copian
solos al formulario**: nombre, apellidos, DNI, fecha de nacimiento, teléfono,
correo y domicilio. La provincia sale del código postal y el municipio, del lugar
donde se firmó, que conviene revisar. Todo queda a la vista para corregirlo antes
de pulsar **Dar de alta**, y como fecha de firma se guarda la que dice el
documento. Un consentimiento escaneado en papel se adjunta igual, pero sin copiar
nada: los datos se teclean.

Si es un **consentimiento de pareja**, el diálogo se ensancha y pone a las dos
personas una al lado de la otra, cada una con sus datos, y el caso que se ofrece
abrir es el de pareja. Si una de las dos ya tenía ficha (mismo DNI), el diálogo lo
dice al adjuntar y se usa la suya, sin cambiar sus datos: solo se le registra el
consentimiento nuevo.

![Ventana de dar de alta con un consentimiento de pareja: las dos personas una al lado de la otra](imagenes/dar-de-alta-pareja.png)

Lo mismo se puede hacer **a mano**, sin consentimiento: al marcar **Abrirle un
caso** con una terapia de pareja, la otra persona se puede **Elegir…** entre las
fichas o **Darla de alta a la vez**. Con lo segundo aparece su columna al lado; si
al teclear su DNI resulta que ya tenía ficha, se dice y se usa la suya. **Quitar**,
en su cabecera, vuelve al alta de una sola persona. Un consentimiento escaneado
adjuntado así se registra a las dos; uno individual de la web no, porque lo firmó
una sola persona: para la pareja hace falta el de pareja.

Si quien llega **ya tuvo ficha** —alguien que vuelve al cabo del tiempo—, el alta
no la puede crear otra vez: avisa de que ese DNI ya existe y ofrece **Abrir su
ficha**, que lleva directamente allí para registrarle el consentimiento nuevo.

Si no, se registra después desde la ficha, pestaña **Resumen**, tarjeta
**Consentimiento informado**:
**Registrar consentimiento firmado…**, y se adjunta el documento escaneado. Queda
guardado cifrado dentro de la ficha. Al lado, un icono y una línea dicen si está
firmado y con qué versión.

Una vez registrado sale **Ver consentimiento firmado…**, que lo abre en una
ventana aparte. Se descifra en memoria: para mirarlo no hace falta dejar una
copia suelta en el disco.

**Los consentimientos no se pisan.** Al registrar uno nuevo, el anterior no
desaparece: pasa a **Anteriores**, debajo, con su fecha y su versión, y se puede
abrir igual con **Ver…**. El de arriba es el que vale hoy; los de abajo son la
prueba de a qué consintió mientras estuvieron vigentes, que es lo que hay que
poder enseñar si alguna vez se discute una sesión de entonces. Todos salen
también en el expediente del derecho de acceso.

Si el escaneo ya está a la vista en el Explorador, se puede **arrastrar el PDF**
sobre el recuadro de puntos que hay justo debajo de esos botones y soltarlo ahí:
hace lo mismo sin pasar por el diálogo de archivos. El recuadro se enciende
cuando lo que se lleva encima vale, y se pone en rojo cuando no (por ejemplo, un
Word en vez de un PDF, o varios archivos a la vez).

---

## 5. Agenda

![Vista de Agenda en modo Semana, con las sesiones en su hora](imagenes/agenda.png)

### Los tres modos

La Agenda es un calendario y se mira de tres maneras, que se eligen en la
cabecera:

- **Día**: la jornada entera, hora a hora. Como la columna es ancha, cada sesión
  se lee de un vistazo sin tener que abrirla: hora de inicio y fin, duración,
  paciente, importe y cobro. Arriba de todo, cuántas sesiones hay, lo que suman y
  cuánto queda por cobrar ese día.
- **Semana**: una columna por día. Es el modo de trabajo y con el que se entra.
- **Mes**: las semanas completas, con las sesiones escritas dentro de cada
  casilla. Es para encuadrar el mes, no para cobrar; por eso aquí no sale el
  panel de la derecha y sí un pie con las sesiones del mes, lo previsto, lo
  cobrado y lo que sigue sin cobrar, con la leyenda de los colores al lado. En
  cada casilla caben cuatro sesiones: si ese día hay más, debajo pone «+2 más» y
  se ven entrando en el día. Los días de los meses de al lado salen apagados,
  para no romper la rejilla.

Las flechas **‹** y **›** mueven un día, una semana o un mes, según el modo en
el que se esté. **Hoy** vuelve al presente.

En Día y en Semana una línea fina cruza la jornada de hoy por la hora que es, y
la franja que se dibuja va de las 8 a las 20 salvo que haya sesiones fuera de
ella: entonces se estira lo que haga falta, porque una rejilla más alta se baja
con la barra y una sesión escondida no se ve nunca.

### Qué se enseña

El botón de la **rueda dentada**, junto a los tres modos, despliega lo que la
agenda enseña y lo que no. Son dos casillas, y las dos se quedan como se dejen:
al volver a abrir la aplicación siguen igual.

**Fin de semana** añade el sábado y el domingo. Viene apagado porque la consulta
no suele pasar sesión esos días y, sin esas dos columnas, las cinco de diario
son bastante más anchas. Si hay una sesión en sábado o en domingo, su columna
sale igual aunque el interruptor esté apagado: una preferencia de ancho no puede
esconder una cita.

**Sesiones canceladas** viene puesto. Al quitarlo, las canceladas —tanto las
avisadas en plazo como las avisadas tarde— dejan de dibujarse, y la hora que
ocupaban vuelve a ofrecerse como rato libre para agendar. Las ausencias («no
asistió») **no** se esconden: esas se cobran íntegras y tienen que verse.

Esconderlas es solo una manera de mirar, no de contar: los pies del día y del
mes —sesiones, previsto, cobrado y lo que sigue sin cobrar— siguen incluyendo
todo lo que hay, esté a la vista o no. Una cancelación fuera de plazo se abona, y
esa deuda no puede desaparecer porque se quite una casilla.

### Del mes al día

En **Mes**, cada fila lleva a la izquierda una franja estrecha con el número de
la semana. Al pulsarla, esa semana se abre en modo Semana. Y al pulsar una
casilla se abre ese día. Es el camino natural de trabajo: el mes enseña dónde
está la carga y desde ahí se entra a trabajarla, sin volver a **Hoy** y contar
flechas.

Pulsar directamente **una sesión** del mes también baja a su día, y la deja
elegida en el panel de la derecha. En el mes no se cobra —no hay panel—, así que
el clic sobre una sesión lleva al único sitio donde sí se puede.

### Agendar una sesión

En **Agenda**, el botón **+ Nueva sesión** abre una ventana: elegir el caso, la
fecha, la hora y la duración. El caso se busca escribiendo el nombre del
paciente, que con la lista larga es más rápido que bajarla entera; entrando en el
campo sin escribir nada se despliega completa, para cuando no se recuerda el
nombre exacto. La duración se elige entre las habituales (30, 45, 50, 60, 75 y 90
minutos). El importe no se pide aquí: sale de la tarifa del tipo de terapia del
caso.

![Ventana de Nueva sesión, con el caso, la fecha y la hora elegidos](imagenes/nueva-sesion.png)

Para online, **Crear enlace de Meet** lo genera automáticamente al agendar. Si se
prefiere otro (Zoom, el que sea), se desmarca esa casilla y se pega el enlace en
el campo que aparece debajo.

Pulsar **Agendar**.

Hay un atajo que ahorra teclear la fecha: en **Día** y en **Semana**, al pasar
el ratón por un rato libre aparece **+ Agendar a las …**. Al pulsarlo se abre la
misma ventana con ese día y esa hora ya puestos. Los ratos libres se ofrecen de
media hora en media hora, para que encajen también las sesiones de 30 y de 45
minutos, y solo de hoy en adelante: en un día pasado no salen, porque agendar
hacia atrás no se admite y ofrecerlo sería mentir.

### Avisar al paciente

Justo después de agendar sale una ventana **Enviar la cita** con el correo ya
redactado: destinatario, asunto y mensaje, todo modificable. **Enviar al
paciente** lo manda; **Ahora no** lo deja sin enviar. La sesión queda agendada
en los dos casos: esa ventana solo decide si se avisa.

La misma ventana sale al **reprogramar** una sesión, con los datos de la cita
nueva y el texto adaptado para que se entienda que es un cambio de hora, no una
cita más.

El texto con el que aparece redactado se puede cambiar de una vez para siempre
en [Mensajes al paciente](#38-mensajes-al-paciente); lo que se escriba aquí vale
solo para este correo.

Si el paciente no tiene correo en la ficha, se puede escribir ahí mismo.

**Por WhatsApp**: clic derecho sobre la sesión en el calendario, **Abrir en
WhatsApp**. Se abre WhatsApp en la conversación con el paciente (el teléfono de su
ficha) y con el mismo texto del correo ya escrito. **No se envía solo**: se revisa y
se pulsa Intro. No hace falta tener al paciente guardado en los contactos del móvil.

Si el ordenador no tiene WhatsApp instalado, se abre la página de WhatsApp en el
navegador, que ofrece seguir en WhatsApp Web. Y el texto queda copiado de todas
formas: si alguna vez se abre el chat vacío, basta pegarlo.

Si el teléfono de la ficha no se entiende (lleva letras, o dos números), Bitácora
no abre nada y pide corregirlo en la ficha: es preferible a escribir a quien no es.
Un número de fuera de España se escribe con su prefijo, como `+44 7700 900123`.

**Copiar invitación**, en el mismo menú, solo copia el texto, para pegarlo
donde se quiera.

WhatsApp no deja que un programa envíe mensajes por su cuenta desde un número
normal, y es mejor así: las formas de saltárselo incumplen sus condiciones y pueden
acabar con el número bloqueado. Por eso los recordatorios automáticos van por correo.

**El recordatorio automático** (el que se configura en [Tarifas](#32-tarifas))
se manda al abrir Bitácora, no por su cuenta con el ordenador apagado: si un día
no se abre el programa, ese día no se
avisa a nadie. Es a propósito, porque un envío que falla sin que nadie lo vea es
peor que no enviarlo. Cada sesión se recuerda una sola vez, así que abrir y
cerrar el programa varias veces no repite el correo. Su texto también se
reescribe en [Mensajes al paciente](#38-mensajes-al-paciente).

### Los colores del cobro

Cada sesión lleva su color de cobro en el filete de la izquierda del bloque, y
el texto que dice lo mismo sale en el panel de la derecha al elegirla (en **Mes**,
en la leyenda del pie). El color va siempre acompañado de su texto: impreso en
blanco y negro, o visto con daltonismo, no distingue una sesión impagada de una
que se abona por haberse cancelado tarde.

Las sesiones que no llegaron a darse —canceladas o con ausencia— salen además
tachadas: el color dice cuánto se cobra, y el tachado dice si ocurrió, que son
dos preguntas distintas.

- **Verde** · «Pagada»: cobrada. Ya se puede facturar. Al elegir la sesión,
  debajo pone por dónde entró el dinero: «Cobrada por bizum», por ejemplo. Si en
  vez de un cobro se le aplicó un crédito, pone «Pagada con crédito».
- **Neutro** · «Pendiente»: sin pagar, pero todavía queda margen antes de la
  sesión.
- **Ámbar** · «Sin pagar · menos de 24 h»: sin pagar y ya dentro de las horas de
  aviso. Es la que hay que mirar.
- **Rojo** · «Impagada»: la sesión ya ha empezado y sigue sin cobrarse.
- **Rojo** · «Se abona íntegra»: cancelada fuera de plazo, o ausencia sin avisar.
  Se cobra aunque no se haya dado.
- **Azul** · «Sin cargo · crédito»: cancelada sin cargo, pero ya estaba pagada:
  el importe queda como crédito para una sesión de recuperación.
- **Gris** · «Sin cargo»: cancelada en plazo. No hay nada que cobrar.

De una sesión cobrada sin forma de pago —las de antes de que se guardara, o una
cubierta con un crédito viejo— el panel avisa de que no consta cómo entró el
dinero. Se arregla con **Corregir la forma de pago**, y hace falta: la factura la
lleva impresa, así que sin ella no se puede emitir. Se dice aquí, que es donde se
arregla, y no al intentar facturar.

### Cerrar una sesión

Al pulsar una sesión del calendario se llena el panel de la derecha:

- **Pagada**, que cobra por Bizum sin preguntar, que es como entra casi todo. El
  botón lleva pegada una flechita a la derecha: al pulsarla salen **Pagada por
  Bizum** y **Pagada por transferencia**, para el cobro que no vino por Bizum. La
  forma de pago queda guardada y es la que luego sale impresa en la factura. (Y
  **Anular el pago** si se marcó por error.)
- **Corregir la forma de pago**, en una sesión ya cobrada: sale al pulsarlo un
  desplegable con **Se cobró por Bizum** y **Se cobró por transferencia**. Es
  para cuando se marcó por Bizum lo que llegó por transferencia. Cambia solo la
  forma; **la fecha del cobro no se mueve**, que es lo que pasaría anulando el
  pago y volviéndolo a marcar. Si esa sesión ya estaba facturada, la factura no
  cambia: para eso hay que rectificarla y emitirla de nuevo (ver
  [Facturación](#8-facturación)).
- **Realizada**: la sesión se dio.
- **No asistió**: no vino y no avisó. Se cobra.
- **Reprogramar**: mueve la sesión a otra fecha conservando el importe y el
  pago. Es lo que se usa cuando el paciente no puede venir pero se le va a dar
  la sesión igualmente. Al confirmar el cambio sale la misma ventana de aviso
  que al agendar, esta vez con la fecha nueva y diciendo que la cita se ha
  movido; **Ahora no** la deja sin enviar y la sesión queda movida igualmente.
- **Cancelar sesión**: la cancelación normal. No hay que echar cuentas: el
  programa mira la hora y decide solo. Si el aviso ha llegado con el margen
  pactado por delante, la sesión queda sin cargo; si ha llegado por debajo de
  ese margen, se abona entera.
- **Cancelar sin cargo**: fuerza mayor. No se cobra aunque el aviso llegue
  tarde. Es la excepción que recoge el consentimiento, y la decisión de aplicarla
  es tuya.

Si al dar una sesión por **realizada** ya estaba pagada, sale una ventana
**Emitir factura** que ofrece facturarla ahí mismo, sin pasar por Facturación. Si
el caso es de pareja se elige a quién se le factura; si no, basta con confirmar.
**Ahora no** la deja sin facturar: se puede emitir después desde la sección de
[Facturación](#8-facturación).

### Una sesión pagada que se cancela

Si la sesión ya estaba pagada, en vez de «Cancelar sin cargo» aparecen dos
opciones, porque hay que decidir qué pasa con el dinero:

- **Cancelar · dejar crédito para recuperar**: el importe queda como crédito
  para una sesión de recuperación de ese mismo caso. Se pone una fecha límite
  (por defecto, la que diga Administración; ampliarla más allá pide un motivo,
  que queda registrado). La decisión de perdonar un aviso tardío es tuya: aquí
  no se miran las 24 h.
- **Cancelar · devolver el importe**: no queda ni cobro ni crédito. El
  reintegro se hace por fuera.

Cuando el crédito existe, la sesión que lo generó muestra **Ampliar plazo del
crédito** en el panel.

### Recuperar la sesión

Al agendar una **Nueva sesión** de un caso con créditos disponibles aparece
**Cubrir con crédito**. Si se elige uno, la sesión queda pagada sin cobrar de
nuevo y se factura con normalidad cuando se dé por realizada. Si el importe del
crédito no coincide con el de la sesión, la diferencia se ajusta aparte.

---

## 6. Ficha, historia clínica, informes y material de trabajo

Desde **Pacientes** → **Abrir ficha**.

La ficha reúne los datos de la persona, sus casos abiertos, si tiene el
consentimiento firmado, su historia, sus informes, el material de trabajo que se
le haya pasado y los cuestionarios que se le hayan cumplimentado. Va por
pestañas: *Resumen*, *Historia*, *Informes*, *Material de trabajo* y
*Cuestionarios*.

### Corregir los datos de un paciente

En la pestaña **Resumen** de la ficha, la tarjeta **Datos** tiene un botón
**Editar**. Ahí se corrigen nombre, apellidos, DNI o NIE, fecha de nacimiento,
teléfono y correo: un número que cambia, un apellido que faltaba, o el documento
que se tecleó mal el primer día. **Descartar** deja la ficha como estaba.

El **domicilio** se corrige aparte, con su propio **Editar** justo debajo, porque
va todo o nada (calle, código postal, municipio y provincia).

Se comprueba lo mismo que al dar de alta: el DNI o NIE tiene que ser válido y no
puede ser el de otra ficha, el correo tiene que estar bien escrito y la fecha de
nacimiento no puede quedar en el futuro. Si algo no cuadra, se dice y el
formulario se queda abierto con lo tecleado.

Cada corrección queda anotada en el **registro de accesos**, y la anotación dice
qué campos cambiaron. Eso es lo que acredita haber atendido una **rectificación**
si el paciente la pide.

Dos avisos:

- Si se cambia el nombre o los apellidos, cambia también el **seudónimo** con el
  que la persona aparece en Google Calendar (ver
  [Conectar Google](#35-conectar-google)). Las citas ya creadas conservan
  el anterior.
- Una ficha **suprimida** no se corrige: hay que restaurarla antes.

### La historia clínica

La pestaña se abre **en lectura**, con la historia ya compuesta tal y como queda.
Para escribir se pulsa **Editar**; la primera vez la historia está en blanco y
vienen ya puestas las diez secciones de la plantilla, para rellenar debajo de cada
una.

Se escribe como en cualquier procesador de texto: se selecciona un trozo y se le
da formato con los botones de la barra de arriba —**Título**, **Subtítulo**,
negrita (Ctrl+B), cursiva (Ctrl+I), **Viñeta** y **Cita**—.

**A tener presente** es un campo aparte, debajo del editor. Lo que se escriba ahí
se ve nada más abrir la ficha, en un aviso destacado: es para riesgo, o para
cualquier cosa que no deba pasarse por alto. Nunca se rellena solo a partir del
texto de la historia.

**Guardar y ver** graba y devuelve a la lectura, que es donde se comprueba cómo
ha quedado. **Descartar** sale sin guardar.

### Informes

En la ficha: elegir el caso arriba, escribir un título y **Crear y escribir**. Se
redacta con la misma barra de formato que la historia y el mismo **Guardar y
ver**.

Los informes del caso salen en una lista; al pulsar uno se abre en lectura, con
**Editar** para retocarlo, **Cerrar informe** para volver a la lista y **Exportar
a PDF…**, que lo saca con el logotipo de marca de agua si se subió uno en
Administración.

### Material de trabajo

Pestaña **Material de trabajo** de la ficha. Cuelga del caso elegido arriba, igual
que los informes.

Para registrar algo: nombre (por ejemplo *WAIS-IV* o *BDI-II*), fecha en
que se pasó, notas o interpretación si se quiere, y el archivo. El archivo se
puede **arrastrar** sobre el recuadro de puntos o buscarlo con **…o elegir
archivo y guardar**; por los dos caminos se guarda con el nombre, la fecha y las
notas que estén escritos arriba. El archivo (PDF, o una foto/escaneo en JPG o
PNG) se guarda cifrado dentro de la ficha; en disco no queda nada legible.

Con un material elegido de la lista:

- **Previsualizar** — abre el archivo en una ventana aparte: las imágenes tal
  cual y los PDF como una imagen por página. El documento se descifra en memoria,
  no se escribe en el disco.
- **Guardar copia…** — descifra el archivo y lo deja donde se diga, para
  adjuntarlo a un informe o abrirlo con otro programa.
- **Eliminar** — borra el material y su archivo. Queda anotado en el registro de
  accesos, como cualquier otro movimiento sobre la historia clínica.

El material de trabajo entra también en el expediente que se le entrega al
paciente si ejerce su derecho de acceso.

### Cuestionarios

Pestaña **Cuestionarios** de la ficha. También cuelgan del caso elegido arriba.

Un cuestionario es una lista de preguntas con opciones y una forma de puntuarlas
(sumar, invertir los ítems de control, clasificar por tramos). Se preparan una vez
en **Administración → Cuestionarios**, importándolos desde un archivo JSON —lo
normal es pedirle a una IA que lo genere siguiendo `docs/cuestionarios.md`— y
**publicándolos**. Solo los publicados aparecen aquí.

Para pasar uno: elegir el cuestionario en el desplegable, **Cumplimentar…**,
marcar cada respuesta y **Guardar**. La aplicación suma y enseña la puntuación y
el tramo al momento. Si quedan respuestas sin marcar y el cuestionario no lo
permite, se guarda como *incompleto*.

Con un cuestionario elegido de la lista: **Ver respuestas** lo reabre en solo
lectura, se pueden editar las **notas**, y **Eliminar** lo borra (queda anotado en
el registro de accesos). También entran en el expediente del derecho de acceso.

Bitácora no interpreta clínicamente: solo cuenta y clasifica según lo que diga
cada plantilla.

---

## 7. Copias de seguridad y recuperación

### Cómo funcionan

Se hace una copia **al cerrar la aplicación, una vez al día**. Va cifrada con la
misma contraseña, y si Google está conectado sube sola a Drive, a la carpeta
«Bitácora · copias de seguridad».

La copia diaria (`bitacora-….zip`) solo lleva la base de datos: es pequeña y se
conservan los últimos días. Los documentos adjuntos (consentimientos, informes,
material de trabajo) se guardan **aparte, un solo ejemplar de cada uno**, en la carpeta
`copias/adjuntos` de al lado —y en su equivalente en Drive—. Así la copia de
cada día no vuelve a arrastrar los mismos documentos.

En Administración se puede forzar una con **Hacer una copia ahora**, ver las que
hay en Drive, y decidir cuántos días se conservan.

> Para llevarse una copia en un USB hay que copiar la carpeta `copias` **entera**
> (el `.zip` y la carpeta `adjuntos`), no solo el archivo. Está dentro de la
> carpeta de datos —normalmente `Documentos\Bitacora\copias`—; la ruta exacta
> aparece en **Administración**, debajo del título.

### Recuperar en un ordenador nuevo

Al abrir Bitácora por primera vez, en vez de crear la consulta:

- **Buscar en Drive…** — pide el archivo de credenciales de Google, abre el
  navegador, lista las copias que haya en Drive y se elige una. Trae también los
  documentos adjuntos.
- **Desde una carpeta…** — se apunta a la carpeta `copias` copiada entera (la del
  USB). Reconstruye la base y los documentos.
- **Desde un archivo…** — si solo se tiene el `.zip`. Recupera la consulta, pero
  sin los documentos adjuntos; avisa de cuántos faltan y se pueden traer luego de
  Drive.

Después pide la contraseña de siempre, y todo vuelve: pacientes, historias,
facturas, y también **la conexión con Google**, que viaja dentro de la copia.

### Si se olvida la contraseña

En la pantalla de entrada, **He olvidado la contraseña**. Pide el usuario, el
código de recuperación que se imprimió, y una contraseña nueva. El código se
puede escribir con guiones o sin ellos, y da igual mayúsculas o minúsculas.

Sin ese código no hay ninguna otra vía. No existe un «te enviamos un correo»:
si lo hubiera, quien entrara en el correo entraría en las historias clínicas.

Si estaba activada la verificación en dos pasos, al recuperar el acceso así se
apaga: hay que volver a configurarla (ver [Verificación en dos
pasos](#34-verificación-en-dos-pasos-opcional-recomendable)).

---

## 8. Facturación

![Pantalla de Facturación, con el desplegable de caso y el listado de facturas emitidas](imagenes/facturacion.png)

**Facturación** → elegir el caso, a quién se factura y **la sesión concreta**
→ **Emitir**.

**Cada factura es de una sola sesión.** El desplegable de sesión solo ofrece
las que están **ya dadas y ya cobradas** y que no se hubieran facturado antes;
si un caso tiene varias sesiones pendientes, hay que emitir una factura por
cada una. Una sesión sin cobrar no aparece en la lista.

La factura sale **exenta de IVA** por el artículo 20.Uno.3º de la Ley del IVA,
que es lo que corresponde a la asistencia sanitaria.

**El concepto es siempre «Prestación de servicios», y no hay ningún otro.** No dice la
modalidad (individual o de pareja), ni la fecha de la sesión, ni si llegó a darse: esa
factura puede acabar en manos de terceros —una mutua, una gestoría, quien la encuentre
en un cajón— y todo eso, cruzado con un nombre y un NIF, es un dato de salud.

**La factura sale en el impreso de siempre**: arriba, los datos de la consulta y
el número y la fecha; debajo, los del paciente por casillas (nombre, dirección,
población, código postal y provincia, que se toman de su domicilio en la ficha);
en medio, el concepto y el importe, sin nada más; y abajo el cuadro de IVA —al 0 %,
por la exención—, la forma de pago y el total.

**Sin domicilio del paciente y sin forma de pago, la factura no sale.** Son
contenido obligatorio del impreso, y una factura emitida ya no se puede
retocar. Si falta el domicilio, la aplicación lo dice por su nombre y hay que
completarlo en la ficha del paciente; si la sesión no dice cómo se cobró, se
arregla en la Agenda con **Corregir la forma de pago**.

### Corregir una factura ya emitida

**Una factura emitida no se edita**: la numeración es correlativa y sin huecos,
y con VeriFactu además será irreversible. Un error se corrige en dos pasos:

1. **Arreglar el dato donde vive**: el domicilio o el NIF, en la ficha del
   paciente; la forma de pago, en la Agenda.
2. Seleccionar la factura y pulsar **Emitir rectificativa**. Se abre una ventana
   que enseña **con qué datos va a salir** —nombre, NIF, dirección, forma de pago
   e importe, releídos de la ficha y de la sesión— y pide **la causa**. Solo hace
   falta escribirla («faltaba el domicilio del destinatario») y confirmar.

Esa ventana es la que evita repetir el error: si el domicilio sigue sin estar,
lo dice ahí y no deja emitir. Y si la factura salió a nombre del miembro
equivocado de una pareja, también se cambia ahí a quién se le factura.

**La rectificativa sustituye a la factura que corrige.** Sale por el mismo
importe y **en positivo** —el servicio se prestó y se cobró; no es un abono—,
pero con los datos ya buenos, y lleva impreso a qué factura sustituye, con qué
fecha y por qué causa. Va en **serie propia** (`R2026/0001`, frente a
`F2026/0001` de las ordinarias). Desde ese momento, la rectificativa es la
factura válida de esa sesión y es la que se entrega al paciente.

En el listado, la columna **Situación** dice en qué estado quedó cada una:
*Vigente*, *Rectificada* (sustituida por la suya) o *Rectificativa de…*. Ninguna
se borra: todas quedan guardadas y numeradas.

**Si hay que volver a corregir**, se rectifica **la rectificativa**, no la
factura de partida: `F2026/0006` → `R2026/0001` → `R2026/0002`. La aplicación no
deja rectificar dos veces la misma —dejaría dos facturas vivas para una sola
sesión— y te dice cuál es la que está vigente.

Cuidado con una cosa: la rectificativa es para **corregir un error** de la
factura. Si el paciente simplemente se ha mudado *después* de que se le
emitiera, esa factura no estaba mal y no hay nada que rectificar; la dirección
nueva sale sola en las facturas siguientes.

**Previsualizar…** enseña la factura seleccionada tal y como saldría impresa, en
una ventana aparte y sin sacar ningún archivo al disco. Sirve para mirarla antes
de mandarla: que el NIF y la dirección sean los buenos, que el importe cuadre, y
que una factura ya rectificada salga con su marca de **SIN EFECTO** cruzada. Desde
esa misma ventana se puede **exportar a PDF** sin volver al listado.

**Enviar al paciente…** se la hace llegar por correo, con el PDF adjunto. Se
abre una ventana con el mensaje ya redactado —el de **Administración › Mensajes
al paciente**— y el correo de quien la paga puesto, si lo tiene en su ficha; todo
se puede retocar antes de que salga. Hace falta la cuenta de Google conectada
([ver Conectar Google](#35-conectar-google)). Una factura que ya se rectificó no
se manda: Bitácora dice cuál es la que está vigente.

**Exportar a PDF…** saca cualquiera de ellas para guardarla o mandarla a mano.

---

## 9. Cuentas: ingresos, gastos y balance

![Cuentas, pestaña de ingresos, con las citas por estado y el detalle de cobros del mes](imagenes/resumen-mensual.png)

**Cuentas** → elegir el mes arriba a la derecha (el selector va por mes y año,
sin día). El mes vale para las tres pestañas: **Ingresos**, **Gastos** y
**Balance**. Al entrar se abre **Ingresos**.

### Ingresos

Lo que suele pedir la gestoría cada mes: cuántas sesiones hubo por estado
(realizadas, no asistió, canceladas…), el total cobrado, y el detalle de cada
cobro.

**Va por lo cobrado, no por lo facturado.** Si una sesión de agosto se cobró en
agosto pero no se factura hasta septiembre, cuenta en el resumen de agosto — el
mes en que entró el dinero, no el mes de la factura. No hace falta tener las
facturas al día para sacar el resumen.

El detalle de cada cobro lleva la fecha, el nombre, el NIF y la dirección de
quien paga, y el importe: los mismos datos que llevaría la factura, aunque esa
sesión todavía no se haya facturado. Es lo que la gestoría necesita para
declarar el ingreso.

**Créditos de sesión.** Si en el mes hubo créditos (sesiones pagadas que se
cancelaron sin cargo y se recuperan más tarde), sale un bloque con cuántos se
generaron, cuántos se consumieron y cuántos quedan pendientes. Sirve para que la
gestoría entienda un cobro que ese mes no cuadra con ninguna sesión ni factura:
el dinero entró, la sesión llega después. El importe del crédito solo cuenta una
vez, el mes en que se pagó.

**No aparece el tipo de terapia.** Ni en el recuento de citas ni en el detalle de
cobros: el documento va a un tercero (la gestoría) y cruzar a una persona con una
modalidad de terapia sería darle un dato de salud que no necesita para su trabajo.

**Exportar facturas del mes…** empaqueta en un ZIP todas las facturas emitidas
ese mes, cada una en su propio PDF, para adjuntarlas al resumen que se manda a la
gestoría. Si el mes no tiene ninguna factura emitida, avisa en vez de dar un ZIP
vacío.

**Exportar a PDF…** lo saca ya con los datos fiscales y el logotipo, listo para
enviarlo.

### Subir a Drive para la gestoría

**Subir a Drive para la gestoría** deja el resumen del mes y cada factura en su
PDF en una carpeta de tu Google Drive: `Bitácora · Gestoría`, con una carpeta por
año y dentro una por mes (`09 septiembre`). Así no hace falta exportar y mandar
nada: la gestoría lo encuentra allí.

- **Compártela una sola vez**, desde Drive: botón derecho sobre
  `Bitácora · Gestoría` → Compartir, y escribe la dirección de la gestoría.
  **Nunca** con «cualquiera que tenga el enlace»: estos PDF van legibles, no
  cifrados como las copias.
- **Se puede repetir.** Si después rectificas una factura de ese mes, vuelve a
  pulsarlo: la carpeta del mes se sustituye entera por lo que dice la aplicación
  ahora. La factura rectificada va también, cruzada por «SIN EFECTO».
- **Se borra sola.** Cada vez que subes, la aplicación borra de Drive los años que
  ya pasan el plazo de conservación (seis desde que terminó cada año). Confírmalo
  con tu gestoría.

Antes de usarlo, activa la verificación en dos pasos en tu cuenta de Google: con
estos papeles en Drive, esa cuenta pasa a protegerlos.

### Gastos

Los gastos de la consulta: alquiler, cuota del colegio, seguro, material…
**Anotar gasto** abre una ventana con el concepto, el importe y la fecha; se
rellena y se pulsa **Anotar**. La fecha se propone dentro del mes que se está
mirando; si se elige una de otro mes, el gasto va a ese mes y la aplicación
avisa de dónde ha ido. Si falta algo, la ventana no se cierra y dice qué falta.
La **papelera** de cada fila quita el gasto.

Por ahora los gastos solo se ven aquí: el PDF para la gestoría sigue llevando
solo los cobros.

### Balance

Arriba, lo cobrado, lo gastado y el balance del mes elegido. Debajo, el **año
mes a mes** con las mismas tres cifras y el total del año, con el mes elegido en
negrita. Un balance negativo sale en rojo.

---

## 10. Cosas que conviene saber

**No mover la carpeta de datos a Drive, OneDrive ni Dropbox.** La aplicación lo
impide a propósito: la sincronización continua corrompe la base de datos. A la
nube van las copias, que para eso están.

**El registro de accesos** (Administración → Ver el registro…) deja constancia
de cada consulta y cada cambio en una historia clínica. Es una obligación legal
y solo se puede mirar, no borrar.

**Suprimir una ficha** no la borra: deja de tratarse y se borran teléfono y
correo de inmediato, pero los datos se conservan **cinco años**, que es el
mínimo que exige la Ley 41/2002. Ese plazo se cuenta desde el **cierre del
último caso** de la persona (por eso hay que cerrarlos antes de suprimir), no
desde el día de la supresión. Pasado el plazo, **Destruir las caducadas** en
Administración las elimina de verdad: se van los datos identificativos, la
historia clínica, los informes, el material de trabajo y **los documentos de sus
consentimientos**, que son los que llevan dentro su nombre, su DNI y su firma. De
cada consentimiento queda solo el rastro —cuándo se firmó y qué versión—, marcado
como «documento destruido», que ya no identifica a nadie y sigue demostrando que
se consintió. Las facturas no se van: tienen su propio plazo fiscal.

**Bloqueo por intentos.** Cinco contraseñas fallidas seguidas bloquean el
acceso un rato. Es a propósito. Los códigos de verificación fallidos cuentan
igual.
