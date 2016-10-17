## LBD 04-07-16 : Parte 1
### Programacion funcional y Object

#### Métodos del constructor Objeto (estáticos)	
- Primero es importante recordar que es un metodo estático y porque son importantes		
	 ```javascript
	function carFactory (color) {
		var distance = 0;
		
		return {
			color: color,
			getDistance: function () { // instance
				return distance;
			},
			setDistance: function (kms) { // instance
				distance = kms;
			}
		}
	}
	
	carFactory.distanceToMiles = function (kms) { // static
		return kms * 0.621371;
	}
	 ```
- ##### Object.keys(o)	
	Returns an array containing the names of all of the given object's own enumerable properties.	
	Ej 1:
	```javascript
	var arr = ['a', 'b', 'c'];
	console.log(Object.keys(arr)); // console: ['0', '1', '2']

	// array like object
	var obj = { 0: 'a', 1: 'b', 2: 'c' };
	console.log(Object.keys(obj)); // console: ['0', '1', '2']

	```
	VS **for in loop** retorna todas las propiedades del objeto + las
	que pertenecen a la cadena del prototipo
	
	Ej 2: Recorrer las props Objeto de manera segura:
	``` 
	Object.keys(myObj).forEach(x => console.log(x));
	```
- ##### Object.assign(target, ob1, ...)	
	Copia las propiedades propias y enumerables de varios objetos a target
	
	Ej 1:
	```javascript
	function copyObject (obj) {
		return Object.assign({}, obj);
	}
	
	var a = { a: 1 };
	var copy = copyObject(a);
	```
	
	
Fuente:	
Mozila MDN: [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
