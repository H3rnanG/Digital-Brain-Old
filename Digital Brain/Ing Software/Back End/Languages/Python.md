#EngineeringSoftware

## Conceptos Básicos
### Que es Python?
Python es un lenguaje de programación de alto nivel, interpretado y de propósito general. Fue creado en 1991 por Guido van Rossum y se ha convertido en uno de los lenguajes más populares en el ámbito de la programación debido a su simplicidad, legibilidad y versatilidad.

Python se destaca por su sintaxis clara y concisa, lo que facilita su aprendizaje y uso. Es un lenguaje interpretado, lo que significa que el código fuente se ejecuta línea por línea mediante un intérprete sin necesidad de compilarlo previamente, lo que agiliza el proceso de desarrollo.

Python es conocido por su amplia gama de bibliotecas y módulos, que ofrecen una gran cantidad de funciones y herramientas para tareas específicas. Estas bibliotecas permiten a los desarrolladores aprovechar soluciones preexistentes, lo que acelera el proceso de desarrollo y hace que Python sea una opción popular en áreas como el análisis de datos, la inteligencia artificial, el aprendizaje automático, el desarrollo web y muchas otras disciplinas.

Una de las características más destacadas de Python es su enfoque en la legibilidad del código y la facilidad de uso. Su filosofía, conocida como "Pythonic", fomenta la escritura de código claro y explícito, lo que facilita la colaboración y el mantenimiento de proyectos a largo plazo.
-- -
## Python Básico
### Variables:
Consta de un espacio en el sistema de almacenaje (memoria principal de un ordenador) y un nombre simbólico (un identificador) que está asociado a dicho espacio.

En `Python` asignamos valores a las variables siguiendo el siguiente formato: 
```python
nombre_variable = valor
x = 1
y = 'Hola'
```

#### Restricciones sobre los nombres de las variables
-   No pueden empezar ni contener carácteres especiales
-   No pueden empezar por números
-   No pueden ser llamadas igual que las palabras claves reservadas en Python
-   No pueden contener espacios

**Observación.** A día de hoy, si los nombres de las variables están compuestos por múltiples palabras, hay 4 formas de escribir dichos nombres:
-   camelCase: `nombreMascota`
-   PascalCase: `NombreMascota`
-   snake_case: `nombre_mascota`
-   kebab-case: `nombre-mascota`

#### Declarando múltiples variables en una sola línea
Se hace del siguiente modo:
```python
age, name = 22, "Maria"
age  # 22
name # Maria
```
--- 
#### Funcion *import*
Antes de explicar en qué consiste la función `import`, hay que definir los siguientes conceptos:
-   **Algoritmo.** Conjunto ordenado de operaciones sistemáticas que permite hacer un cálculo y hallar la solución de un problema.
-   **Función.** Bloque de código con un nombre asociado, que recibe cero o más argumentos como entrada, sigue una secuencia de sentencias, la cuales ejecuta una operación deseada y devuelve un valor y/o realiza una tarea.
-   **Script.** Archivo diseñado para ser ejecutado. Puede contener funciones, programas, etc.
-   **Módulo.** Script que contiene colecciones de funciones, definiciones y declaraciones de `Python`.

Las funciones de un módulo pueden ser importadas. Es aquí donde entra en juego la función `import`.
Por ejemplo, vamos a importar el módulo `math`, del cual hablaremos en futuras secciones de este curso.
De momento, lo que nos interesa saber acerca de este módulo es que es de utilidad a la hora de usar funciones matemáticas (definidas según los estándares de C).
```python
import math
```
Con la línea de código anterior, hemos cargado el módulo de `math`, permitiéndonos así poder trabajar con las funciones que contiene, haciendo uso de la sintaxis `math.funcion()` o `math.variable`.

A la hora de usar funciones de un módulo, puede resultar tedioso tener que poner siempre el nombre del módulo previo a la función. Es por ello que la función `import` nos permite hacer lo siguiente:
```python
import math as mt
```
Con la línea de código anterior, no solo hemos cargado el módulo de `math`, sino que a la hora de usar alguna de sus funiones, ahora podremos usar la sintaxis `mt.funcion()` o `mt.variable`. Es decir, en vez de tener que poner el nombre del módulo, podemos cambiarle el nombre o, como en este caso, usar la abreviatura `mt` (o la que quereamos utilizar), cosa que resulta de mucha utilidad para módulos con nombres muy largos.

Si por el contrario no queremos cargar todo el módulo, sino que simplemente queremos cargar una función o una variable, lo podemos hacer de la siguiente forma:
```python
from math import pi
# Al igual que podíamos modificar el nombre del módulo a la hora de llamarlo, también lo podemos hacer con las funciones y las variables.
from math import pi as numero_pi
```

Si por el contrario quisiésemos cargar más de una función o variable, pero sin necesidad de cargar todo el módulo, lo podríamos hacer del siguiente modo:
```python
from math import pi, log, exp
```
En este caso, la línea de código anterior nos permite acceder a la variable `pi` y las funciones `log()` y `exp()`, todas del módulo `math`, directamente haciendo uso de la sintaxis `pi`, `log()` y `exp()` en vez de tener que usar la sintaxis `math.pi`, `math.log()` o `math.exp()`, respectivamente.

Por último, si quisiésemos cargar todas las funciones del módulo `math` y evitar tener que usar la sintaxis `math.funcion()` o `math.variable`, entonces lo podríamos hacer con la siguiente instrucción:
```python
from math import *
```
-- - 
####
---
## Números
### Tipos de números
-   `int`: número entero
-   `float`: número en coma flotante

Para saber el tipo de dato de un número podemos utilizar la función `type()`
```python
type(5)   # int
type(5.0) # float
type(5.)  # float
```

Podemos indicar el tipo de número que deseamos utilizar con las funciones `int()` y `float()`.
```python
type(int(7.0)) #int
type(int(9.))  #int
type(float(3)) #float
```
--- 
### Operaciones Aritmeticas
Los operadores son símbolos o palabras reservadas que se utilizan en programación para realizar operaciones matemáticas, lógicas o de comparación entre valores o variables.
```python
Suma = 10 + 2           # = 12
Resta = 10 - 7          # = 3
Multiplicacion = 10 * 2 # = 20
Division = 10 / 2       # = 5
```

#### Division Entera o Eucledia
Dados dos números naturales a y b, con b≠0, la división Euclídea de a entre b asocia un cociente q y un resto r, ambos números naturales, que satisfacen
```python
a = b⋅q+r
r < b
```

Para obtener el cociente de la división entera, utilizamos la función `//`
```python
DivisionEntera = 10 // 3 # = 3
```

Para obtener el resto de la división entera, utilizamos la función `%`
```python
Modulo = 10 // 3 # = 1
```

Para calcular la potencia n-ésima de un número, usamos la función `**`
```python
Potencia = 5 ** 3      # = 125
# Para calcular la potencia n-ésima de un número, también podemos usar la función `pow()`
PotenciaPow = pow(5,3) # = 125
```
---
### Numero Complejos
**Observación.** En `Python`, los números complejos se definen en forma binómica y en vez de utilizar una `i`, se utiliza la letra `j` para representar la unidad imaginaria.
```python
z = 2 + 5j # Complex 
```

También podemos definir números complejos en `Python` con la función `complex()`
```python
z = complex(1,-7) # 1-7j
```

Para obtener la parte real, utilizamos el método `.real`
```python
z.real # 1.0
```

Para obtener la parte imaginaria, utilizamos el método `.imag`
```python
z.imag # -7.0
```

Si queremos indicar que la parte imaginaria es 1 o -1, no basta con poner `j` o `-j`, sino que hay que escribir `1j` o `-1j`, siempre que definamos el número complejo en su forma binómica.
Para calcular el conjugado de un número complejo, utilizamos el método `.conjugate()`
```python
z = -2 + 1j
z.conjugate() # (-2-1j)
```

Para calcular el módulo de un número complejo, utilizamos la función `abs()`
```python
z = -2j
abs(z) # 2.0
```

Para calcular el argumento de un número complejo, utilizamos la función `phase()` del paquete `cmath`.
```python
import cmath
cmath.phase(z) #-1.5707963267948966
```

Para pasar de forma binómica a forma polar, usamos la función `polar()` del paquete `cmath`.
```python
z # (-0-2j)
cmath.polar(z) # (2.0, -1.5707963267948966)
```

