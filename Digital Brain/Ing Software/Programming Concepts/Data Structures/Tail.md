#EngineeringSoftware 

  
Una cola, en programación, es una estructura de datos que sigue una política conocida como FIFO (First In, First Out), lo que significa que el primer elemento que se inserta en la cola es el primero en ser retirado. En PHP, puedes implementar colas utilizando arrays o utilizando la clase `SplQueue`.

Aquí te explico cómo funcionan las colas en PHP utilizando ambos enfoques:

## Colas utilizando arrays:
#### Creacion de una cola:
```php
$cola = [];
```

---
#### Agregar elementos a una cola:
```php
array_push($cola, 'elemento1'); 
array_push($cola, 'elemento2'); 
array_push($cola, 'elemento3');
```

---
#### Retirar elemento de una cola:
```php
$elemento = array_shift($cola); 
echo $elemento; // Imprime "elemento1"
```

---
#### Acceder al primer elemento de una cola:
```php
$elementoFrontal = reset($cola); 
echo $elementoFrontal; // Imprime "elemento2"
```

---
## Colas utilizando 'SplQueue( )':
#### Creacion de una cola:
```php
$cola = new SplQueue();
```

---
#### Agregar elementos a una cola:
```php
$cola->enqueue('elemento1'); 
$cola->enqueue('elemento2'); 
$cola->enqueue('elemento3');
```

---
#### Retirar elemento de una cola:
```php
$elemento = $cola->dequeue(); 
echo $elemento; // Imprime "elemento1"
```

---
#### Acceder al primer elemento de una cola:
```php
$elementoFrontal = $cola->bottom(); 
echo $elementoFrontal; // Imprime "elemento2"
```

---
##
En ambos enfoques, puedes realizar operaciones básicas de una cola, como agregar elementos con `enqueue`, retirar elementos con `dequeue` y acceder al primer elemento sin retirarlo con `front` o `bottom`. El uso de colas es útil en situaciones en las que necesitas procesar elementos en el orden en que fueron agregados, como en la implementación de algoritmos de búsqueda o en la gestión de tareas.