# Clases en JavaScript

### ¿Qué son las clases en JavaScript?

En JavaScript, las clases nos permiten crear instancias de objetos con ciertas características. Una clase es una forma de organizar código de forma entendible con el objetivo de simplificar el funcionamiento de nuestro programa. 

Las clases nos permite crear herencia y trabajar de manera orientada a objetos.


En pocas palabras.... 

**Las clases nos permiten crear objetos de una forma más clara y nos permite trabajar de manera más sencilla la herencia.**

## Sintaxis de una Clase

La manera de crear una Clase es la siguiente: 

```javascript
class Persona {
	constructor(nombre, edad, frase) {
		this.nombre = nombre;
		this.edad = edad;
		this.frase = frase;
	}
	
	getInfo() {
		return `${this.nombre}, ${this.edad} años,  ${this.frase}`;
	}
}
```

Utilizamos la palabra reservada **class** para indicar que es una clase, seguido del nombre de la clase en este caso **Persona**, luego viene el **constructor()** con los argumentos que va a tener nuestro objeto, en este caso nuestra persona va a tener un nombre, edad y una frase.

Dentro del **constructor** debemos hacer referencia a esos paramentros usando **this**, en pocas palabras **this** hace referencia a la variable de la instancia dentro de la clase.

Tambíen podriamos definir nuestras variables del objeto de la siguiente manera: 

```javascript
class Persona {
	
	nombre;
	edad;
	frase;
	codigo;
	
	constructor(nombre, edad, frase) {
		this.nombre = nombre;
		this.edad = edad;
		this.frase =  frase;
	}
	
}
```

El **constructor** va a recibir los parametros recibidos y los va a asignar a las variables que creamos anteriorment, nota que no es necesario el uso de **let** o **const** , esto se debe al modo estricto de JS.

###### NOTA: El constructor siempre se va a ejecutar al crear una instancia de esa clase.
```javascript
class Figura {
	constructor() {
		console.log("Hola soy una el constructor de Figura");
	}
}

const rectangulo = new Figura();
console.log(rectangulo) // "Hola soy una el constructor de Figura"
```

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Instanciar o crear un objeto

Como mencionamos anteriormente, las clases nos permite crear varios objetos que heredan las mismas caracteriticas que definimos en el constructor.

```javascript
const maria = new Persona("Maria", 35, "Soy Maria y soy programadora");
```
Para crear ese objeto, se crea una constante que apunta una instancia de nuestra clase Persona, usando la palabra reservada **new** seguido del nombre de la clase, entre parentesis los elementos que va a tener nuestra persona en este caso: **nombre, edad y frase**

Podemos acceder a esas propiedades de la siguiente manera: 

```javascript
console.log(maria.nombre) // "Maria"
console.log(maria.edad) // 35
console.log(maria.frase) // "Soy Maria y soy programadora"
```

También podemos aceder a los métodos de la siguiente manera:

```javascript
maria.getInfo(): // "Maria, 35 años, Soy Maria y soy programadora"
```
