#EngineeringSoftware 

En PHP, las listas son estructuras de datos que permiten almacenar y manipular una colección ordenada de elementos. Las listas en PHP se pueden implementar de diferentes formas, siendo las más comunes el uso de arrays y la clase `SplDoublyLinkedList`.

En el contexto de las listas en PHP, se refiere a una colección de elementos en la que se mantiene el orden de inserción. Cada elemento en la lista puede ser accedido y manipulado según su posición en la lista.

## Utilizando arrays:
#### Creacion de una Lista:
```php
$lista = [
	'elemento1',
];
```

---
#### Acceso a elementos por indice:
```php
echo $lista[0]; // Imprime "elemento1"
```

---
#### Modificación de valores:
```php
$lista[0] = 'nuevo elemento';
```

---
#### Inserción de nuevos elementos:
```php
array_push($lista, 'elemento2'); 
array_push($lista, 'elemento3'); 
array_push($lista, 'elemento4');
```

---
#### Eliminación de un elemento:
```php
unset($lista[2]);
```

---
#### Verificación de existencia de un elemento:
```php
if (isset($lista[0])) {
    echo 'El elemento existe.';
} else {
    echo 'El elemento no existe.';
}
```

---
#### Recorrer una lista:
```php
foreach ($lista as $elemento) 
{ 
	echo $elemento . ' '; 
}
```

## Utilizando 'SplDoublyLinkedList( )'
#### Creacion de una Lista:
```php
$lista = new SplDoublyLinkedList();
```

---
#### Acceso a elementos por indice:
```php
echo $lista->offsetGet(0); // Imprime "elemento1"
```

---
#### Modificación de valores:
```php
$lista->offsetSet(1, 'nuevo elemento');
```

---
#### Inserción de nuevos elementos:
```php
$lista->push('elemento1'); 
$lista->push('elemento2'); 
$lista->push('elemento3');
```

---
#### Eliminación de un elemento:
```php
$lista->offsetUnset(2);
```

---
#### Verificación de existencia de un elemento:
```php
if (isset($lista->offsetGet(0))) {
    echo 'El elemento existe.';
} else {
    echo 'El elemento no existe.';
}
```

---
#### Recorrer una lista:
```php
$lista->rewind(); 
while ($lista->valid()) 
{ 
	echo $lista->current() . ' '; 
	$lista->next(); 
}
```
