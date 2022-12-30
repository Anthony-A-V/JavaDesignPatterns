## 📌 Propósito

Abstract Factory es un patrón de diseño creacional que nos permite producir familias de objetos relacionados sin especificar sus clases concretas.

## 💡 Aplicabilidad
<p style="text-align: justify;">
Utiliza el patrón Abstract Factory cuando tu código deba funcionar con varias familias de productos relacionados, pero no desees que dependa de las clases concretas de esos productos, ya que puede ser que no los conozcas de antemano o sencillamente quieras permitir una futura extensibilidad.
</p>

<p style="text-align: justify;">
El patrón Abstract Factory nos ofrece una interfaz para crear objetos a partir de cada clase de la familia de productos. Mientras tu código cree objetos a través de esta interfaz, no tendrás que preocuparte por crear la variante errónea de un producto que no combine con los productos que ya ha creado tu aplicación.
</p>

* Considera la implementación del patrón Abstract Factory cuando tengas una clase con un grupo de métodos de fábrica que nublen su responsabilidad principal.


* En un programa bien diseñado cada clase es responsable tan solo de una cosa. Cuando una clase lidia con varios tipos de productos, puede ser que valga la pena extraer sus métodos de fábrica para ponerlos en una clase única de fábrica o una implementación completa del patrón Abstract Factory.


## 📝 Cómo implementarlo

1. Mapea una matriz de distintos tipos de productos frente a variantes de dichos productos.<br><br>
2. Declara interfaces abstractas de producto para todos los tipos de productos. Después haz que todas las clases concretas de productos implementen esas interfaces.<br><br>
3. Declara la interfaz de la fábrica abstracta con un grupo de métodos de creación para todos los productos abstractos.<br><br>
4. Implementa un grupo de clases concretas de fábrica, una por cada variante de producto.<br><br>
5. Crea un código de inicialización de la fábrica en algún punto de la aplicación. Deberá instanciar una de las clases concretas de la fábrica, dependiendo de la configuración de la aplicación o del entorno actual. Pasa este objeto de fábrica a todas las clases que construyen productos.<br><br>
6. Explora el código y encuentra todas las llamadas directas a constructores de producto. Sustitúyelas por llamadas al método de creación adecuado dentro del objeto de fábrica.

## 🚩 Pros y contras

### ✅ Pros

* Puedes tener la certeza de que los productos que obtienes de una fábrica son compatibles entre sí.<br></br>
* Evitas un acoplamiento fuerte entre productos concretos y el código cliente.<br></br>
* Principio de responsabilidad única. Puedes mover el código de creación de productos a un solo lugar, haciendo que el código sea más fácil de mantener.<br></br>
* Principio de abierto/cerrado. Puedes introducir nuevas variantes de productos sin descomponer el código cliente existente.

### ❎ Contras
* Puede ser que el código se complique más de lo que debería, ya que se introducen muchas nuevas interfaces y clases junto al patrón.

## 📔 Créditos
<a href="https://refactoring.guru/design-patterns"> https://refactoring.guru/design-patterns </a>
