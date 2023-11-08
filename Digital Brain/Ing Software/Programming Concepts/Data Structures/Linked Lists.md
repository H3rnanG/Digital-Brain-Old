#EngineeringSoftware 

Las listas enlazadas son una estructura de datos dinámica en la que los elementos están organizados en nodos. Cada nodo contiene un elemento de datos y una referencia (enlace) al siguiente nodo en la lista. La lista en sí está formada por una secuencia de nodos enlazados.

En PHP, puedes implementar listas enlazadas creando una clase para representar un nodo y otra clase para representar la lista en sí. Aquí te explico cómo puedes utilizar las listas enlazadas en PHP:

## Creacion de la Clase Nodo:
```php
class Nodo {
    public $dato;
    public $siguiente;

    public function __construct($dato) {
        $this->dato = $dato;
        $this->siguiente = null;
    }
}
```

La clase `Nodo` representa un nodo en la lista enlazada. Tiene una variable `$dato` para almacenar el valor del nodo y una variable `$siguiente` que es una referencia al siguiente nodo en la lista.

## Creacion de la Clase Lista Enlazada:
```php
class ListaEnlazada {
    public $inicio;

    public function __construct() {
        $this->inicio = null;
    }

    public function agregar($dato) {
        $nuevoNodo = new Nodo($dato);

        if ($this->inicio === null) {
            $this->inicio = $nuevoNodo;
        } else {
            $actual = $this->inicio;
            while ($actual->siguiente !== null) {
                $actual = $actual->siguiente;
            }
            $actual->siguiente = $nuevoNodo;
        }
    }

    public function imprimir() {
        $actual = $this->inicio;
        while ($actual !== null) {
            echo $actual->dato . " ";
            $actual = $actual->siguiente;
        }
    }
}
```

La clase `ListaEnlazada` representa la lista enlazada en sí. Tiene una variable `$inicio` que es una referencia al primer nodo de la lista. La lista proporciona métodos para agregar elementos (`agregar`) y para imprimir los elementos en la lista (`imprimir`).

## Como utilizarla:
```php
$lista = new ListaEnlazada();
$lista->agregar(5);
$lista->agregar(10);
$lista->agregar(15);

$lista->imprimir();
// Imprime: 5 10 15
```

En este ejemplo, creamos una lista enlazada y agregamos tres elementos a la lista. Luego, imprimimos los elementos en la lista utilizando el método `imprimir`.

##
Las listas enlazadas son útiles cuando necesitas una estructura de datos dinámica que permite la inserción y eliminación eficiente de elementos en cualquier posición. Sin embargo, el acceso a un elemento en particular en una lista enlazada requiere recorrer la lista desde el principio hasta la posición deseada.

Ten en cuenta que esta implementación es una versión básica y simplificada de las listas enlazadas en PHP. En aplicaciones más complejas, es posible que desees considerar implementaciones más robustas y optimizadas.