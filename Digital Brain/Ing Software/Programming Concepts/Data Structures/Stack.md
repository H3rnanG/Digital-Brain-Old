#EngineeringSoftware 

Una pila, en programación, es una estructura de datos que sigue una política conocida como LIFO (Last In, First Out), lo que significa que el último elemento que se inserta en la pila es el primero en ser retirado. En PHP, puedes implementar pilas utilizando arrays o utilizando la clase `SplStack`.

Aquí te explico cómo funcionan las pilas en PHP utilizando ambos enfoques:

## Pilas utilizando arrays:
#### Creacion de una Pila:
```php
$pila = [];
```

--- 
#### Agregar elementos a una pila:
```php
array_push($pila, 'elemento1'); 
array_push($pila, 'elemento2'); 
array_push($pila, 'elemento3');
```

---
#### Retirar elemento de una pila:
```php
$elemento = array_pop($pila); // Almacenando el primer valor en $elemento
echo $elemento; // Imprime "elemento3"
```

---
#### Accediendo al primer valor:
```php
$elementoSuperior = end($pila); // Almacenando el primer valor en $elemento
echo $elementoSuperior; // Imprime "elemento2"
```

----


## Pilas utilizando 'SplStack( )' 
#### Creacion de una Pila:
```php
$pila = new SplStack();
```

--- 
#### Agregar elementos a una pila:
```php
$pila->push('elemento1'); 
$pila->push('elemento2'); 
$pila->push('elemento3');
```

---
#### Retirar elemento de una pila:
```php
$elemento = $pila->pop(); 
echo $elemento; // Imprime "elemento3"
```

---
#### Accediendo al primer valor:
```php
$elementoSuperior = $pila->top(); 
echo $elementoSuperior; // Imprime "elemento2"
```

----
##
En ambos enfoques, puedes realizar operaciones básicas de una pila, como agregar elementos con `push`, retirar elementos con `pop` y acceder al elemento superior sin retirarlo con `top`. El uso de pilas es útil en situaciones en las que necesitas almacenar elementos de manera temporal y acceder a ellos en orden inverso al que se agregaron.

