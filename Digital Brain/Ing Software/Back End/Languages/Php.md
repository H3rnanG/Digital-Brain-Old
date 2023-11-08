#EngineeringSoftware
# Conceptos Basicos
## Que es php?
PHP es un lenguaje de programación de código abierto y de propósito general que se utiliza principalmente para el desarrollo web del lado del servidor. Fue creado originalmente en 1994 por Rasmus Lerdorf como un conjunto de scripts de Perl para la gestión de su propio sitio web personal. A lo largo de los años, PHP ha evolucionado en un lenguaje de programación completo y ha sido ampliamente adoptado en el desarrollo de aplicaciones web.

PHP es especialmente adecuado para el desarrollo de aplicaciones web dinámicas y basadas en bases de datos, ya que permite la interacción con servidores de bases de datos y la generación de contenido HTML y otros formatos de salida en tiempo real. También es fácil de integrar con otros lenguajes de programación, como HTML, CSS, JavaScript y otros, lo que lo convierte en una herramienta muy útil para el desarrollo de sitios web complejos.

PHP se ejecuta en un servidor web y su código se procesa en el servidor, lo que significa que los usuarios que acceden a una página web basada en PHP solo ven el resultado de la ejecución del código, no el código fuente en sí. Además, PHP es un lenguaje de programación de código abierto, lo que significa que su código fuente es libremente disponible y se puede modificar y distribuir libremente.
# Php Basico
## Variables:
Una variable es un espacio de memoria reservado en un programa de computadora para almacenar un valor. Para definir variables en php se necesita el caracter *''$''*.
```php
# String
$variableString = 'Texto';
# Numericas
$variableNumerica = 18;
```

## Constantes:
Una constante es similar a una variable en que también es un espacio de memoria reservado para almacenar un valor en un programa de computadora. La diferencia principal es que una constante es un valor que no puede ser modificado una vez que se ha definido durante la ejecución del programa. Para definir variables en php usa la palabra reservada *''define( )''*.
```php
# Es un buena practica escribir todas las constantes en MAYUSCULA
define('PI',3.1416);
# Para Imprimirla no necesitas el $
echo PI;
```

## Arreglo Indexado:
Un arreglo, también conocido como matriz o vector, es una estructura de datos en programación que permite almacenar y manipular una colección de elementos del mismo tipo. 
Para definir variables en php usa la palabra reservada *''array( )''* o solo usar *"[ ]"*.
```php
$arregloArray = array('Valor1',123,true,['Otro Arreglo',456]);
$arregloNormal = ['Valor1',123,true,['Otro Arreglo',456]];

echo arregloNormal[0];
# Esto devuelve: Valor1
```

## Arreglo Asociaivo:
Un arreglo asociativo es un tipo especial de arreglo en programación donde cada elemento se identifica por una clave o nombre en lugar de un índice numérico. A diferencia de los arreglos indexados tradicionales, los arreglos asociativos permiten acceder a los elementos utilizando una clave alfanumérica en lugar de un índice numérico.
Para definir variables en php usa la palabra reservada *''array( )''* o solo usar *"[ ]"*.
```php
$arregloArray = array('ValorString' => 'String','ValorNumero' => 123, 
					  'Valor Boleano' => true);
$arregloNormal = ['ValorString' => 'String','ValorNumero' => 123, 
					'Valor Boleano' => true];
echo arregloNormal['ValorString'];
# Esto devuelve: String
```

## Arreglo Multidimensionales:
Un arreglo asociativo es un tipo especial de arreglo en programación donde cada elemento se identifica por una clave o nombre en lugar de un índice numérico. A diferencia de los arreglos indexados tradicionales, los arreglos asociativos permiten acceder a los elementos utilizando una clave alfanumérica en lugar de un índice numérico.
Para definir variables en php usa la palabra reservada *''array( )''* o solo usar *"[ ]"*.
```php
$ArregloMultidimensional = [
	['Valor 1','Valor 2'],
	[12345,67890],
	[true,false]
]
echo arregloNormal[0][1]; #Acceder al primer valor del primer array
echo arregloNormal[1][1]; #Acceder al segundo valor del segundo array
#Esto devuelve: Valor1
			   #12345 
```

