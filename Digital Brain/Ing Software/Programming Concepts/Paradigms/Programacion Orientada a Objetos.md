#EngineeringSoftware 

La programación orientada a objetos (POO) es un [[Programming Concepts#Paradigma en Programacion:|paradigma]] de programación que se basa en la organización y estructuración del código a través de la creación de objetos, los cuales son instancias de clases. En POO, los objetos representan entidades o conceptos del mundo real y poseen propiedades (atributos) y comportamientos (métodos).

## 4 Principios de la POO
#### Abstracción:
Se refiere a la capacidad de modelar un objeto en términos de sus características y comportamientos esenciales, sin preocuparse por los detalles de implementación.
```php
abstract class Vehiculo {
  abstract public function encender();
  abstract public function apagar();
}

class Coche extends Vehiculo {
  public function encender() {
    echo "Encendiendo coche...";
  }
  
  public function apagar() {
    echo "Apagando coche...";
  }
}

$coche = new Coche();
$coche->encender(); // Output: Encendiendo coche...
$coche->apagar(); // Output: Apagando coche...
```

En este ejemplo, la clase Vehiculo es una clase abstracta que define dos métodos abstractos (`encender()` y `apagar()`) que cualquier vehículo debe implementar. La clase Coche extiende la clase Vehiculo y proporciona una implementación para los métodos abstractos. De esta manera, la clase Coche se abstrae de los detalles específicos de cómo se enciende o se apaga un vehículo, lo que permite una mayor flexibilidad en la implementación.

#### Encapsulamiento:
La encapsulación se refiere a la ocultación de datos y métodos dentro de una clase, de manera que solo sean accesibles desde dentro de la clase. Para lograr esto, se utilizan modificadores de acceso, como `public`, `private` y `protected`. Aquí tienes un ejemplo:
```php
class Usuario {
  private $nombre;
  private $email;
  
  public function __construct($nombre, $email) {
    $this->nombre = $nombre;
    $this->email = $email;
  }

  public function getNombre() {
    return $this->nombre;
  }
  
  public function getEmail() {
    return $this->email;
  }
  
  public function setEmail($email) {
    $this->email = $email;
  }
}

$usuario = new Usuario("Juan", "juan@example.com");
echo $usuario->getNombre(); // Output: Juan
$usuario->setEmail("nuevo-email@example.com"); // Cambiamos de email
echo $usuario->getEmail(); // Output: nuevo-email@example.com
```

En este ejemplo, la clase Usuario tiene dos propiedades (nombre y email) que están definidas como privadas. Esto significa que solo se pueden acceder a ellas desde dentro de la clase. Sin embargo, la clase proporciona métodos públicos (`getNombre()`, `getEmail()` y `setEmail()`) para acceder a estas propiedades. De esta manera, los detalles de implementación están ocultos y solo se puede acceder a la información del usuario a través de una interfaz pública.
- *get:* Obtener
- *set:* Establecer

#### Polimorfismo:
El polimorfismo se refiere a la capacidad de objetos de diferentes clases de responder al mismo mensaje de manera diferente. En otras palabras, objetos de diferentes clases pueden implementar el mismo método de manera distinta. Aquí tienes un ejemplo:
```php
class Figura {
  public function area() {
    echo "Calculando área de la figura...";
  }
}

class Cuadrado extends Figura {
  private $lado;
  
  public function __construct($lado) {
    $this->lado = $lado;
  }
  
  public function area() {
    return $this->lado * $this->lado;
  }
}

class Circulo extends Figura {
  private $radio;
  
  public function __construct($radio) {
    $this->radio = $radio;
  }
  
  public function area() {
    return 3.14 * $this->radio * $this->radio;
  }
}

$cuadrado = new Cuadrado(5);
$circulo = new Circulo(3);

echo $cuadrado->area(); // Output: 25
echo $circulo->area(); // Output: 28.26
```

En este ejemplo, la clase Figura tiene un método `area( )` que es redefinido en las clases hijas Cuadrado y Circulo. Cada clase hija proporciona su propia implementación del método `area( )` que calcula el área de la figura específica.

Al llamar al método `area( )` en las instancias de las clases Cuadrado y Circulo, se ejecuta la implementación correspondiente de cada clase hija. Esto demuestra el polimorfismo, donde un objeto puede tomar diferentes formas dependiendo de su clase real y cómo se ha redefinido un método heredado.

#### Herencia:
La herencia permite crear nuevas clases basadas en clases existentes, heredando sus atributos y métodos. La clase derivada (hija) hereda los atributos y métodos de la clase base (padre) y puede agregar o modificar su comportamiento. Aquí tienes un ejemplo:
```php
class Animal {
  protected $nombre;
  
  public function __construct($nombre) {
    $this->nombre = $nombre;
  }
  
  public function mover() {
    echo "El animal se mueve...";
  }
}

class Perro extends Animal {
  public function ladrar() {
    echo "El perro ladra...";
  }
}

$perro = new Perro("Fido");
$perro->mover(); // Output: El animal se mueve...
$perro->ladrar(); // Output: El perro ladra...
echo $perro->nombre; // Error: propiedad protegida, no se puede acceder directamente
```

En este ejemplo, la clase Animal es la clase padre que tiene una propiedad protegida llamada "nombre" y un método `mover()`. La clase Perro es la clase hija que hereda de Animal y también tiene un método propio `ladrar()`.

Al crear una instancia de la clase Perro, podemos llamar a los métodos tanto de la clase padre como de la clase hija. El método `mover( )` se hereda de la clase Animal, mientras que el método `ladrar( )` es específico de la clase Perro.

Sin embargo, la propiedad "nombre" está definida como protegida en la clase Animal, lo que significa que no se puede acceder directamente desde fuera de la clase. En este caso, se producirá un error si intentamos imprimir el valor de `$perro->nombre`.

## Principios Solid
Los principios SOLID son un conjunto de principios de diseño de software que se enfocan en lograr un código limpio, modular, fácil de mantener y escalable. Estos principios fueron acuñados por Robert C. Martin (también conocido como "Uncle Bob") y se consideran fundamentales en la Programación Orientada a Objetos. A continuación, te explicaré brevemente cada uno de los principios SOLID:
#### 1. Principio de Responsabilidad Única (Single Responsibility Principle - SRP):
Este principio establece que una clase debe tener una única responsabilidad y motivo para cambiar. Cada clase debe tener una sola razón para ser modificada. Esto ayuda a mantener un código [[Diccionary#Cohesivo:|cohesivo]] y [[Diccionary#Modular:|modular]], facilitando su mantenimiento y reutilización.
```python
class Logger:
    def __init__(self, file_path):
        self.file_path = file_path

    def log_message(self, message):
        with open(self.file_path, 'a') as file:
            file.write(message + '\n')

class UserManager:
    def __init__(self, logger):
        self.logger = logger

    def add_user(self, user):
        # Lógica para agregar un usuario
        self.logger.log_message('Usuario agregado: ' + user.name)
```
En este ejemplo, la clase `Logger` se encarga exclusivamente de la funcionalidad de registro (log) y la clase `UserManager` se encarga exclusivamente de la gestión de usuarios. Cada clase tiene una única responsabilidad y motivo para cambiar.

#### 2. Principio de Abierto/Cerrado (Open/Closed Principle - OCP):
Este principio establece que las entidades de software (clases, módulos, etc.) deben estar abiertas para la extensión pero cerradas para la modificación. En lugar de modificar el código existente, se deben agregar extensiones o nuevas implementaciones para introducir nuevas funcionalidades. Esto se logra mediante el uso de la herencia, interfaces y composición.
```python
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius**2
```
En este ejemplo, la clase `Shape` es una clase base que define el método abstracto `area()`. Las clases derivadas `Rectangle` y `Circle` extienden la clase `Shape` y proporcionan su propia implementación del método `area()`. Esto permite extender el comportamiento sin modificar el código existente.

#### 3. Principio de Sustitución de Liskov (Liskov Substitution Principle - LSP): 
Este principio establece que los objetos de una clase base deben poder ser sustituidos por instancias de sus clases derivadas sin alterar el comportamiento correcto del programa. En otras palabras, los objetos deben ser intercambiables sin causar efectos secundarios no deseados. Esto garantiza que la herencia se utilice correctamente y que las subclases no rompan las expectativas establecidas por la clase base.
```python
class Bird:
    def fly(self):
        pass

class Sparrow(Bird):
    def fly(self):
        return "Sparrow is flying."

class Penguin(Bird):
    def fly(self):
        raise Exception("Penguins cannot fly.")

def make_bird_fly(bird):
    return bird.fly()

sparrow = Sparrow()
penguin = Penguin()

print(make_bird_fly(sparrow))
print(make_bird_fly(penguin))
```
En este ejemplo, la clase `Bird` es una clase base que define el método `fly()`. Las clases derivadas `Sparrow` y `Penguin` heredan de `Bird` y proporcionan su propia implementación del método `fly()`. Sin embargo, el método `fly()` de `Penguin` lanza una excepción porque los pingüinos no pueden volar. A pesar de las diferencias en la implementación, ambas clases pueden ser utilizadas en el contexto de `make_bird_fly()`, cumpliendo con el principio de sustitución de Liskov.

#### 4. Principio de Segregación de Interfaz (Interface Segregation Principle - ISP):
Este principio establece que una interfaz no debe obligar a las clases a depender de métodos que no utilizan. En lugar de tener interfaces monolíticas, es preferible tener interfaces específicas y cohesivas para cada contexto. Esto ayuda a evitar la dependencia innecesaria y acoplamientos fuertes entre clases.
```python
class Printer:
    def print_document(self, document):
        pass

class Scanner:
    def scan_document(self):
        pass

class Photocopier(Printer, Scanner):
    def print_document(self, document):
        # Lógica para imprimir un documento

    def scan_document(self):
        # Lógica para escanear un documento
```
En este ejemplo, la clase `Printer` define la interfaz para imprimir documentos y la clase `Scanner` define la interfaz para escanear documentos. La clase `Photocopier` implementa ambas interfaces, pero solo implementa los

métodos necesarios para realizar las tareas de impresión y escaneo. Esto evita que `Photocopier` dependa de métodos que no necesita.

#### 5. Principio de Inversión de Dependencia (Dependency Inversion Principle - DIP): 
Este principio establece que los módulos de alto nivel no deben depender de los módulos de bajo nivel. Ambos deben depender de abstracciones. Además, las abstracciones no deben depender de los detalles, sino que los detalles deben depender de las abstracciones. Este principio promueve el uso de la inyección de dependencias y la programación orientada a interfaces para reducir el acoplamiento y facilitar la flexibilidad y la extensibilidad del código.
```python
class Notification:
    def send_notification(self, message):
        pass

class EmailNotification(Notification):
    def send_notification(self, message):
        # Lógica para enviar una notificación por correo electrónico

class SMSNotification(Notification):
    def send_notification(self, message):
        # Lógica para enviar una notificación por mensaje de texto

class NotificationService:
    def __init__(self, notification):
        self.notification = notification

    def send_notification(self, message):
        self.notification.send_notification(message)
```
En este ejemplo, la clase `Notification` es una clase abstracta que define el método `send_notification()`. Las clases derivadas `EmailNotification` y `SMSNotification` implementan este método de acuerdo con su respectivo medio de notificación. La clase `NotificationService` depende de la abstracción `Notification`, lo que le permite cambiar la implementación concreta en tiempo de ejecución, cumpliendo con el principio de inversión de dependencia.