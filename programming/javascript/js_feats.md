

ECMAScript

- varaible and test scopes
```js
{
//block scope
	// nested scope
}

function sum(a, b) {
// Function scope
	var myVar = 1;
}

// use let instead of var

// immutable
const answer = 42;

// the contents can be changes
const numbers = [2, 4, 5];
const person = {
	firstName: '',
	lastName: ''
}

```

- arrow functions
- regular function give access to their "calling" environment while arrow functions give access to their "defining" environment

```js
const X = function() => {
// this here is the caller of X
}

const Y = () => {
// it's the same "this" found in Y's scope
}


```

- object literal

```js
const obj = {
p1: 10,
p2: 20,
f2: () => {},
[mystery]: 42,

}
```

- destructuing

```js
const {PI, E, SQRT2}  = Math;


const circle = {
label: 'asd',
radius: 2
}

const circleArea = ({radius}, {precision = 2}) => (PI * radius * radius).toFixed(precision)

const [first, ...rest] = [10, 20, 23 , 23];

// copy array
// swallow coppies
const newArray = [...prevArray]
```


- template strings
```js
const myString = `hello ${myVar} from my string`
```

- classes
```js

class Person {
	constructor(name) {
		this.name = name;
	}
}


class Student extends Person {
	constructor(name) {
		super(name);
		this.grade = grade;
	}
}

```


- Promises and async/await

```js

const fetchData = async () => {
	const resp = await fetch('www');
	const data = await resp.json();

}
```