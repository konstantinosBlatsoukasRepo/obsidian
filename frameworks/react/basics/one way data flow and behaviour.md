
```js

/*
  Write JavaScript/React code here and press Ctrl+Enter to execute.

  Try: mountNode.innerHTML = 'Hello World!';
   Or: root.render(<h2>Hello React!</h2>);
*/

// event handler
function logRandom() {
  console.log(Math.random());
}

function Button(props) {
  return (
  <button onClick={props.onClickFunction}>+1</button>
  );
}

//Display
function Display(props) {
  return (
    <div>{props.message}</div>
  );
}

function App() {
    const [counter, setCounter] = useState(42);
    const incrementCounter = () => setCounter(counter + 1);
    return  (
      <div>
        <Button onClickFunction={incrementCounter}/>
        <Display message={counter}/>
      </div>
    )
}

ReactDOM.render(
  <App />,
  document.getElementById('mountNode'),
)


```