# What is API ? How to use it ?
A simple note and example for learning what a API is ?

 - In computer programming, an `application programming interface` `(API)` is a communication protocols.
 - In general terms, it is a set of clearly defined methods of communication between various components.

## How to use the HTTP request GET with JavaScript
 [Example code](https://d50000.github.io/What-is-API-How-to-use-it-/)with pure JavaScript.
 
```
// Create a request variable and assign a new XMLHttpRequest object to it. It's same as  jQuery $.ajax .
let request = new XMLHttpRequest();
// Open a new connection, using the GET request on the URL endpoint
request.open('GET', 'https://api.coinmarketcap.com/v2/ticker/', true);
// Send request
request.send();

request.onload = function () {
    // Response prototype will be object.
	let apiResult = JSON.parse(this.response);
	if (request.status == 200) {
		// code here to do something.....
		
	} else {
		console.log(`Something Wrong, error code: ${request.status}.`);
	}
};
```
 

### Reference:
 - https://www.taniarascia.com/how-to-connect-to-an-api-with-javascript/
 - https://medium.freecodecamp.org/javascript-from-callbacks-to-async-await-1cc090ddad99