Para pasar de forma polar a forma binómica, usamos la función `rect()` del paquete `cmath`.
```python
cmath.rect(abs(z), cmath.phase(z)) # (1.2246467991473532e-16-2j)
```
---
####
----
## Strings
**String:** Cadena ordenada de caracteres.
Una variable de tipo string es aquella que guarda un string. Cuando queremos que una variable se trate de una variable de tipo string, `str` en `Python`, a la hora de declararla, el contenido de la variable debe ir o bien entre comillas dobles `" "`, o bien entre comillas simples `' '`.
```python
s1 = "Esto es un string entre comillas dobles"
s2 = 'Esto es un string entre comillas simples'
type(s1) # str
type(s2) # str
```

### Concatenacion de Strings
La concatenación es una operación que une dos o más strings en uno solo.
En `Python`, para concatenar dos variables de tipo string usamos la función `+`.
```python
s1 = "Hola, "
s2 = "Juan"
s1 + s2 # Hola, Juan
```
---
### Repeticion de Strings
La repetición es una operación que repite la variable string tantas veces como indiquemos.
En `Python`, para repetir una variable de tipo string usamos la función `*`. El orden de los factores no altera el producto. Es decir, tanto da usar la sintaxis `num_repeticiones * variable_str` como `variable_str * num__repeticiones`.
```python
s1 = "¿Falta mucho? "
s1 * 5 # ¿Falta mucho? ¿Falta mucho? ¿Falta mucho? ¿Falta mucho? ...
```
---
### Funcion 'print( )'
Hasta ahora, cada vez que mostrábamos strings por pantalla, estos salían entre comillas simples.
La función `print()` nos sirve, entre otras muchas cosas, para mostrar strings por pantalla.
```python
s = "Hello world"
y = 2.0
print(y) # 2.0
print(s) # Hello world
```

Al igual que podíamos concatenar strings con la función `+`, combinando ésta junto con la función `print()` podemos concatenar strings con variables que almacenan strings
```python
name = "Don Pepito"
print("¡Buenos días, " + name + "!") # ¡Buenos días, Don Pepito!
```

**Observación.** Podemos obtener exactamente el mismo resultado utilizando comas (`,`) en vez de la función `+`. Eso sí, después de cada coma se nos añade automáticamente un espacio en blanco que no siempre buscamos, como ocurre a continuación después del resultado de la variable `name`.
```python
name = "Don Pepito"
print("¡Buenos días,", name, "!") # ¡Buenos días, Don Pepito!
```

--- 
### Funcion 'str( )'
Con la función `str()`, podemos concatenar strings y variables de cualquier tipo dentro de un `print()`:
```python
nombre = "María"
edad = 22
print("Mi hermana se llama " + nombre + " y su edad es " + str(edad))
# Mi hermana se llama Maria y su edad es 22
```

---
### Metodo 'format( )'
Existe otra forma de concatenar strings y variables de cualquier tipo dentro de un `print()` y es gracias al método `.format()`. Lo que hay que hacer es indicar con llaves, `{}`, donde queremos situar el resultado de las variables y luego, dentro de los paréntesis del método `.format()`, indicar las variables en su respectivo orden.
```python
nombre = "Ricardo"
numero_gatos = 3
print("Mi abuelo se llama {} y tiene {} gatos".format(nombre, numero_gatos))
# Mi abuelo se llama Ricardo y tiene 3 gatos
```

---
### Substrings
Para acceder a un caracter de una variable string usamos la sintaxis de `[]`
```python
s = "Soy fan de los videojuegos"
s[0] # Primer caracter 's'
s[5] # Sexto caracter 'a'
```

Si precedemos el índice por un `-`, entonces empezamos desde el final
```python
s[-1] # Último elemento 's'
s[-7] # Séptimo elemento empezando por el final 'o'
```

Si queremos acceder a varios caracteres seguidos, podemos utilizar la función `:`
```python
s[4:7] # Del quinto al séptimo 'fan'
s[:7] # Del primero al séptimo 'Soy fan'
s[8:] # Del noveno al final 'de los videojuegos'
```

Si precedemos por `-` al índice de la izquierda de `:` y no ponemos ninguno a su derecha, lo que hacemos es obtener los últimos elementos
```python
s[-10:] # Diez últimos elementos 'ideojuegos'
```

---
### Métodos para trabajar con strings
El método `.lower()` nos transforma el string que indiquemos a minúsculas.
```python
s = "Me ENCANTAN el chocolate y las galletas"
s.lower() # me encantan el chocolate y las galletas
```

El método `.upper()`, por el contrario, lo transforma a mayúsculas.
```python
s.upper() # ME ENCANTAN EL CHOCOLATE Y LAS GALLETAS
```

El método `.count()` cuenta cuántas veces aparece una letra o un string dentro del string al cuál le aplicamos dicho método.
```python
s.count("o") # 2
```

El método `.capitalize()` convierte a mayúscula el primer caracter de un string.
```python
s = "me encanta aprender con udemy"
s.capitalize() # Me encanta aprender con udemy
```

El método `.title()` convierte a mayúscula el primer caracter de cada palabra de un string.
```python
s.title() # Me Encanta Aprender Con Udemy
```

El método `.swapcase()` convierte a mayúscula las minúsculas y viceversa.
```python
s = "Me ENCANTA aprender con Udemy"
s.swapcase() # mE encanta APRENDER CON uDEMY
```

El método `.replace()` reemplaza el caracter (o caracteres) que le indiquemos por el string que queramos.
```python
s = "Los tomberis son buenos"
s.replace("buenos", "malos") # Los tomberis son malos
```

El método `.split()` rompe el string en el caracter que le indiquemos y elimina dicho caracter.
```python
s = "El elefante tiene las orejas muy grandes"
s.split("e") # Rompemos por la letra e minúscula
# ['El ', 'l', 'fant', ' ti', 'n', ' las or', 'jas muy grand', 's']

s.split(" ") # Rompemos por los espacios
# ['El', 'elefante', 'tiene', 'las', 'orejas', 'muy', 'grandes']
```

El método `.strip()` elimina los espacios sobrantes a principio y final del string.
```python
s = "       El elefante tiene las orejas muy grandes        "
s.strip() # El elefante tiene las orejas muy grandes
```

El método `.rstrip()` elimina los espacios sobrantes al final del string.
```python
s.rstrip()
#        El elefante tiene las orejas muy grandes
```

El método `.lstrip()` elimina los espacios sobrantes al principio del string.
```php
s.lstrip()
# El elefante tiene las orejas muy grandes        
```

El método `.find()` busca el caracter que indiquemos y nos devuelve la primera posición en la que aparece.
```python
s = "Este es un curso de Python para hacer en casa o en cualquier lado"
s.find("e") # 3
```

El método `.find()` tiene otros dos parámetros de uso opcional: `start` y `end`, que sirven para indicar donde queremos que empiece la búsqueda y donde queremos que acabe.
```python
s.find("e", 10) # Solamente indicamos start '18'
s.find("e", 30, 40) # Indicamos start y end '35'
```

El método `.index()` busca el caracter que indiquemos y nos devuelve la primera posición en la que aparece.
```python
s = "Este es un curso de Python para hacer en casa o en cualquier lado"
s.index("e") # 3
```

El método `.index()` tiene otros dos parámetros de uso opcional: `start` y `end`, que sirven para indicar donde queremos que empiece la búsqueda y donde queremos que acabe.
```python
s.index("e", 10) # Solamente indicamos start '18'
s.index("e", 30, 40) # Indicamos start y end '35'
```

**Observación.** Observemos que los métodos `.index()` y `.find()` son casi idénticos. El único punto en que difieren es que si el caracter indicado no se encuentra en el string, el método `.index()` arroja error, mientras que `.find()` arroja el índice -1.

El método `.rindex()` busca el caracter que indiquemos y devuelve el último indice en el que fue encontrado.
```python
s.rindex("e") # 58
```
También consta de los dos parámetros de uso opcional: `start` y `end`, que sirven para indicar donde queremos que empiece la búsqueda y donde queremos que acabe.

---
### Otras funciones a tener en cuenta
La función `len()` nos devuelve el número de caracteres del string.
```python
s = "Tengo hambre"
len(s) # 12
```

La función `input()` sirve para que el usuario introduzca un string por consola:
```python
print("Introduce tu nombre: ")
name = input("Nombre: ") 
```