## Funcion count( ):
Para contar los elementos de un arreglo se usa la palabra reservada *"count( )"*.
```php
$meses = ['January','February','March','April','May','June',
		  'July','August','September','October','November','December']
$numeroMeses = count($meses);
echo $numeroMeses
# Esto devuelve: 12
```

## Funcion sort( ) y rsort( ):
Para ordenar los elementos de un arreglo se usa la palabra reservada *"sort( )"* o *"rsort( )"*.
```php
$meses = ['January','February','March','April','May','June',
		  'July','August','September','October','November','December']
$mesesOrdenados = sort($meses);
# Si lo iteramos con un forEach devolveria: April, August, ...
$mesesOrdenadosInverso = rsort($meses);
# Si lo iteramos con un forEach devolveria: September, October, ...
```

## Condicionales:
Las condicionales son una estructura de control en programación que permite que un programa tome decisiones basadas en una condición específica. Las condicionales permiten que un programa ejecute diferentes bloques de código según el resultado de una prueba o evaluación.
##### Condicional ' If '
Si la condicion es VERDADERA se ejecutara el codigo dentro de las llaves.
```php
if (Condicion)
{
	#Codigo que se ejecutara si la condicion es Verdadera
}
```

##### Condicional ' else '
Si la primera condicion no es VERDADERA se ejecutar el bloque de codigo dentro de *"Else"*.
```php
if (Condicion)
{
	#Codigo que se ejecutara si la condicion es VERDADERA
}
else 
{
	#Codigo que se ejecutara si la condicion es FALSA
}
```

##### Condicional ' else if '
Si la primera condicion no es VERDADERA se verificara si la siguiente condicion si es VERDADERA las veces que haya un *"Else if"*.
```php
if (Condicion)
{
	#Codigo que se ejecutara si la condicion es VERDADERA
}
else if (Condicion_2)
{
	#Codigo que se ejecutara si la Condicion es FALSA y la Condicion_2 es VERDADERA
}
else if (Condicion_3)
{
	#Codigo que se ejecutara si la Condicion2 es FALSA y la Condicion_3 es VERDADERA
}
else 
{
	#Codigo que se ejecutara si todas las condiciones anteriores son FALSAS
}
```


## Operadores:
Los operadores son símbolos o palabras reservadas que se utilizan en programación para realizar operaciones matemáticas, lógicas o de comparación entre valores o variables.
##### Operadores Aritmeticos:
```php
$variableSuma = 10 + 2 # 12
$variableResta = 10 - 7 # 3
$variableMultiplicacion = 10 * 2 # 20
$variableDivision = 10 / 2 # 5
$variableModulo = 10 % 3 # 1
```

##### Operadores de Asignacion:
```php
$variableAsignada = 10
# Suma
$variableAsignada += 2 # 10 + 2
# Resta
$variableAsignada -= 2 # 10 - 2
# Multiplicacion 
$variableAsignada *= 2 # 10 * 2
# Division 
$variableAsignada /= 2 # 10 / 2
```

##### Operadores de Comparacion:
```php
$variable = 10 == '10' #true
$variable = 10 === '10' #false 
$variable = 10 != '10' #true 
$variable = 10 !== '10' #true 
# y tambien estan: < , > , <= , >= 
```

##### Operadores Logicos 
```php
# El and necesita que las dos condiciones sean verdaderas para ejecutar el codigo
if (condicion && condicion_2) { /*Condicion*/ } 
# El or necesita que una de las condiciones sean verdaderas para ejecutar el codigo
if (condicion || condicion_2) { /*Condicion*/ } 
# El xor necesita que una de las condiciones sean verdaderas para ejecutar el codigo
# si las dos condiciones son verdaderas el resultado sera falso
if (condicion xor condicion_2) { /*Condicion*/ } 
# El not necesita que no se cumpla la condicion para ejecutar el codigo
if (!condicion_2) { /*Condicion*/ } 
```

