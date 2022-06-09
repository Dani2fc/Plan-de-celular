# Encapsulación

- Cuando un objeto se encuentra encapsulado, solo sus métodos tienen acceso a sus atributos,
evitando así, la manipulación de los atributos mediante la presencia de fuentes externas,
es decir, quien programa un objeto controla los métodos de acceso, su estado y su comportamiento.
- Es una de las propiedades más importantes de la POO.
- Consiste en la separación de las propiedades externas de un objeto, correspondiente a la interfaz 
de sus funciones, de los detalles de implementación interna del objeto.
- Se reduce la complejidad del sistema protegineod los objetos contra posibles errores, y 
permitinedo lograr de mejor manera extensiones futuras en la implementación de los objetos.
- Consiste básicamente en proteger los atributos del acceso directo de los objetos, colocandolos
en una zona privada, y la única forma de acceder a ellos es por medio de los métodos que están en 
una zona pública.

## Mensajes

- Una aplicación orientada a objetos está compuesta por varios objetos creados desde sus respectivas clases.
- Estos obk¿jetos necesitan una forma de comunicarse, para intercambiar datos entre sí, y lo hacen por medio
de mensajes.
- Los mensajes puden contener parámetros en los cuales se indican las características específicas de la acción
a realizar.
- Estructuralmente está compuesto por los siguientes elementos: 
    1. Objeto destino, hacia el cual el mensaje es enviado.
    2. El nombre del método a llamar.
    3. Parámetros solicitados por el método, a través del cual suele 
    darse la información.
- El envío y recepción de mensajes es simplemente una petición de un objeto a otro objeto para que este se 
comporte de una manera determinada ejecutando uno de sus métodos.
- Ejemplo.
    Si existe un objeto A de la clase Carro y un objeto B de la clase Impuesto, para calcular el 10% de impuestos sobre el precio del carro. la comunicación podría ser:
    `float costo = A.getPrecio();`
    `B.calcularImpuesto(costo*0.10)`

## Ciclo de vida de los objetos
- El objeto nace cuando se crea, vive cuando se utiliza en un programa y muere cuando deja de usarse.

## Constructores 
- Son métodos especiales, que tienen las siguientes características:
    - Se llaman solo una vez al crear el objeto.
    - Tienen el mismo nombre de la clase.
    - Pueden haber varios (sobrecarga de métodos).
    - Al crear un objeto solo se utiliza uno.
    - No devuelve nada, ni void (realmente devuelve el objeto creado).
- Inicializa los atributos del objeto al momento de crearse sin hacer otra instrucción adicional.
- Java provee un constructor por defecto.
- Tipos:
    - Por defecto no recibe parámetros.
    - Común u ordinario: puede recibir toda clase de parámetros.
    - De copia: que permite la construcción de una copia del objeto.

## Crecimiento y vida del objeto
- Una vez creado el objeto:
    - Se puede trabajar con él.
    - Llamar a los métodos de su clase.
    - Guardar datos para almacenarlos temporalmente antes de registrarlo en una BD.
    - Compartr datos con los dem+as objetos, pasandoles mensajes.
- Cada objeto consume memoria, y depende de los atrbutos que tenga.

## Muerte del objeto
- Java utiliza el Garbage Collector para liberar los objetos no referenciados.
- Java cuenta las referencias que hay sobre cada objeto. El objeto se borra cuando no tenga referencias.
- Antes de borrarlo Java da la oportunidad de limpiarse a sí mismo: finalización.
- LLamado explicíto al gc `System.gc();`

## Ejercicio
- Crear un programa para gestionar un plan de telefonía celular. El plan tiene un número de celular,
operador, cantidad de minutos y un costo por minuto. Calcular el total a pagar teniendo en cuenta que 
si el operador es movilujo tiene un 50 % de descuento. Usar mínimo 3 constructores.

## Análisis del ejercicio
- Costo predeterminado del plan, generar un número telefónico random de 7 digítos con un prefijo random (300,313,321 etc.),
elejir aleatoriamente uno entre tres operadores, la cantidad de minutos hace que varíe el precio del plan, por último
reducir el precio a la mitad si el operador del plan es movilujo.