Aquí también nos serán útiles las funciones `int()` y `float()`, pues si en vez del nombre queremos que el usuario nos indique su edad o su altura, querremos tratar dichos valores como números. Entonces, haríamos lo siguiente
```python
print("Introduce tu edad: ")
age = int(input("Edad: "))
```

####
----
## Variables booleanas y operadores de decisión
### Booleanos
**Dato booleano.** Es un tipo de dato que solamente puede tomar 2 valores: `True` (verdadero) o `False` (falso).
**Variable lógica.** Variable que almacena datos booleanos.

```python
is_adult = True
type(is_adult) # True
```

---
### Operadores Logicos
Para hacer la negación, utilizamos el operador `not`.
```python
A = True
not A # False

B = False
not B # True
```

Para hacer la conjunción entre dos variables lógicas, utilizamos el operador `and`.
```python
A, B = True, True
A and B # True

A and (not B) # False
```

Para hacer la disyunción entre dos variables lógicas, utilizamos el operador `or`.
```python
A, B = False, False
A or B # False

(not A) or B # True
```

---
### Operadores de Comparacion
En `Python` podemos comparar datos y obtener un resultado booleano. Los operadores de comparación disponibles son
```python
> # Estrictamente mayor
≥ # Mayor o igual
< # Estrictamente menor
≤ # Menor o igual
== # Igual
!= # Diferente
```

----
### Mas Metodos de Strings
El método `.startswith()` nos devuelve verdadero si el string empieza con el caracter o la cadena de caracteres indicado.
```python
s = "Mallorca es una isla preciosa"
s.startswith("m") # False
s.startswith("M") # True
```

El método `.endswith()` nos devuelve verdadero si el string acaba con el caracter o la cadena de caracteres indicado.
```python
s = "Mallorca es una isla preciosa"
s.endswith("a") # True
s.endswith("bonita") # False
```

El método `.isalnum()` nos devuelve verdadero si todos los caracteres del string son alfanuméricos.
```python
s = "Python365"
s.isalnum() # True

s = "Han creado un blog llamado Python365"
s.isalnum() # False
```

El método `.isalpha()` nos devuelve verdadero si todos los caracteres del string son del alfabeto.
```python
s = "Cachalote"
s.isalpha() # True

s = "Mi perro se llama Guindilla"
s.isalpha() # False
```

El método `.isdigit()` nos devuelve verdadero si todos los caracteres del string son dígitos.
```python
s = "365"
s.isdigit() # True

s = "Pyo365"
s.isdigit() # False
```

El método `.isspace()` nos devuelve verdadero si todos los caracteres del string son espacios en blanco.
```python
s = "                  "
s.isspace() # True
```

El método `.islower()` nos devuelve verdadero si todos los caracteres del string están en minúscula.
```python
s = "Mi gato se llama Bigotes"
s.islower() # False
```

El método `.isupper()` nos devuelve verdadero si todos los caracteres del string están en mayúscula.
```python
s = "Mi gato se llama Bigotes"
s.isupper() #False
```

El método `.istitle()` nos devuelve verdadero si todas las palabras del string empiezan en mayúscula y el resto de las letras de la palabra están en minúscula.
```python
s = "Platero Y Yo"
s.istitle() # True
```

---
### Operadores de Decision
#### If:
Cuando queremos comprobar si se cumple alguna condición, utilizamos el operador de decisión `if`. La sintaxis que debemos seguir es la siguiente:
```python
if condicion:
    consecuencia
```

#### Else:
Ahora, nos podríamos preguntar qué le podríamos decir al usuario en el caso en que no satisfaga la condición. Ahí es donde entra en juego el operador de decisión `else`. Esta vez, la sintaxis a seguir es la siguiente:
```python
if condición:
    consecuencia_si_es_verdad
else:
    consecuencia_si_es_falsa
```

#### Elif:
Ahora, en vez de comprobar si se cumple o no una condición, nos podríamos preguntar cómo haríamos para comprobar más de una condición. Podríamos hacerlo a lo bruto anidando operadores `if`, esto es, metiendo un `if` dentro de otro; o bien, podríamos hacerlo utilizando el operador de decisión `elif`.

El operador `elif` funciona del siguiente modo: se empieza con un operador `if`; si la condición de este no se cumple, pasamos a la siguiente condición posible precedida de un `elif`; si esta tampoco se cumple, pasamos al siguiente `elif`; seguimos así hasta que o bien se satisface alguna condición y realizamos su consecuencia, o hasta llegar al `else`, que implica que no se ha satisfecho ninguna de las condiciones anteriores.

La sintaxis del operador de decisión `elif` es la siguiente:
```python
if condición_1:
  consecuencia
elif condición_2:
  consecuencia
elif condición_3:
  consecuencia
.
.
.
else:
  consecuencia
```

#### Operador Ternario:
Si queremos hacer un simple `if` / `else` en una sola línea de código, podemos utilizar el operador ternario, que tiene la siguiente estructura:
```python
consecuencia_cierto if condición else consecuencia_falso
```

#### Operadores Anidados:
```python
age = 20
name = "Martin"
  
if age >= 18:
  if name.startswith("M") or name.startswith("m"):
    print("Eres mayor de edad pues tienes {} años y tu nombre, que es {}, empieza por M".format(age, name))w
  else:
    print("Eres mayor de edad pues tienes {} años".format(age))
else:
  print("Eres muy joven")
```


####
---
## Operadores de Iteración
### Bucle 'While'
La idea del bucle `while` es: mientras la condición sea cierta, seguimos realizando las líneas del interior del bucle. Una vez la condición deja de ser verdadera, salimos del bucle.

Su estructura es la siguiente
```python
inicialización de la variable de la condición

while condición verdadera:
  instrucción 1
  instrucción 2
  .
  .
  .
  instrucción n
```
**Observación.** Vuelven a aparecer tanto los dos puntos después de la condición como la indentación previa a las instrucciones que se encuentran dentro del bucle.

**¡Cuidado!** Hay que tener en cuenta que alguna de las instrucciones que se encuentran dentro del bucle `while` tiene que modificar a la variable de la condición. De lo contrario, si la variable de la condición nunca es modificada, la condición nunca llegará a ser falsa y el bucle no acabaría nunca, con lo que pasaría a convertirse en lo que se denomina bucle infinito.

---
### Comando 'Break'
`break` es muy útil si dada una condición queremos que se salga inmediatamente de un bucle `while`. Veámoslo con un ejemplo:

#### Ejemplo 1:
```python
fibo_ant = 1 # Término anterior
fibo = 1 # Término actual
idx = 3 # Como ya tenemos los dos primeros términos, empezamos con el índice 3
  
print("El término {} ocupa la posición {}".format(fibo_ant, 1))
print("El término {} ocupa la posición {}".format(fibo, 2))
  
while fibo <= 500000: # Establecemos una cota para que el bucle no sea infinito
  temp = fibo  # Guardamos temporalmente el fibonacci actual
  fibo = fibo + fibo_ant  # Calculamos el nuevo término de la sucesión
  fibo_ant = temp # Modicamos el valor del término anterior
  print("El término {} ocupa la posición {}".format(fibo, idx))
  if idx == 20: # Si llegamos al vigésimo índice,
    break       # salimos del bucle
  idx += 1 # Incrementamos el valor del índice
```

---
### Combinacion while ... else
Podemos combinar un bucle `while` con el operador `else` para ejecutar un bloque de código una vez la condición del `while` haya dejado de ser verdadera.
```python
i = 10
print("Preparados para despegue. Empieza la cuenta atrás.")

while i >= 0:
  print(i)
  i -= 1
else:
  print("La cuenta atrás ha finalizado.")
```

---
### Bucle 'for'
La idea del bucle `for` es: para todos los elementos de la clave, seguimos realizando las líneas del bucle. Una vez nos quedemos sin elementos, salimos del bucle.

Su estructura es la siguiente
```python
for clave:
  instrucción 1
  instrucción 2
  .
  .
  .
  instrucción n
```

---
### Función 'range'
La función `range()` tiene 3 posibles argumentos:
- `start`
- `stop`
- `step`
Veremos el uso de la función `range()` con un ejemplo. Recuperemos el ejemplo en que queríamos imprimir los 10 primeros números naturales:
```python
for i in range(1, 11, 1):
  print(i)

for x in range(5):
    print(x)
```
**Observación.** Cosas a tener en cuenta cuando usamos la función `range()`:
- El elemento indicado en el argumento `stop` nunca se incluye.
- Si no indicamos ningún elemento en el argumento `start`, por defecto éste vale 0.
- El valor por defecto del argumento `step` es 1.

