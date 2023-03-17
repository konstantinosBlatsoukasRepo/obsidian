
```js
function logRandom() {
	console.log(Math.random());
}

function Button() {
  return <button onClick={logRandom}>Test</button>;
}

ReactDOM.render(
  <Button />,
  document.getElementById('mountNode'),
)
```