#EngineeringSoftware 
# Que es el Internet?
El internet, también conocido como la red de redes, **es una red global de computadoras interconectadas que permite la comunicación y el intercambio de información a nivel mundial.** En términos simples, es una red de computadoras distribuidas por todo el mundo que están conectadas entre sí a través de una variedad de tecnologías de comunicación, como cables de fibra óptica, conexiones inalámbricas y líneas telefónicas.

---
# Como trabaja el Internet?
En un nivel alto, **Internet funciona conectando dispositivos y sistemas informáticos mediante un conjunto de protocolos estandarizados.** Estos protocolos definen cómo se intercambia la información entre dispositivos y garantizan que los datos se transmitan de manera confiable y segura.

**El núcleo de Internet es una red global de enrutadores interconectados,** que se encargan de dirigir el tráfico entre diferentes dispositivos y sistemas. Cuando envía datos a través de Internet, se dividen en pequeños paquetes que se envían desde su dispositivo a un enrutador. El enrutador examina el paquete y lo reenvía al siguiente enrutador en el camino hacia su destino. Este proceso continúa hasta que el paquete llega a su destino final.

Para garantizar que los paquetes se envíen y reciban correctamente, Internet utiliza una variedad de protocolos, incluido el **Protocolo de Internet (IP)** y el **Protocolo de control de transmisión (TCP)**. IP es responsable de enrutar los paquetes a su destino correcto, mientras que TCP garantiza que los paquetes se transmitan de manera confiable y en el orden correcto.

Además de estos protocolos básicos, existe una amplia gama de otras tecnologías y protocolos que se utilizan para permitir la comunicación y el intercambio de datos a través de Internet, incluido el Sistema de nombres de dominio (DNS), el Protocolo de transferencia de hipertexto (HTTP) y el Protocolo seguro. Protocolo de seguridad de capa de sockets/capa de transporte (SSL/TLS). Como desarrollador, es importante tener un conocimiento sólido de cómo estas diferentes tecnologías y protocolos funcionan juntos para permitir la comunicación y el intercambio de datos a través de Internet.

---
# Conceptos basicos y terminologias:
Para comprender Internet, es importante estar familiarizado con algunos conceptos y terminología básicos. Aquí hay algunos términos y conceptos clave que debe tener en cuenta:

- **Paquete:** Pequeña unidad de datos que se transmite a través de Internet.
- **Enrutador:** Dispositivo que dirige paquetes de datos entre diferentes redes.
- **Dirección IP:** Un identificador único asignado a cada dispositivo en una red, utilizado para enrutar datos al destino correcto.
- **Nombre de dominio:** Un nombre legible por humanos que se utiliza para identificar un sitio web, como google.com.
- **DNS:** El sistema de nombres de dominio es responsable de traducir los nombres de dominio en direcciones IP.
- **HTTP:** El protocolo de transferencia de hipertexto se utiliza para transferir datos entre un cliente (como un navegador web) y un servidor (como un sitio web).
- **HTTPS:** Una versión cifrada de HTTP que se utiliza para proporcionar una comunicación segura entre un cliente y un servidor.
- **SSL/TLS:** Los protocolos Secure Sockets Layer y Transport Layer Security se utilizan para proporcionar una comunicación segura a través de Internet.

---
# El rol de los protocolos:
Los protocolos desempeñan un papel fundamental a la hora de permitir la comunicación y el intercambio de datos a través de Internet. Un protocolo es un conjunto de reglas y estándares que definen cómo se intercambia información entre dispositivos y sistemas.

Hay muchos protocolos diferentes utilizados en la comunicación por Internet, incluido el **Protocolo de Internet (IP)**, el **Protocolo de control de transmisión (TCP)**, el **Protocolo de datagramas de usuario (UDP)**, el **Sistema de nombres de dominio (DNS)** y muchos otros.