Por lo tanto, obtendríamos el mismo resultado que en el ejemplo anterior ejecutando las siguientes líneas de código:
```python
for i in range(1, 11):
  print(i)
```

### Comando 'continue'
El comando `continue` es similar a `break`, pero en vez de salir del bucle, lo que hace es interrumpir la iteración en la que se encuentra y empezar la siguiente iteración.
#### Ejemplo 2:
Supongamos que queremos que se nos impriman todos los números entre 0 y 100 que no son ni divisibles entre 2 ni entre 5.

**Ejercicio.** Pensad cómo podríais resolver este problema en el cual se exige que en algún momento utilicéis el comando `continue`.
```python
	for i in range(101):
  if i % 2 == 0 or i % 5 == 0:
    continue
  print(i)
```

### Bucles Anidados
Se trata de bucles dentro de bucles
#### Ejemplo 3:
Vamos a calcular las tablas de multiplicar de los números del 1 al 10 anidando dos bucles `for`:
```python
for i in range(1, 11):
  print("\nTabla de multiplicar del {}".format(i))
  for j in range(1, 21):
    print("{} x {} = {}".format(i, j, i * j))
```
####
---
## Estructuras de Datos: Listas
**Listas:** Son un conjunto de elementos ordenados separados por comas y escritos entre `[]`
Estas son :
- *heterogéneas:* los elementos pueden ser de distinto tipo en una misma lista.
- *mutables:* los elementos pueden ser modificados.
Un ejemplo de lista sería:
```python
l = ["Juan", 31, 172.32, True]
print(l) # ['Juan', 31, 172.32, True]
```

### Tamaño de una Lista
Para saber la longitud o el tamaño de una lista, podemos hacer uso de la función `len()`
```python
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
len(l) # 9
```

---
### Elementos de una Lista
Cada elemento en la lista tiene su propio índice.
```python
names = ["Maria", "Juan", "Claudia", "Jorge", "Avelina"]
```
A `María` le corresponde el índice 0; a `Juan`, el 1; a `Claudia` el 2; a `Jorge`, el 3; y a `Avelina`, el 4.

**¡Cuidado!** En `Python`, los índices siempre empiezan en 0. De este modo, al primer elemento le corresponde el índice 0; al segundo, el índice 1; y al n-ésimo, le corresponde el índice n−1.

Dada una lista, podemos acceder a sus elementos utilizando la sintaxis `[]`.
```python
print(names[0]) # Maria
print(names[3]) # Jorge
```

**¡Cuidado!** Si dada una lista llamamos a un elemento cuyo índice no existe para dicha lista, `Python` automáticamente nos devolverá error.

Podemos acceder a los últimos elementos de la lista haciendo uso de índices negativos.
```python
print(names[-1]) # Ultimo Elemento               -> Avelina
print(names[-3]) # Tecer Elemento desde el Final -> Claudia 
```

Si en vez de querer acceder a los elementos uno por uno estamos interesados en acceder a avarios elementos a la vez, podemos hacer uso de la función `:`
```python
print(names[2:4]) # ['Claudia', 'Jorge']
print(names[:3])  # ['Maria', 'Juan', 'Claudia']
print(names[3:])  # ['Jorge', 'Avelina']
```

---
### Bucles con Listas
Si quisiéramos imprimir por pantalla todos los elementos de una lista, lo podríamos hacer mediante los índices:
```python
for i in range(len(names)):
  print(names[i])
```
o mucho más fácilmente iterando la lista con un `for` con la siguiente sintaxis:
```python
for name in names:
  print(name)
```
 ---
### Concatenación de Listas
Dadas dos o más listas, podemos concatenarlas haciendo uso de la función `+`
```python
l1 = [True, 21, "Marta"]
l2 = [22.5, False, 22, "Rafa"]
print(l1 + l2)
# [True, 21, 'Marta', 22.5, False, 22, 'Rafa']
```

---
### Repetición de Listas
Podemos repetir una misma lista tantas veces como queramos con la función `*`
```python
abc = ["A", "B", "C"]
print(abc * 5)
# ['A', 'B', 'C', 'A', 'B', 'C', 'A', 'B', 'C', 'A', 'B', 'C', 
#  'A', 'B', 'C']
```

----
### Lista Vacia
```python
empty_list = []
print(len(empty_list)) # 0
```

---
### Conversión de Listas
Para convertir un objeto iterable de `Python` a lista, hay que usar la función `list()`
```python
print(type(range(0, 100, 10)))
# <class 'range'>
print(list(range(0, 100, 10)))
# [0, 10, 20, 30, 40, 50, 60, 70, 80, 90]
print(type(list(range(0, 100, 10))))
# <class 'list'>
```

---
### Listas Anindadas
Las listas anidadas son listas dentro de listas. Es decir, las listas no solo pueden contener números, strings o datos booleanos, sino que también pueden contener otras listas.

A continuación mostramos una lista anidada, pues consta de 3 elementos:
- 1 lista de 3 strings
- 1 lista heterogénea de 3 elementos que a su vez contiene una lista con 5 números
- 1 número
```python
l = [["María", "Santos", "Fernández"],
     ["Juan", [1, 2, 3, 4, 5], 32],
     2]
print(l)
# [['María', 'Santos', 'Fernández'], ['Juan', [1, 2, 3, 4, 5], 32], 2]
```

Para acceder a un elemento, necesitamos indicar su índice. Si un elemento está en una lista dentro de una lista dentro de una lista, en primer lugar indicamos el índice de la lista exterior dentro de `[]`; después, el índice de la siguiente lista más exterior también entre `[]`; y por último, el índice de la lista más interna, claramente también entre `[]`.

Accedamos al string `Fernández`y luego al número `5`.
```python
print(l[0][2]) # Fernández
print(l[1][1][4]) # 5
```

---
### Metodos para trabajar con Listas
#### append( )
Podemos añadir nuevos elementos a una lista con el método `.append()`
```python
names = ["María", "Cristina", "Juana"]
print(names) # ['María', 'Cristina', 'Juana']

names.append("Andrea")
print(names) # ['María', 'Cristina', 'Juana', 'Andrea']
names.append("Ana")
print(names) # ['María', 'Cristina', 'Juana', 'Andrea', 'Ana']
```
**Observación.** Los elementos añadidos con el método `.append()`, se incluyen al final.

Si quisiéramos añadir un nuevo elemento a una lista, pero no lo quisiéramos al final, sino en una posición específica, entonces utilizaremos el método `.insert()` al que primero le indicamos el índice donde queremos posicionar el nuevo elemento y, en segundo lugar, indicamos dicho nuevo elemento.
```python
names = ["Mario", "Cristian", "Juan"]
print(names) # ['Mario', 'Cristian', 'Juan']

names.insert(1, "Andrés")
print(names) # ['Mario', 'Andrés', 'Cristian', 'Juan']
names.insert(3, "Miguel")
print(names) # ['Mario', 'Andrés', 'Cristian', 'Miguel', 'Juan']
```
**Observación.** Cuando le indicamos que queremos el elemento `Andrés` en el índice 1, el que antes ocupaba dicho índice, `Cristian`, pasa a ocupar el siguiente, 2, y así con el resto de elementos que van a continuación.

----
#### count( )
El método `.count()` recibe un elemento como argumento y cuenta la cantidad de veces que aparece en la lista
```python
numbers = [0, 1, 1, 2, 2, 2, 3, 3, 3, 3]

counted = []
for element in numbers:
  if element not in counted:
    counted.append(element)
    print("El elemento {} aparece {} veces".format(element, numbers.count(element)))
```

---
#### extend( )
El método `.extend()` extiende la lista agregando al final el iterable indicado por parámetro.
```python
numbers = [1, 2, 3, 4, 5]
print(numbers) # [1, 2, 3, 4, 5]
numbers.extend([6])
print(numbers) # [1, 2, 3, 4, 5, 6]
numbers.extend([7, 8])
print(numbers) # [1, 2, 3, 4, 5, 6, 7, 8]
numbers.extend(range(9, 16))
print(numbers) # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
```
**Observación.** Un iterable es un objeto de `Python` capaz de devolver sus elementos uno por uno, permitiendo ser iterado en un bucle for. De momento solo conocemos las listas y el resultado de `range()`, pero en secciones futuras veremos los diccionarios, las tuplas y los conjuntos, que también son objetos iterables.