## Switch:
la estructura de control "switch" se utiliza para tomar decisiones basadas en el valor de una expresión. Su estructura es:
```php
switch ($variable) 
{
	case valor1:
		# Código a ejecutar si $variable es igual a valor1
		break;
	case valor2: 
		# Código a ejecutar si $variable es igual a valor2 
		break;
	
	default: 
		// código a ejecutar si $variable no coincide con ningún valor break;
}
```
## ShortHand:
```php
# Con isset verificamos si una variable contiene algun valor, 
# si es asi devolvera true
isset($variable)
# Ahora si el ShortHand
(Condicion) ? /*Ejecutar si es True*/ : /*Ejecutar si es False*/;
```
## Ciclo For:
El ciclo "for" es una estructura de control que se utiliza para ejecutar un bloque de código repetidamente un número específico de veces. La sintaxis básica del ciclo "for" es la siguiente:
```php
for (incializacion, condicion, incremento/decremento) 
{
	# Código a ejecutar en cada iteración del ciclo
}
# Un ejemplo:
for ($i = 1; $i <= 10; $i++) 
{ 
	echo $i . " "; 
}
```

## Ciclo While:
El ciclo "while" es una estructura de control que se utiliza para ejecutar un bloque de código repetidamente mientras se cumple una condición determinada. La sintaxis básica del ciclo "while" es la siguiente:
```php
while (condición) 
{ 
	# código a ejecutar en cada iteración del ciclo 
}
# Un ejemplo:
$i = 1; 
while ($i <= 10) 
{
	echo $i . " "; $i++; 
}
```

## Ciclo Do While:
El ciclo "do while" es una estructura de control que es similar al ciclo "while", pero con una diferencia importante: el bloque de código dentro del ciclo se ejecuta al menos una vez, independientemente de si se cumple o no la condición especificada.
La sintaxis básica del ciclo "do while" es la siguiente:
```php
do 
{ 
	// Código a ejecutar en cada iteración del ciclo 
} while (condición);
# Un ejemplo:
$i = 1; 
do 
{ 
	echo $i . " "; $i++; 
} while ($i <= 10);
```


## Ciclo For Each:
El ciclo "foreach" es una estructura de control que se utiliza para iterar sobre los elementos de un arreglo (array) o de un objeto. Es una forma simplificada de recorrer los elementos de una lista sin necesidad de utilizar un ciclo "for" tradicional.
La sintaxis básica del ciclo "foreach" es la siguiente:
```php
foreach ($arreglo as $valor) 
{ 
	# Código a ejecutar en cada iteración del ciclo 
}
# Un ejemplo:
$numeros = array(1, 2, 3, 4, 5); 
foreach ($numeros as $numero) 
{ 
	echo $numero . " "; 
}
```

## Sentencias Break y Continue:
La sentencia "break" se utiliza para salir inmediatamente de un ciclo cuando se cumple cierta condición. Cuando se ejecuta la sentencia "break", el control del programa sale del ciclo y continúa ejecutando el código que sigue después del ciclo. La sintaxis básica es la siguiente:
```php
for ($i = 1; $i <= 10; $i++) 
{ 
	if ($i == 5) 
	{ 
		break; 
	} 
	echo $i . " "; 
}
```

Por otro lado, la sentencia "continue" se utiliza para saltar a la siguiente iteración de un ciclo cuando se cumple cierta condición. Cuando se ejecuta la sentencia "continue", el control del programa salta al inicio del ciclo y continúa con la siguiente iteración. La sintaxis básica es la siguiente:
```php
for ($i = 1; $i <= 10; $i++) 
{ 
	if ($i % 2 == 0) 
	{ 
		continue; 
	} 
	echo $i . " "; 
}
```

## Funcion var_dump( ):
Esta funcion nos muestra informacion acerca de una variable.
```php
var_dump($variable);
```

## Funcion print_r( ):
Esta funcion nos muestra informacion acerca de una variable pero mas facil de leer.
```php
print_r($variable);
```
## Funciones:
Las funciones son bloques de código que se pueden llamar varias veces en un programa. Las funciones pueden aceptar parámetros y devolver valores, lo que permite a los programadores reutilizar código y hacer que sus programas sean más modulares y fáciles de mantener.
```php
function nombre_de_la_funcion($parametro1, $parametro2, ...) 
{ 
	// código a ejecutar return $valor; 
}
```