IP es responsable de enrutar paquetes de datos a su destino correcto, mientras que TCP y UDP garantizan que los paquetes se transmitan de manera confiable y eficiente. DNS se utiliza para traducir nombres de dominio en direcciones IP y HTTP se utiliza para transferir datos entre clientes y servidores.

Uno de los beneficios clave de utilizar protocolos estandarizados es que permiten que dispositivos y sistemas de diferentes fabricantes y proveedores se comuniquen entre sí sin problemas. Por ejemplo, un navegador web desarrollado por una empresa puede comunicarse con un servidor web desarrollado por otra empresa, siempre que ambos cumplan con el protocolo HTTP.

Los Protocolos mas conocidos son:
## Direcciones IP y Dominios:
**Una dirección IP es un identificador único asignado a cada dispositivo en una red.** Se utiliza para enrutar datos al destino correcto, asegurando que la información se envíe al destinatario previsto.
Las direcciones IP normalmente se representan como una serie de cuatro números separados por puntos, como "192.168.1.1".

**Los nombres de dominio, por otro lado, son nombres legibles por humanos que se utilizan para identificar sitios web y otros recursos de Internet.** Por lo general, se componen de dos o más partes, separadas por puntos. Por ejemplo, "google.com" es un nombre de dominio.
Los nombres de dominio se traducen a direcciones IP mediante el Sistema de nombres de dominio (DNS).

**El DNS es una parte fundamental de la infraestructura de Internet, responsable de traducir los nombres de dominio en direcciones IP.** Cuando ingresa un nombre de dominio en su navegador web, su computadora envía una consulta DNS a un servidor DNS, que devuelve la dirección IP correspondiente.
Luego, su computadora usa esa dirección IP para conectarse al sitio web u otro recurso que haya solicitado.

---
## Http y Https:
Http y Https son los dos protocolos comumente mas usados en aplicacion y servicios basados en internet.

**Http es el protocolo usado para transferir informacion entre el cliente (como un navegador) y el servidor (como un sitio web).** Cuando visitas un sitio web tu navegador web envia una solicitud HTTP al servidor, solicitando la pagina web o otros recursos solicitados. Luego el servidor envia una respuesta HTTP al cliente que contiene los datos solicitados.

**Https es una version mas segura de Http,** que sifra los datos que se transmiten entre el cliente y el servidor mediante cifrado **SSL/TLS (Secure Sockets Layer/Transport Layer Security).** 

### Metodos Http:
HTTP define un conjunto de **métodos de petición** para indicar la acción que se desea realizar para un recurso determinado. Aunque estos también pueden ser sustantivos, estos métodos de solicitud a veces son llamados _HTTP verbs_.

- **GET:** El método `GET` solicita una representación de un recurso específico. Las peticiones que usan el método `GET` sólo deben recuperar datos.
- **HEAD:** El método `HEAD` pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta.
- **POST:** El método `POST` se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.
- **PUT:** El modo `PUT` reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.
- **DELETE:** El método `DELETE` borra un recurso en específico.
- **CONNECT:** El método `CONNECT` establece un túnel hacia el servidor identificado por el recurso.
- **OPTIONS:** El método `OPTIONS` es utilizado para describir las opciones de comunicación para el recurso de destino.
- **TRACE:** El método `TRACE` realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.
- **PATCH:** El método `PATCH` es utilizado para aplicar modificaciones parciales a un recurso.

---
## Tcp y IP:
**TCP/IP (Protocolo de control de transmisión/Protocolo de Internet) es el protocolo de comunicación subyacente utilizado por la mayoría de las aplicaciones y servicios basados ​​en Internet.** Proporciona una entrega de datos confiable, ordenada y con verificación de errores entre aplicaciones que se ejecutan en diferentes dispositivos.

Al crear aplicaciones con TCP/IP, hay algunos conceptos clave que se deben comprender:

- **Puertos:** los puertos se utilizan para identificar la aplicación o servicio que se ejecuta en un dispositivo. A cada aplicación o servicio se le asigna un número de puerto único, lo que permite enviar datos al destino correcto.
- **Sockets:** un socket es una combinación de una dirección IP y un número de puerto, que representa un punto final específico para la comunicación. Los sockets se utilizan para establecer conexiones entre dispositivos y transferir datos entre aplicaciones.
- **Conexiones:** Se establece una conexión entre dos enchufes cuando dos dispositivos quieren comunicarse entre sí. Durante el proceso de establecimiento de la conexión, los dispositivos negocian varios parámetros, como el tamaño máximo del segmento y el tamaño de la ventana, que determinan cómo se transmitirán los datos a través de la conexión.
- **Transferencia de datos:** una vez que se establece una conexión, los datos se pueden transferir entre las aplicaciones que se ejecutan en cada dispositivo. Los datos normalmente se transmiten en segmentos, y cada segmento contiene un número de secuencia y otros metadatos para garantizar una entrega confiable.

---
## Ssl y Tls:
**SSL/TLS es un protocolo utilizado para cifrar datos que se transmiten a través de Internet.** Se utiliza comúnmente para proporcionar conexiones seguras para aplicaciones como navegadores web, clientes de correo electrónico y programas de transferencia de archivos.

Cuando se utiliza SSL/TLS para proteger la comunicación por Internet, hay algunos conceptos clave que se deben comprender:

- **Certificados:** Los certificados SSL/TLS se utilizan para establecer confianza entre el cliente y el servidor. Contienen información sobre la identidad del servidor y están firmados por un tercero de confianza (una Autoridad de certificación) para verificar su autenticidad.
- **Handshake:** Durante el proceso de protocolo de enlace SSL/TLS, el cliente y el servidor intercambian información para negociar el algoritmo de cifrado y otros parámetros para la conexión segura.
- **Cifrado:** Una vez que se establece la conexión segura, los datos se cifran utilizando el algoritmo acordado y pueden transmitirse de forma segura entre el cliente y el servidor.

---
# Que es una Uri?
**El URI (siglas de _uniform resource identifier_) o identificador uniforme de recursos sirve para acceder a un recurso físico o abstracto por Internet**. Dependiendo de la situación, el recurso puede ser de muchos tipos: por ejemplo, un URI puede identificar tanto una página web como al remitente o al destinatario de un correo electrónico. Las aplicaciones utilizan este identificador único para interactuar con el recurso o consultar información sobre el mismo.
## Sintaxix de una Uri:
Un URI consta de un máximo de cinco partes, de las cuales solo dos son obligatorias:

- **_scheme_** _(esquema)_: proporciona información sobre el protocolo utilizado.
- **_authority_** _(autoridad)_: identifica el dominio.
- **_path_** _(ruta)_: muestra la ruta exacta al recurso.
- **_query_** _(consulta)_: representa la acción de consulta.
- **_fragment_** _(fragmento)_: designa una parte del recurso principal.

Los dos elementos imprescindibles que deben contener todos los identificadores son _scheme_ y _path_. En la estructura del URI, los componentes se enumeran uno tras otro por este orden y están separados por caracteres estándar.

```none
scheme :// authority path ? query # fragment
```