---
#### index( )
El método `index()` recibe un elemento como argumento y devuelve el índice de la primera aparición en la lista.
```python
numbers = [0, 1, 1, 2, 2, 2, 3, 4, 3, 4]
print(numbers.index(2)) # 3
print(numbers.index(4)) # 7
```

---
#### pop( )
El método `.pop()` devuelve el último elemento de la lista y lo borra de la misma.
```python
print(numbers)
for i in range(5):
    print(numbers.pop()) # Almacena el ultima valor o lo elimina
    print(numbers)
```

---
#### remove( )
El método `.remove()` recibe como argumento un elemento y borra su primera aparición de la lista.
```python
numbers = [0, 1, 2, 4, 3, 4, 5, 6, 7]
numbers.remove(4)
print(numbers) # [0, 1, 2, 3, 4, 5, 6, 7]
```

---
#### reverse( )
El método `.reverse()` devuelve la lista en orden inverso.
```python
numbers = [1, -1, 2, -2, 3, -3]
numbers.reverse()
print(numbers) # [-3, 3, -2, 2, -1, 1]
```

---
#### sort( )
El método `.sort()` devuelve la lista en orden.
```python
numbers = [1, 3, 5, 2, 4]
numbers.sort()
print(numbers) # [1, 2, 3, 4, 5]
```

Si quisiésemos ordenar los elementos en orden decreciente, podríamos hacer uso del parámetro `reverse` del método `.sort()`:
```python
numbers = [1, 3, 5, 2, 4]
numbers.sort(reverse = True)
print(numbers) # [5, 4, 3, 2, 1]
```
**Observación.** De momento solo conocemos las listas y el resultado de `range()`, pero en secciones futuras veremos los diccionarios, las tuplas y los conjuntos, que también son objetos iterables.
####
---

### Matrices
Hay un tipo muy utilizado de listas anidadas. Se caracteriza por ser una lista de m listas, donde cada una de las listas tiene el mismo número de elementos, **n**. A este tipo de listas se les conoce como matrices.
```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

Para acceder a los elementos de una matriz en `Python`, utilizamos la sintaxis `[][]`, donde primero indicamos la fila y, a continuación, la columna
```python
matrix[0][2] # 3
matrix[1][1] # 5
matrix[2][0] # 7
```

Podemos mostrar una matriz de `Python` en forma de tabla con un bucle `for`, del siguiente modo
```python
for row in matrix: # Accedemos a las filas de la matrix
  print(row)
# [1, 2, 3] 
# [4, 5, 6]
# [7, 8, 9]
```

Si lo que queremos es mostrar todos los elementos de la matriz en columna, podemos utilizar dos bucles `for` anidados del siguiente modo:
```python
for row in matrix: # Accedemos a las filas
  for element in row: # Accedemos a los elementos de las filas
    print(element)
```

Si lo que queremos es mostrar la matriz en forma de tabla, sin comas ni claudators por en medio, lo podemos hacer de dos formas:
- Haciendo uso de las dimensiones de la matriz y, por tanto, de la función `range()`
- Sin hacer uso de las dimensiones
La primera forma sería:
```python
# m es el número de filas y n, el de columnas
m = len(matrix)
n = len(matrix[0])

for i in range(m):
  for j in range(n):
    print(matrix[i][j], end = " ")
  print("")
```

#### Suma de Matrices
Para poder sumar dos matrices, necesitamos que tengan la misma dimensión. Entonces, dadas A y B dos matrices con dimensión m×n, su suma será una matriz de dimensión m×n y sus elementos se obtienen del siguiente modo:
![[Pasted image 20230626142533.png]]

Dadas dos matrices con la misma dimensión, las podemos usar haciendo uso de bucles `for`anidados.
```python
A = [[1, 0, -3], [2, 0, 1], [-1, -1, 0]]
B = [[-1, -2, 0], [-2, 3, 0], [0, 0, -3]]

m = len(A)
n = len(A[0])

if len(A) == len(B) and len(A[0]) == len(B[0]):
  C = []

  for i in range(m):
    C.append([])
    for j in range(n):
      C[i].append(A[i][j] + B[i][j])

  print(C)

else:
  print("No se puede realizar la suma, pues las dimensiones de las matrices no coinciden.")
```

#### Producto de Matrices
Para poder multiplicar matrices, necesitamos que la matriz de la izquierda tenga el mismo número de columnas que número de filas tiene la matriz de la derecha. Entonces, dadas las matrices **A y B** de dimensiones **m×n** y **n×p** respectivamente, su producto será una matriz de dimensión m×p y se obtiene del siguiente modo:
![[Pasted image 20230710114310.png]]

Dadas dos matrices, la primera con el mismo número de columnas que filas tiene la segunda, podemos multiplicarlas del siguiente modo:
```python
A = [[1, 0, -3, 2], [2, 0, 1, 1], [-1, 0, -1, 0]]
B = [[-1, -2, 0], [-2, 3, 0], [0, 0, -3], [1, 1, -1]]

m, n, p = len(A), len(B), len(B[0])

C = []

for i in range(m):
  C.append([])
  for j in range(p):
    elemento = 0
    for k in range(n):
      elemento = elemento + A[i][k] * B[k][j]
    C[i].append(elemento)
```

El resultado de multiplicar las matrices A y B ha sido:
![[Pasted image 20230710115215.png]]
```python
for row in C:
  print(row)

[1 ,  0,  7] 
[-1, -3, -4] 
[1 ,  2,  3]
```

---
#### Matrices con Numpy
Existe una forma más sencilla de trabajar con matricdes y es gracias a la librería `numpy`. Para importarla, simplemente hay que ejecutar la siguiente línea de código.
```python
import numpy as np
```

Para crear una matriz vacía, usamos el método `.empty()`, al que le indicamos por parámetro las dimensiones
```python
A = np.empty((2, 3)) # 2 filas y 3 columnas
print(A)
```

Para crear una matriz vacía con las mismas dimensiones de otra matriz definida anteriormente, usamos el método `.empty_like()`, al que le indicamos por parámetro la matriz existente
```python
B = np.empty_like(A)
```

Para crear una matriz nula, usamos el método `.zeros()`, al que le indicamos por parámetro las dimensiones
```python
C = np.zeros((3, 5)) # Matriz nula de dimensiones 3 x 5
print(C)
```

Para crear una matriz de ceros con las mismas dimensiones de otra matriz definida anteriormente, usamos el método `.zeros_like()`, al que le indicamos por parámetro la matriz existente
```python
D = np.zeros_like(A) # Tendrá 2 filas y 3 columnas y todos sus elementos valdrán 0
print(D)
```

Para crear una matriz de unos, usamos el método `.ones()`, al que le indicamos por parámetro las dimensiones
```python
E = np.ones((1, 4)) # Matriz de unos de dimensiones 1 x 4
print(E)
```

Para crear una matriz de unos con las mismas dimensiones de otra matriz definida anteriormente, usamos el método `.ones_like()`, al que le indicamos por parámetro la matriz existente
```python
F = np.ones_like(C) # Tendrá 3 filas y 5 columnas y todos sus elementos valdrán 1
print(F)
```

Podemos crear matrices de numpy a partir de listas con el método `.matrix()`
```python
M = np.matrix([[1, 0, -3, 2], [2, 0, 1, 1], [-1, 0, -1, 0]])
print(M)
```

Para saber las dimensiones de una matriz, podemos utilizar el método `.shape`
```python
M.shape # (3, 4)
```

Ahora es más sencillo sumar matrices, pues solamente necesitamos la función `+`
```python
A = np.matrix([[1, 0, -3], [2, 0, 1], [-1, -1, 0]])
B = np.matrix([[-1, -2, 0], [-2, 3, 0], [0, 0, -3]])
matrixSum = A + B
matrixSum
```

También es más sencillo hacer el producto matricial A⋅B con el método `.dot()`
```python
A = np.matrix([[1, 0, -3, 2], [2, 0, 1, 1], [-1, 0, -1, 0]])
B = np.matrix([[-1, -2, 0], [-2, 3, 0], [0, 0, -3], [1, 1, -1]])