## Sentencia return:
La sentencia `return` se utiliza para devolver un valor desde una función. Cuando se llama a una función que contiene la sentencia `return`, el valor devuelto por la función puede ser asignado a una variable o utilizado en otra parte del programa.
```php
function nombre_de_la_funcion($parametro1, $parametro2, ...) 
{ 
	return $valorRetornado;
	
}
```

## Funciones utiles para Strings:
### htmlspecialchars( ):
Protege y vuelve caracteres especiales a html para impedir injecciones.
```php
$variable = '< > && " "';
htmlspecialchars($variable);
```
### trim( ):
Elimina todos los espacios en blanco al inicio y al final de un string.
```php
$variable = '     Hola     ';
trim($variable); # Hola
```
### strlen( ):
Cuenta el numero de caracteres dentro de un string.
```php
$variable = 'Hola';
strlen($variable); # 4
```
### substr( ):
Permite retornar un pedaso de una linea de una cadena de texto.
```php
$variable = 'Hola Mundo';
substr($variable,0,4); # Hola 
```
##### strtoupper( ) y strtolower( ):
Convierte todo el string en mayusculas o minusculas.
```php
$variable = 'Hola Mundo';
strtolower($variable); # hola mundo
strtoupper($variable); # HOLA MUNDO
```

##### strpos( ):
Retorna la posicion de un caracter en especifico.
```php
$variable = 'Hola Mundo';
strpos($variable,'a'); # 3
```

## Funciones utiles para Arrays:
##### extract( ):
Extrae todos los valores de un array.
```php
$array = [
		'campo1' => 'string1',
		'campo2' => 12345
];

extract($array);
echo $campo1 # string1
```

##### array_pop( ):
Elimina o extrae el ultimo valor de un array.
```php
$array = [
		'campo1' => 'string1',
		'campo2' => 12345
];

$ultimoValor = array_pop($array);
# o tambien solo lo puedes eliminar
array_pop($array);
```