---
## Que es la IANA?
**La [IANA](https://www.ionos.es/digitalguide/servidores/know-how/iana-que-es-y-cual-es-su-funcion/ "IANA: qué es y cuál es su función") (Internet Assigned Numbers Authority) es la entidad que se encarga de coordinar los esquemas de los URI, es decir, la primera parte de todos los enlaces.** También cabe la posibilidad de utilizar _schemes_ personalizados, aunque los establecidos por esta organización son ampliamente utilizados en todo Internet. Estos son los más conocidos:

- **about**: información del navegador
- **data**: datos incrustados
- **feed**: canales web
- **file**: archivos
- **ftp**: [file transfer protocol](https://www.ionos.es/digitalguide/servidores/know-how/file-transfer-protocol/ "File Transfer Protocol")
- **git**: control de versiones con Git
- **http**: [hypertext transfer protocol](https://www.ionos.es/digitalguide/hosting/cuestiones-tecnicas/protocolo-http/ "protocolo HTTP")
- **https:** [hypertext Transfer Protocol Secure](https://www.ionos.es/digitalguide/hosting/cuestiones-tecnicas/que-es-https/ "¿Qué es HTTPS?")
- **imap:** internet message access protocol
- **mailto**: direcciones de correo electrónico
- **news**: grupos de noticias de Usenet
- **pop**: POP3
- **rsync**: sincronización de datos
- **sftp**: _SSH file transfer protocol_
- **ssh**: _[Secure Shell](https://www.ionos.es/digitalguide/servidores/herramientas/protocolo-ssh/ "Protocolo SSH")_
- **tel**: números de teléfono
- **urn**: uniform resource name

---
## URL vs. URN
- **URL:** Uniform Resource Location: Localizador Uniforme de Recursos. Es una URI que indica la ubicación de un recurso en internet y permite localizarlo.
- **URN:** Uniform Resource Name: Nombre Uniforme de Recursos. Esta cadena especializada indica el nombre de un recurso que es único en internet. La URN indica un nombre único y público de un recurso en internet.
![[Pasted image 20230926125411.png]]
# Tecnologias Futuras:
Internet está en constante evolución y todo el tiempo surgen nuevas tecnologías y tendencias. Como desarrollador, es importante mantenerse actualizado con los últimos desarrollos para poder crear aplicaciones y servicios innovadores y eficaces.

Estas son algunas de las tendencias y tecnologías emergentes que están dando forma al futuro de Internet:

- **5G:** 5G es la última generación de tecnología de redes móviles, que ofrece velocidades más rápidas, menor latencia y mayor capacidad que las generaciones anteriores. Se espera que permita nuevos casos de uso y aplicaciones, como vehículos autónomos y cirugía remota.
- **Internet of Things (IoT):** IoT se refiere a la red de dispositivos físicos, vehículos, electrodomésticos y otros objetos que están conectados a Internet y pueden intercambiar datos. A medida que IoT siga creciendo, se espera que revolucione industrias como la atención sanitaria, el transporte y la fabricación.
- **Inteligencia Artificial (IA):** las tecnologías de IA, como el aprendizaje automático y el procesamiento del lenguaje natural, ya se están utilizando para impulsar una amplia gama de aplicaciones y servicios, desde asistentes de voz hasta detección de fraude. A medida que la IA continúa avanzando, se espera que permita nuevos casos de uso y transforme industrias como la atención médica, las finanzas, y educación.
- **Blockchain:** Blockchain es una tecnología de contabilidad distribuida que permite transacciones seguras y descentralizadas. Se utiliza para impulsar una amplia gama de aplicaciones, desde criptomonedas hasta gestión de la cadena de suministro.
- **Edge Computing:** La computación de borde se refiere al procesamiento y almacenamiento de datos en el borde de la red, en lugar de en centros de datos centralizados. Se espera que permita nuevos casos de uso y aplicaciones, como análisis en tiempo real y aplicaciones de baja latencia.

---
# Conclucion:
Y eso nos lleva al final de este artículo. Hemos cubierto mucho terreno, así que tomemos un momento para repasar lo que hemos aprendido:

- Internet es una red global de computadoras interconectadas que utiliza un conjunto estándar de protocolos de comunicación para intercambiar datos.
- Internet funciona conectando dispositivos y sistemas informáticos mediante protocolos estandarizados, como IP y TCP.
- El núcleo de Internet es una red global de enrutadores interconectados que dirigen el tráfico entre diferentes dispositivos y sistemas.
- Los conceptos y terminología básicos con los que necesita familiarizarse incluyen paquetes, enrutadores, Direcciones IP, nombres de dominio, DNS, HTTP, HTTPS y SSL/TLS.
- Los protocolos desempeñan un papel fundamental a la hora de permitir la comunicación y el intercambio de datos a través de Internet, permitiendo que dispositivos y sistemas de diferentes fabricantes y proveedores se comuniquen sin problemas.