matrixProd = A.dot(B)
matrixProd
```

Gracias a `numpy`, también es mucho más sencillo mostrar una matriz en forma de tabla, pues nos basta con hacer uso de la función `print()`:
```python
print(matrixSum)
print(matrixProd)

[[ 0 -2 -3] 
 [ 0  3  1] 
 [-1 -1 -3]] 
[[ 1  0  7] 
 [-1 -3 -4] 
 [ 1  2 3]]
```

####
---
## Estructuras de Datos: Diccionarios
La segunda estructura de datos que veremos son los **diccionarios**. Éstos son un conjunto de elementos no ordenados escritos entre llaves, `{}`, que constan de claves y valores.

Cada conjunto `clave: valor` es separado por comas. Las claves funcionan como identificadores y preceden a `:`. A continuación van los valores, que son elementos (numéricos, booleanos, strings, listas, diccionarios...) asociados a esa clave.

Los diccionarios, al igual que las listas, son:

- hetereogéneos: los elementos pueden ser de distinto tipo en un mismo diccionario
- mutables: los elementos pueden ser modificados

Un ejemplo de diccionario sería:
```python
dicc = {"Jose": 32, "Marina": 21}
print(dicc)
```

**¡Cuidado!** En `Python`, las claves de un diccionario deben ser únicas. Esto es, no puede haber dos claves que sean exactamente iguales. Si se da que hay dos claves iguales, entonces `Python` se queda con el último valor asociado a dicha clave.

### Elementos de un diccionario

Anteriormente se ha comentado que los diccionarios no tienen orden. De modo que a sus elementos no se accede por posición, sino que debemos hacerlo mediante sus claves.

La sintaxis es `diccionario[clave]`
```python
dicc = {
    "names": ["Ana", "Borja", "Carmen"],
    "ages" : [31, 25, 16]
    }
dicc["names"]
```

Podemos acceder a todas las claves de un diccionario con el método `.keys()`
```python
dicc.keys() # dict_keys(['names', 'ages'])
```

También podemos acceder a todos los valores de un diccionario con el método `.values()`
```python
dict_values([['Ana', 'Borja', 'Carmen'], [31, 25, 16]])
```

**Observación.** La función `str()` impone que lo que sea que introduzcamos sea un dato de tipo `string`. Funciona exactamente del mismo modo que lo hacen las funciones `int()` y `float()` introducidas y utilizadas en temas anteriores.

```python
value_string = str(0)
type(value_string) # '0'
```

### Tamaño de un diccionario
Para saber cuántos elementos contiene un diccionario, podemos usar la función `len()` del siguiente modo:
```python
dicc = {"fruit": ["Manzana", "Pera", "Naranja"],
        "price": [2, 1.5, 1],
        "color": ["roja", "verde", "naranja"]}

print(len(dicc)) # 3
```

### Bucles y diccionarios
Para recorrer todo el diccionario, podemos hacer uso de un bucle `for`, pues el diccionario es una estructura iterable:
```python
dicc = {"username": "msf",
        "name": "María",
        "age": 22,
        "city": "Palma de Mallorca"}

for key in dicc:
  print(key, ":", dicc[key])
```

Otra forma de recorrer el diccionario sería obteniendo una lista de tuplas de la forma `(clave, valor)` para cada elemento de un diccionario, que construimos con el método `.items()`. Al ser una lista, sabemos que es iterable y podemos mostrar todas sus entradas haciendo uso de un bucle `for`.
```python
dicc.items()
# dict_items([('username', 'msf'), ('name', 'María'), ('age', 22), ('city', 'Palma de Mallorca')])
```

### Más métodos de diccionarios
#### clear( )
El método `.clear()` elimina todos los elementos del diccionario dejándolo vacío.
```python
dicc = {"a": 4, "b": 3, "c": 2, "d": 1}
print(dicc) # {'a': 4, 'b': 3, 'c': 2, 'd': 1}

dicc.clear()
print(dicc) # {}
```

#### copy( )
El método `.copy()` devuelve una copia del diccionario original.
```python
dicc = {"a": 4, "b": 3, "c": 2, "d": 1}
dicc_copy = dicc.copy()

print(dicc_copy) # {'a': 4, 'b': 3, 'c': 2, 'd': 1}
```

#### fromkeys( )
El método `.fromkeys()` recibe como parámetros un iterable y un valor y devuelve un diccionario que contiene como claves los elementos del iterable con el mismo valor ingresado.
```python
dicc = dict.fromkeys(["a", "b", "c", "d", "e"], [1, 2, 3, 4])
print(dicc) # {'a': [1, 2, 3, 4], 'b': [1, 2, 3, 4], 'c': [1, 2, 3, 4], 'd': [1, 2, 3, 4], 'e': [1, 2, 3, 4]}
```

**Observación.** Si el parámetro valor se deja en blanco, el método devolverá un diccionario con el valor `None` para todas las claves.
```python
dicc = dict.fromkeys(["a", "b", "c", "d", "e"])
print(dicc) # {'a': None, 'b': None, 'c': None, 'd': None, 'e': None}
```

#### get( )
El método `.get()` recibe como parámetro una clave y devuelve el valor de dicha clave.
```python
dicc = {"a": 1, "e": 2, "i": 3, "o": 4, "u": 5}
print(dicc.get("a")) # 1
```

#### pop( )
El método `.pop()` recibe como parámetro una clave, la elimina y devuelve su valor.
```python
dicc = {"a": 1, "e": 2, "i": 3, "o": 4, "u": 5}
print(dicc) # {'a': 1, 'e': 2, 'i': 3, 'o': 4, 'u': 5}
print(dicc.pop("i")) # 3
print(dicc) # {'a': 1, 'e': 2, 'o': 4, 'u': 5}
```

**Observación.** Si la clave indicada por parámetro no se encuentra en el diccionario, el método devuelve error.

El método `.setdefault()` puede funcionar de dos formas:
- Como el método `.get()`
- Para agregar un nuevo elemento al diccionario.
```python
# Como .get()
dicc = {"a": 1, "e": 2, "i": 3, "o": 4, "u": 5}
print(dicc.setdefault("i")) # 3

# Para agregar nuevo elemento
print(dicc.setdefault("ü", 6)) # 6
print(dicc) # {'a': 1, 'e': 2, 'i': 3, 'o': 4, 'u': 5, 'ü': 6}
```

El método `.update()` recibe como parámetro otro diccionario. En caso de tener claves iguales, actualiza el valor de la clave repetida. En caso de no haber claves iguales, el par `clave: valor` es agregado al diccionario al que es aplicado el método.
```python
dicc1 = {"a": 1, "e": 2, "i": 3, "o": 4, "u": 5}
dicc2 = {"a": 1, "b": 2, "c": 3, "d": 4, "e": 5}
dicc1.update(dicc2)
  
print(dicc1) # {'a': 1, 'e': 5, 'i': 3, 'o': 4, 'u': 5, 'b': 2, 'c': 3, 'd': 4}
```

### Construyendo diccionarios con dict( )
Para convertir un objeto iterable de `Python` a diccionario, hay que usar la función `dict()`
```python
l = [["x", 1], ["y", 2]]
dict(l) # {'x': 1, 'y': 2}
```

Aunque la función `dict()` también sirve para definir diccionarios directamente:
```python
dicc1 = dict(x = 0, y = 1, z = -1)
print(dicc1) # {'x': 0, 'y': 1, 'z': -1}
```

```python
dicc2 = dict({"x": 0, "y": 1, "z": -1})
print(dicc2) # {'x': 0, 'y': 1, 'z': -1}
```

```python
dicc3 = dict({"x": 0}, y = 1, z = -1)
print(dicc3) # {'x': 0, 'y': 1, 'z': -1}
```
###
----
## Estructuras de Datos: Conjuntos
Ahora, es el turno de los **conjuntos**. Éstos son una estructura sin orden que no admiten múltiples ocurrencias de un mismo elemento. Pueden ser definidos a partir de una lista con la función `set()`, o bien, los elementos del conjunto pueden ir entre llaves, `{}`, y estar separados por comas.

Los conjuntos son:

- heterogéneos: los elementos pueden ser de distinto tipo en un mismo conjunto
- no mutables: los elementos no pueden ser modificados una vez el conjunto ha sido creado

Los conjuntos pueden construirse con la función `set()` o directamente entre llaves, `{}`.
```python
set1 = set([1, 7, 4, 2, 0])
print(set1) # {0, 1, 2, 4, 7}
type(set1) # set