### join( ) y implode( ):
Divide todos los valores de una array con lo que especifiquemos.
```php
$array = ['valor1','valor2','valor3'];

echo join(', ',$array); # valor1, valor2, valor3
echo implode(' - ',$array); # valor1 - valor2 - valor3
```
### array_reverse( ):
Invierte el array que especifiquemos.
```php
$array = ['valor1','valor2','valor3'];

array_reverse($array);
echo join(', ',$array); # valor3, valor2, valor1
```
### stripslashes( ):
La función `stripslashes()` en PHP elimina las barras invertidas (`\`) de una cadena.
## Funciones Matematicas:
### round( ):
Nos permite redondear un numero o especificar en numero de decimales:
```php
$numero = 15.781;
echo round($numero); #16
echo round($numero,2); #15.78
```

### rand( ):
Nos retorna un numero aleatorio entre valores que especifiquemos.
```php
echo rand(1,10); # Obtenemos un numero aleatorio del 1 al 10
```

### ceil( ):
Nos permite redondear un numero hacia el numero siguiente:
```php
$numero = 15.1;
echo ceil($numero); #16
```

## Scope de php:
En PHP, el "scope" o ámbito de una variable se refiere a la parte del programa donde se puede acceder a dicha variable. Una variable puede tener diferentes ámbitos dependiendo de cómo se declare. En PHP, existen tres tipos de ámbitos:

1.  *Global:* Las variables globales pueden ser accedidas desde cualquier parte del programa, incluyendo dentro de funciones y clases. Para declarar una variable global en PHP, se utiliza la palabra clave `global` seguida del nombre de la variable:
```php
$variable_global = "Hola";

function imprimir_mensaje() {
  global $variable_global;
  echo $variable_global;
}

imprimir_mensaje(); // imprime "Hola"
```
En este ejemplo, la variable `$variable_global` se declara fuera de la función y luego se utiliza dentro de la función `imprimir_mensaje()` mediante la palabra clave `global`.

2.  *Local:* Las variables locales solo pueden ser accedidas dentro de la función o bloque de código donde se declaran. Las variables locales se declaran sin ninguna palabra clave especial:
```php
function imprimir_mensaje() {
  $mensaje = "Hola";
  echo $mensaje;
}

imprimir_mensaje(); // imprime "Hola"
```
En este ejemplo, la variable `$mensaje` solo puede ser accedida dentro de la función `imprimir_mensaje()`.

3.  Estático: Las variables estáticas son similares a las variables locales, pero su valor se mantiene entre llamadas a la función. Las variables estáticas se declaran utilizando la palabra clave `static`:
```php
function contar_llamadas() {
  static $contador = 0;
  $contador++;
  echo "Esta es la llamada número " . $contador;
}

contar_llamadas(); // imprime "Esta es la llamada número 1"
contar_llamadas(); // imprime "Esta es la llamada número 2"
contar_llamadas(); // imprime "Esta es la llamada número 3"
```
En este ejemplo, la variable `$contador` se declara como estática dentro de la función `contar_llamadas()`, lo que significa que su valor se mantiene entre llamadas a la función.
## Include y Require:
-   `include` intenta incluir el archivo especificado, y si no lo encuentra, emite una advertencia y continúa la ejecución del script.
-   `require`, por otro lado, intenta incluir el archivo especificado, y si no lo encuentra, emite un error fatal y detiene la ejecución del script.
```php
# include
include 'direccion del archivo';
# required
require 'direccion del archivo';
```
## Funcion die( ):
Esta funcion corta o termina la ejecucion del programa.
```php
echo 'Hola Mundo';
die();
echo 'Adios Mundo' # Esta ni las siguientes lineas de codigo se ejecutaran
```
## Declaracion de Tipo Escalar:
Las declaraciones de tipo escalar (también conocidas como tipado fuerte o type hinting) en PHP permiten especificar el tipo de dato que se espera para los parámetros y valores de retorno de una función.
Por ejemplo, si se define una función que espera un parámetro de tipo entero y devuelve un valor de tipo cadena, se puede hacer una declaración de tipo escalar para asegurarse de que solo se pasen valores de tipo entero y que el valor de retorno sea una cadena:
```php
declare(strict_types=1); # Declaramos que la aplicacion sea estrica
function sumar(int $a, int $b){
  return 'El resultado es: ' . ($a + $b);
}
```
En este ejemplo, `$a` y `$b` son parámetros de tipo entero, y la función devuelve una cadena que contiene el resultado de la suma de los dos números.
## Declaraciones de Tipo Devolucion:
Son exactamente lo mismo que las [[#Declaracion de Tipo Escalar:]] pero donde nos permiten que tipo de dato queremos regresar.
```php
declare(strict_types=1); # Declaramos que la aplicacion sea estrica
function sumar(int $a, int $b) : int{
  return 'El resultado es: ' . ($a + $b);
}
```
## Operador de Nave Especial:
El operador de nave espacial (`<=>`) en PHP es un operador de comparación que se introdujo en PHP 7. Este operador devuelve un valor entero negativo, cero o positivo, según si el valor del operando izquierdo es menor que, igual a o mayor que el valor del operando derecho. La sintaxis del operador de nave espacial es la siguiente:
```php
$a <=> $b
```
Donde `$a` y `$b` son los valores que se quieren comparar.
El resultado de la comparación será:

-   `-1` si `$a` es menor que `$b`
-   `0` si `$a` es igual a `$b`
-   `1` si `$a` es mayor que `$b`
# Formularios
## Enviar datos por el metodo POST:
`POST` es uno de los métodos HTTP que se utilizan para enviar datos de un formulario HTML desde el cliente (como un navegador web) al servidor (donde se ejecuta un script PHP). Podemos acceder al valor del campo en un script PHP de la siguiente manera:
```php
$variable = $_POST('NameEtiqueta');
```

## Enviar datos por el metodo GET:
`GET` es uno de los métodos HTTP que se utilizan para enviar datos desde el cliente (como un navegador web) al servidor (donde se ejecuta un script PHP). Podemos acceder al valor del campo en un script PHP de la siguiente manera:
```php
$variable = $_GET('NameEtiqueta');
```

## Enviar datos a la misma pagina:
Para enviar datos a la misma pagina en php puedes dejar el campo action de tu formulario vacio e implementar toda la logica en el mismo archivo, tambien puedes escribir el nombre del mismo archivo o tambien podemos usar el *"$_SERVE[]"*.
```php
<form action="" method="metodo de envio">
	Etiquetas del formulario...
</form>

<form action="nombreArchivo.php" method="metodo de envio">
	Etiquetas del formulario...
</form>

<form action="<?php echo htmlspecialchars($_SERVER['PHP_SELF']);?>" method="metodo de envio">
	Etiquetas del formulario...
</form>
```

## Comprobar si un formulario se envio:
Para verificar que tipo de envio se realizo en el formulario es *"$_SERVER['REQUEST_METHOD']"*.
```php
if($_SERVER['REQUEST_METHOD'] == 'GET')
{
	#Codigo a ejecutar si se envio por GET.
} else 
{
	#Codigo a ejecutar si se envio por POST.
}
```
O tambien podemos usar la palabra reservada *"isset"*.
```php
if(isset($_POST['NamedelSubmit'])
{
	#Codigo a ejecutar si se envio por Submit.
} else 
{
	#Codigo a ejecutar si se entro a la pagina por url.
}
```

## Validando Formularios:
### Funcion filter_var:
`filter_var()` en PHP se utiliza para filtrar una variable con un filtro especificado.
Los filtros son funciones predefinidas que se utilizan para validar y sanear datos de entrada. Estos filtros se pueden utilizar para validar direcciones de correo electrónico, direcciones IP, números de teléfono, URLs, etc. También se pueden utilizar para sanitizar cadenas, como por ejemplo, eliminando caracteres no válidos o peligrosos.
La sintaxis de la función `filter_var()` es la siguiente:
```php
filter_var($variable, $filtro, $opciones);
```
donde:
-   `$variable`: la variable que se va a filtrar
-   `$filtro`: el tipo de filtro que se aplicará a la variable
-   `$opciones`: parámetros adicionales que se pueden pasar al filtro (opcional)

El filto que utilizariamos seria el *"FILTER_SANITIZE_FULL_SPECIAL_CHARS"*.
```php
$variable = filter_var($variable, FILTER_SANITIZE_FULL_SPECIAL_CHARS);
```


### Hay un Ejemplo de un Formulario en:
La direccion *"C:\laragon\www\Engineering Software\BackEnd\Php\Formularios\Practica"*.
# Programacion Orientada a Objetos
#### Que es la POO:
La programación orientada a objetos (POO) en PHP es un paradigma de programación que se basa en la creación de objetos que interactúan entre sí para realizar tareas. En POO, los objetos son instancias de clases, que son plantillas que definen las propiedades y métodos de los objetos. Para definir una clase se usa la palabra reservada *"class"*.
```php
class NombreClase
{
	# Atributos
	# Metodos()
}
```

## Palabra reservada This:
En PHP, la palabra reservada "this" se utiliza dentro de una clase para hacer referencia al objeto actual. Es una variable que se refiere al objeto en el que se está ejecutando el método en el que se utiliza la palabra reservada "this".

Cuando se utiliza la palabra reservada "this" dentro de un método de una clase, se puede acceder a las propiedades y métodos del objeto actual. Por ejemplo, si se tiene una clase llamada "Persona" con una propiedad llamada "nombre", se puede acceder a esta propiedad utilizando "this->nombre" dentro de un método de la clase.
```php
class Persona
{
	public $nombre;
	public $edad;

	public function () {
		echo $this->nombre;
	}
}
```

## Metodo Constructor:
El método constructor en PHP es un método especial de una clase que se ejecuta automáticamente cuando se crea un objeto a partir de esa clase. Su función es inicializar las propiedades del objeto y realizar cualquier otra tarea de configuración necesaria.

El método constructor se define dentro de la clase utilizando el nombre *"`__construct.`"* Por ejemplo, si se tiene una clase llamada "Persona", se podría definir su constructor de la siguiente manera:
```php
class Persona { 
	public $nombre; 
	public $edad; 
	public function __construct($nombre, $edad) 
	{ 
		$this->nombre = $nombre; 
		$this->edad = $edad; 
	} 
}
```

## Herencia:
La herencia en PHP es un concepto de la programación orientada a objetos que permite definir una nueva clase basada en una clase existente, y heredar todas sus propiedades y métodos. La clase original se conoce como la clase base o superclase, y la nueva clase se conoce como la clase derivada o subclase.

Para crear una clase derivada en PHP, se utiliza la palabra clave "extends", seguida del nombre de la clase base. Por ejemplo, si se tiene una clase llamada "Persona" y se quiere crear una clase derivada llamada "Empleado", se podría hacer de la siguiente manera:
```php
class Empleado extends Persona {
   public $sueldo;
   function __construct($nombre,$edad,$sueldo)
   {
	   parent::__contruct($nombre,$edad);
	   # parent hace referencia a esto ->
	   /* 
		$this->nombre = $nombre; 
		$this->edad = $edad; 
	   */
	   $this->sueldo = $sueldo;
   }
   public function calcularSueldo() {
      // método para calcular el sueldo del empleado
   }
}
```


## Clases Abstractas:
Una clase abstracta en PHP es una clase que no puede ser instanciada directamente, sino que solo puede ser utilizada como base para otras clases. Es decir, una clase abstracta proporciona una plantilla o modelo para otras clases que se basan en ella.

Para definir una clase abstracta en PHP, se utiliza la palabra clave *"`abstract`"* antes del nombre de la clase. Además, al menos un método en la clase debe ser definido como abstracto, utilizando la misma palabra clave "abstract" antes de su declaración.
```php
abstract class Figura {
   protected $nombre;
   public function __construct($nombre) {
      $this->nombre = $nombre;
   }
   abstract public function calcularArea();
}

class Cuadrado extends Figura {
   private $lado;
   public function __construct($nombre, $lado) {
      parent::__construct($nombre);
      $this->lado = $lado;
   }
   public function calcularArea() {
      return $this->lado * $this->lado;
   }
}

class Circulo extends Figura {
   private $radio;
   public function __construct($nombre, $radio) {
      parent::__construct($nombre);
      $this->radio = $radio;
   }
   public function calcularArea() {
      return pi() * $this->radio * $this->radio;
   }
}
```

## Palabra Reservada Static:
En PHP, la palabra reservada "static" se utiliza para definir propiedades y métodos de clase que son compartidos por todas las instancias de la clase, en lugar de pertenecer a una instancia específica.

Cuando se define una propiedad o método como "static", esta propiedad o método puede ser accedido directamente desde la clase, sin necesidad de crear una instancia de la misma. Por ejemplo:
```php
class Persona {
   public static $contador = 0;
   public function __construct() {
      self::$contador++;
   }
   public static function getContador() {
      return self::$contador;
   }
}
	
$persona1 = new Persona();
$persona2 = new Persona();
echo Persona::getContador(); // Imprime 2

```

# Sessions y Cookies
## Sesiones
Las sesiones en PHP son una forma de mantener información de una sesión de usuario específica a través de varias páginas web. Una sesión es un conjunto de interacciones entre el usuario y una aplicación web que ocurren en un período de tiempo específico.

Cuando un usuario inicia una sesión en una aplicación web PHP, se genera un identificador de sesión único que se utiliza para mantener información de la sesión. Esta información se almacena en el servidor web y se asocia con el identificador de sesión único.

Para iniciar una sesión en PHP, se utiliza la función "session_start()". Esta función debe ser llamada al principio de cada página que utilice variables de sesión. Por ejemplo:
```php
<?php
session_start();
$_SESSION['nombre'] = 'Juan';
$_SESSION['edad'] = 30;

# Para cerrar sesion se usa:
session_destroy();
?>
```
## Cookies
En PHP, las cookies son pequeños archivos de texto que se almacenan en el navegador del usuario para recordar información sobre el usuario o sus preferencias.

Las cookies son útiles para recordar información como el nombre de usuario y la contraseña, el idioma preferido del usuario, la ubicación geográfica del usuario y la información del carrito de compras. Las cookies se pueden utilizar para rastrear la actividad del usuario y personalizar la experiencia del usuario en un sitio web.

Para crear una cookie en PHP, se utiliza la función "setcookie()", que toma varios parámetros como nombre, valor, tiempo de expiración, dominio y ruta de la cookie. Por ejemplo:
```php
setcookie('nombreCookies', 'ValorCookie', time() + (86400 * 30), '/carpetaDondeEstaraDisponiblelaCookie');
# para que este disponible en todo el dominio solo remplaza por '/'

# Para acceder a una cookie
$variable = $_COOKIE['nombreCookies'];

#Para eliminar una cookie: cambiar el tiempo a uno menor al actual, solo remplaza el signo '+' por '-'
```
# Mysql
## Conectar la Base de Datos:
Crear una instancia de la clase PDO, especificando el nombre de la base de datos, el nombre de usuario y la contraseña en los parámetros del constructor. Por ejemplo:
```php
$dsn = 'mysql:host=localhost;dbname=nombre_de_la_base_de_datos';
$username = 'nombre_de_usuario';
$password = 'contraseña';

try {
    $conexion = new PDO($dsn, $username, $password);
} catch (PDOException $e) {
    echo 'Error al conectar a la base de datos: ' . $e->getMessage();
}
```

## Ejecutando Consultas por Query:
Se pueden ejecutar consultas de SQL utilizando el método "query()".
```php
$resultadosConsulta = $conexion->query('Consulta');
```

## Ejecutando Consultas por Prepare:
Se pueden ejecutar consultas de SQL utilizando el método "prepare()".
```php
$statement = $conexion->prepare('Consulta'); # No se ejecuta,solo se guarda
$statement->execute(); # Ahora si se ejecuta
```

Tambien podemos ejectuar las consultas de una forma en la que podamor remplazar los valores de la consulta en el metodo *"execute()"*.
```php
$id = 2

$statement = $conexion->prepare('Consulta where ID = :valor'); # No se ejecuta,solo se guarda
$statement->execute(
	array(':valor' => $id) # Tambien puede ir un valor directamente
); # Ahora si se ejecuta
```

# Postgresql
## Conectar la Base de Datos:
Para conectar una base de datos con postgresql se una la funcion *"pg_connect( )"*. 
Por ejemplo:
```php
$conexion = pg_connect("host=localhost dbname=mi_base_de_datos user=mi_usuario password=mi_contraseña");
```

## Ejecutando Consultas por Query:
Se pueden ejecutar consultas de SQL utilizando el método *"pg_query( )"*.
```php
$resultado = pg_query($conexion, "CONSULTA SQL");
```

## Almacenando resultado de Consultas:
Existen muchas formas para almacenar los resultados de las consultas sql.
La mas usada seria *"pg_fetch_array( )"*.
```php
$fila = pg_fetch_array($resultado)
```

Estas son las demas funciones:
1.  `pg_query()`: esta función envía una consulta SQL a la base de datos y devuelve un objeto `PgSql\Result` que contiene los resultados.
    
2.  `pg_fetch_assoc()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve un array asociativo que representa una fila del resultado.
    
3.  `pg_fetch_array()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve un array indexado y un array asociativo que representan una fila del resultado.
    
4.  `pg_fetch_row()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve un array indexado que representa una fila del resultado.
    
5.  `pg_fetch_object()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve un objeto que representa una fila del resultado.
    
6.  `pg_fetch_all()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve un array multidimensional que contiene todas las filas del resultado.
    
7.  `pg_fetch_all_columns()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve un array unidimensional que contiene todos los valores de una columna específica del resultado.
    
8.  `pg_num_rows()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve el número de filas en el resultado.
    
9.  `pg_affected_rows()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve el número de filas afectadas por la última operación de inserción, actualización o eliminación.
    
10.  `pg_num_fields()`: esta función toma un objeto `PgSql\Result` como argumento y devuelve el número de columnas en el resultado.

