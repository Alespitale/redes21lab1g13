
# Tarea Estrella

Los IDN (Internationalized Domain Names) pueden crearse con ayuda de Unicode, un estándar de codificación con más de 120.000 caracteres procedentes de docenas de scripts y conjuntos de símbolos. 

Hoy en día, prácticamente todos los navegadores soportan Unicode y los IDN hacen posible que la mayoría de caracteres que no sean ASCII puedan visualizarse en el repertorio de caracteres Unicode como secuencias de caracteres compatibles con ASCII. Debido a que el estándar Unicode más actual también contiene muchos emojis, esto abre la puerta a los dominios que contienen emojis.

El sistema de nombres de dominio (DNS) utiliza una cantidad limitada de los ya de por sí restringidos caracteres ASCII.
El mecanismo utilizado para traducir un nombre de dominio que contenga caracteres Unicode complejos es Punycode. 

Punycode es una sintaxis de codificación usada en programación que usa una cadena Unicode que puede ser traducida en una cadena de caracteres más limitada compatible con los nombres de red. 

Un string de Punycode está formado por letras de la A a la Z, cifras entre el 0 y el 9 y el símbolo del string. Debido a que la traducción tiene lugar en el navegador web y no en el DNS, los IDN funcionan sin necesidad de hacer cambios. Por lo tanto, tras la conversión a Punycode, los caracteres se pueden convertir en un URL, creando asi la posibilidad de registrar un dominio con un emoji.

## ¿Como lo hace?

Veamos un ejemplo IDN: azulejos-coruña

El IDN azulejos-coruña contiene la letra “ñ”, no incluida dentro de los caracteres antes permitidos para los nombres de dominio y que, por lo tanto, debe codificarse mediante Punycode para garantizar la compatibilidad.

En el primer paso, el proceso de codificación prevé una normalización de la cadena de caracteres de salida (así, todas las letras mayúsculas se sustituyen por minúsculas).

En el segundo paso, se eliminan todos los caracteres no ASCII, sustituyéndolos en el dominio por su forma codificada y separándose por un guion.

Al codificar direcciones de Internet con Punycode, cada cadena resultante va acompañada del prefijo ACE (abreviatura de ASCII Compatible Encoding):

Prefijo ACE: xn--

El prefijo ACE garantiza que los nombres de dominio que contienen guiones no sean interpretados erróneamente como nombres de dominio internacionales.

Finalmente, como resultado codificado para azulejos-coruña se obtiene:

ACE: xn--azulejos-corua-2nb


## Referencias:

<https://www.ionos.es/digitalguide/dominios/noticias-sobre-dominos/registro-de-dominios-con-emojis-como-funciona/>
<https://www.ionos.mx/digitalguide/dominios/gestion-de-dominios/punycode/>
<https://es.wikipedia.org/wiki/Punycode>
[Convertidor](https://www.punycoder.com/)