set2 = set((1, 7, 4, 2, 0))
print(set2) # {0, 1, 2, 4, 7}
type(set2) # set

set3 = {1, 7, 4, 2, 0}
print(set3) # {0, 1, 2, 4, 7}
type(set3) # set
```

**Observación.** Al decir que los conjuntos no tienen orden, lo que ocurre es que `Python` no mantendrá el que hemos introducido, tal y como hacía con las listas, sino que reordenará todos los elementos por orden primero numérico (yendo antes los negativos que los positivos) y luego alfabético de las claves. Con la función `print()`, si hay elementos negativos, el conjunto no se ordena correctamente.

Por lo que hemos visto hasta ahora, podemos decir que los conjuntos en `Python` son fieles a la definición matemática de éstos, salvo por el hecho de que en `Python` un conjunto no puede contener como elemento a otro conjunto:

**Conjunto.** Colección de elementos pertenecientes a la misma categoría, y cuya agrupación puede ser considerada o identificada en sí misma como un objeto. Un conjunto queda definido únicamente por sus elementos y por nada más. En particular, un conjunto puede escribirse como una lista de elementos, pero cambiar el orden de dicha lista o añadir elementos repetidos no define un conjunto nuevo.

### Subconjunto: 
**Subconjunto.** Un subconjunto B de un conjunto A es un conjunto que contiene algunos de los elementos de A (o quizá todos). Se denota por B⊆A

**Subconjunto propio.** Un subconjunto propio B de un conjunto A es un conjunto que tiene algunos de los elementos de A, pero no todos. Se denota por B⊂A

Para saber si un conjunto B es subconjunto del conjunto A, podemos utilizar el método `.issubset()` o el comparador `<=`. Para saber si se trata de un subconjunto propio, tenemos el comparador `<`.
```python
A, B = {0, 3, 7, 2, 5}, {2, 3, 0}
B.issubset(A) # True
B <= A # True
B < A # True
```

**Superconjunto.** Un superconjunto A de un conjunto B es un conjunto que contiene a B. Se denota por A⊇B

**Superconjunto propio.** Un superconjunto propio A de un conjunto B es un conjunto que contiene a B y consta de al menos un elemento más. Se denota por A⊃B

Para saber si un conjunto A es superconjunto del conjunto B, podemos utilizar el método `.issuperset()` o el comparador `>=`. Para saber si se trata de un superconjunto propio, tenemos el comparador `>`.
```python
A, B = {0, 3, 7, 2, 5}, {2, 3, 0}
A.issuperset(B) # True
A >= B # True
A > B # True
```
---
### Operaciones con conjuntos:
Dados los conjuntos A y B, vamos a ver una serie de operaciones que podemos hacer con ellos.
![[Pasted image 20230818134311.png]]

**Unión.** La unión de dos conjuntos A y B es un nuevo conjunto A∪B que contiene todos los elementos de A y/o todos los de B.
![[Pasted image 20230818134415.png]]

En `Python`, la unión de dos conjuntos se consigue con la función `|` o bien, con el método `.union()`
```python
A, B = {1, 3, 5, 7, 9}, {0, 2, 4, 6, 8}

A | B # {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
A.union(B) # {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
B.union(A) # {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
```

**Intersección.** La intersección entre dos conjuntos A y B es un nuevo conjunto A∩B que contiene todos los elementos comunes de A y B.
![[Pasted image 20230818134702.png]]

En `Python`, la intersección de dos conjuntos se consigue con la función `&` o bien, con el método `.intersection()`
```python
A, B = {0, 1, 3, 5, 8, 13}, {0, 2, 4, 6, 8}

A & B
A.intersection(B)
B.intersection(A)
```

**Diferencia.** La diferencia entre dos conjuntos A y B es un nuevo conjunto A−B que contiene todos los elementos de A que no están en B
![[Pasted image 20230818135723.png]]
En `Python`, la diferencia de dos conjuntos se consigue con la función `-` o bien, con el método `.difference()`
```python
A, B = {0, 1, 4, 5, 8, 13}, {0, 3, 4, 7, 8}

A - B # {1, 5, 13}
A.difference(B) # {1, 5, 13}
B.difference(A) # {3, 7}
```

**Diferencia simétrica.** La diferencia entre dos conjuntos A y B es un nuevo conjunto A△B que contiene todos los elementos de A∪B no están en A∩B
![[Pasted image 20230818135916.png]]
![[Pasted image 20230818135928.png]]
En `Python`, la diferencia simétrica de dos conjuntos se consigue con el método `.symmetric_difference()`
```python
A, B = {0, 1, 4, 5, 8, 13}, {0, 3, 4, 7, 8}

A.symmetric_difference(B) # {1, 3, 5, 7, 13}
(A-B) | (B-A) # {1, 3, 5, 7, 13}
(A | B) - (A & B) # {1, 3, 5, 7, 13}
``` 

---
### Elementos de un Conjunto: 
#### add( )
Podemos añadir un elemento a un conjunto con el método `.add()`
```python
set1 = {1, 2, 3, 4, 5}
set1.add(-1)
print(set1) # {1, 2, 3, 4, 5, -1}

set1.add(0)
print(set1) # {0, 1, 2, 3, 4, 5, -1}
```

#### update( )
Para añadir elementos de otro conjunto en el conjunto actual, podemos usar el método `.update()`
```python
set1 = {1, 2, 3, 4, 5}
set2 = {-1, -2, -3, -4, -5}

print(set1) # {1, 2, 3, 4, 5}

set1.update(set2)
print(set1) # {1, 2, 3, 4, 5, -1, -5, -4, -3, -2}
```

**Observación.** El método `.update()` nos permite añadir los elementos de un iterable al conjunto actual
```python
set1 = {1, 2, 3, 4, 5}
l = [-1, -2, -3, -4, -5]

set1.update(l)
print(set1) # {1, 2, 3, 4, 5, -2, -5, -4, -3, -1}
```

#### in
Podemos averiguar si un elemento pertenece a un conjunto con el operador `in`
```python
set1 = {1, -1, 2, -2, 3, -3}

print(3 in set1) # True
print(0 in set1) # False
```

#### remove( ) / discard( )
También podemos eliminar elementos de un conjunto con los métodos `.remove()` o `.discard()`
```python
set1 = {"a",  "e", "i", "o", "u"}

set1.remove("a")
set1.discard("o")
  
print("a" in set1) # False
print("o" in set1) # False
print(set1) # {'e', 'u', 'i'}
```

**Observación.** Si intentamos eliminar un elemento que no existe ya de por sí en el conjunto con el método `.remove()`, `Python` nos devolverá error, mientras que con el método `.discard()` no devolverá ningún error.

---
### Tamaño de un Conjunto:
Para saber cuántos elementos contiene un conjunto, podemos usar la función `len()`del siguiente modo:
```python
set1 = {1, "a", "i", "o", 2, "e", 4, 3, 5, "u"}
print(len(set1)) # 10
```
---
### Bucles y conjuntos:
Podemos acceder a todos los elementos de un conjunto mediante un bucle `for`
```python
set1 = {"manzana", "pera", "melón"}
for item in set1:
  print(item)
```
---
### Más métodos de conjuntos:
#### pop( )
El método `.pop()` nos devuelve un objeto del conjunto (como no hay orden, no sabemos cuál es) y lo elimina de éste.
```python
set1 = {"u", 5, -3, "a", "b"}
set1 # {-3, 5, 'a', 'b', 'u'}
set1.pop() # b
set1 # {-3, 5, 'a', 'u'}
```

#### clear( )
El método `.clear()` vacía el conjunto.
```python
set1 = {"a", "e", "i", "o", "u"}
set1.clear()
print(set1) # set()
```
###
----
## Estructuras de Datos: Tupla
Éstas son un conjunto de elementos, que pueden ser de distintos tipos, separados por comas y escritos entre paréntesis, `()`.

Las tuplas son:
- heterogéneas: los elementos pueden ser de distinto tipo en una misma tupla
- no mutables: los elementos no pueden ser modificados una vez la tupla ha sido creado

Un ejemplo de tupla sería:
```python
t = ("Juan", 32, "profesor", True)
print(t) # ('Juan', 32, 'profesor', True)
```

Podemos declarar una tupla sin necesidad indicar sus elementos entre paréntesis
```python
t = "Juan", 32, "profesor", True
type(t) # tuple
```

Podemos declarar tuplas con la función `tuple()`
```python
t = tuple(("Juan", 32, "profesor", True))
type(t) # tuple

tuple([1,2,3]) 
```

### Elementos de una tupla: 
Podemos acceder a los elementos de una tupla mediante el índice que ocupan con la sintaxis de claudator, `[]`
```python
t = 1, "a", 2, "e", 3, "i", 4, "o", 5, "u"
print(t[0]) # 1
print(t[5]) # i
```

Al igual que con las listas, podemos acceder a los elementos de tuplas mediante el uso de índices negativos
```python
print(t[-1]) # u
print(t[-4]) # 4
```

Para acceder a múltiples entradas de una tupla a la vez, podemos utilizar la función `:` para indicar un intervalo de índices.
```python
print(t[2:6]) # (2, 'e', 3, 'i')
print(t[:5])  # (1, 'a', 2, 'e', 3)
print(t[5:])  # ('i', 4, 'o', 5, 'u')
```

**Observación.** Recordad que

- el índice indicado tras los dos puntos, `:`, nunca es incluido.
- si no se indica índice a la izquierda de `:`, se considera desde el índice 0 hasta el inmediatamente anterior al indicado a la derecha de `:`
- si no se indica índice a la derecha de `:`, se considera desde el índice indicado a la izquierda de `:` hasta el último elemento

También podemos usar índices negativos con la función `:`
```python
print(t[-5:-1]) # ('i', 4, 'o', 5)
```

Para saber si un elemento pertenece a una tupla, podemos usar la palabra clave `in`
```python
print(6 in t)   # False
print("i" in t) # True
```

Hemos dicho que las tuplas son inmutables. Esto es, una vez creada la tupla, sus elementos no pueden ser modificados
```python
t = "Cereza", "Manzana", "Pera"
t[1] = "Kiwi"
```

Una alternativa sería convertir a lista, realizar la modificación y reconvertir a tupla
```python
t = "Cereza", "Manzana", "Pera"
t = list(t)
t[1] = "Kiwi"
t = tuple(t)

print(t)       # ('Cereza', 'Kiwi', 'Pera')
print(type(t)) # <class 'tuple'>
```
---
### Método unpacking:
Podemos extraer los valores de una tupla en variables. Este proceso es conocido como **unpacking**
```python
fruits = "Cereza", "Kiwi", "Pera", "Naranja"
print(type(fruits)) # <class 'tuple'>

# Con paréntesis
(fruit1, fruit2, fruit3, fruit4) = fruits
# o tambien
fruit1, fruit2, fruit3, fruit4 = fruits
  
print(fruit1)
print(fruit2)
print(fruit3)
print(fruit4)
```

**¡Cuidado!** El número de variables debe coincidir con el número de elementos de la tupla. De lo contrario, debe usarse un asterisco para guardar los elementos restantes en una lista.
```python
fruits = "Cereza", "Kiwi", "Pera", "Naranja"

(fruit1, fruit2, *restFruits) = fruits

print(fruit1) # Cereza
print(fruit2) # Kiwi
print(restFruits)  # ['Pera', 'Naranja']
print(type(restFruits))
```

**Observación.** Si el asterisco es añadido en alguna variable que no sea la última, `Python` almacenará tantos elementos en la lista como sea necesario para que el número de elementos restantes coincida con el número de variables restantes.
```python
fruits = "Cereza", "Kiwi", "Pera", "Naranja", "Melocotón", "Sandía", "Melón"

(fruit1, *restFruits, fruit2, fruit3) = fruits

print(fruit1) # Cereza
print(restFruits) # ['Kiwi', 'Pera', 'Naranja', 'Melocotón']
print(fruit2) # Sandía
print(fruit3) # Melón
```

```python
fruits = "Cereza", "Kiwi", "Pera", "Naranja", "Melocotón", "Sandía", "Melón"

(fruit1, *_, fruit2, fruit3) = fruits

print(fruit1)
print(fruit2)
print(fruit3)
```
---
### Concatenación de Tuplas:
Podemos concatenar tuplas con la función `+`, aunque el resultado será una nueva tupla, ya que recordemos éstas no pueden ser modificadas.
```python
t1 = 1, 3
t2 = 2, 4

t1 + t2 # (1, 3, 2, 4)
```
---
### Repetición de tuplas
Podemos repetir tuplas un número n de veces con la función `*`
```python
t = ("a", "b", "c")
t * 5 # ('a', 'b', 'c', 'a', 'b', 'c', 'a', 'b', 'c', 'a', 'b', 'c', 'a', 'b', 'c')
```
---
### Tamaño de una tupla
Podemos calcular el número de elementos de una tupla con la función `len()`
```python
t = "Juan", 32, "profesor", True
len(t) # 4
```

**¡Cuidado!** Si quisiésemos crear una tupla de un solo elemento, tendríamos que hacer lo siguiente
```python
t1 = ("manzana", )
print(type(t1)) # <class 'tuple'>

# Lo siguiente no es una tupla
t2 = ("manzana")
print(type(t2)) # <class 'str'>
```
---
### Bucles y tuplas
Podemos iterar una tupla utilizando un bucle `for`
```python
fruits = "Cereza", "Kiwi", "Pera", "Naranja", "Melocotón", "Sandía", "Melón"

for fruit in fruits:
  print(fruit)
```

También podemos usar la técnica de unpacking en los bucles
```python
t = ("cereza", "roja"), ("kiwi", "amarillo"), ("pera", "verde"), ("naranja", "naranja")

for fruit, color in t:
  if fruit == "kiwi":
    print("El color del", fruit, "es", color)
  else:
    print("La {} es {}".format(fruit, color))
```
----
### Tuplas y el resto de estructuras de datos:
Una tupla puede contener listas, diccionarios, conjuntos y tuplas.
```python
t = [4, 5, 6], {"vowels": ("a", "e", "i", "o", "u")}, {1, 2, 3}, ("x", "y")
type(t) # tuple
```

Asimismo,

- las listas pueden contener diccionarios, conjuntos, tuplas y otras listas
- los diccionarios pueden contener listas, conjuntos, tuplas y otros diccionarios
- los conjuntos no pueden contener ni listas, ni diccionarios, ni tuplas, ni siquiera otros conjuntos

Dado cualquier objeto iterable en `Python`, lo podemos convertir a tupla con la función `tuple()`
```python
print(tuple(l)) # A partir de una lista
print(type(tuple(l)))

print(tuple(dicc)) # A partir de un diccionario solo se guardan las claves en la tupla
print(type(tuple(dicc)))

print(tuple({1, 2, 3, 4, 5})) # A partir de un conjunto
print(type(tuple({1, 2, 3, 4, 5})))
```
---
### La función `zip()`
La función `zip()` sirve para juntar listas en tuplas
```python
objects = ["libreta", "pluma", "portaminas", "pack_minas"]
price = [5.00, 3.30, 1.29, 0.50]
items = zip(objects, price)
print(items) # <zip object at 0x7f3782cff6c8>
```

Podemos convertir el resultado de una función `zip()` a una lista
```python
items = zip(objects, price)
list(items) # [('libreta', 5.0), ('pluma', 3.3), ('portaminas', 1.29), ('pack_minas', 0.5)]
```

Podemos convertir el resultado de una función `zip()` a un diccionario
```python
items = zip(objects, price)
dict(items) # {'libreta': 5.0, 'pack_minas': 0.5, 'pluma': 3.3, 'portaminas': 1.29}
```

**¡Cuidado!** Hay que crear de nuevo el objeto `zip()`, pues el resultado de esta función es un iterador y, una vez ha sido convertido a lista, diccionario o tupla, se considera una iteración completa y no será capaz de generar más valores.

Podemos convertir el resultado de una función `zip()` a una tupla:
```python
items = zip(objects, price)
tuple(items) # (('libreta', 5.0), ('pluma', 3.3), ('portaminas', 1.29), ('pack_minas', 0.5))
```

```python
for obj, pr in zip(objects, price):
    print("El objeto {} cuesta {} €.".format(obj, pr))

# El objeto libreta cuesta 5.0 €. 
# El objeto pluma cuesta 3.3 €. 
# El objeto portaminas cuesta 1.29 €. 
# El objeto pack_minas cuesta 0.5 €.
```
###
---
