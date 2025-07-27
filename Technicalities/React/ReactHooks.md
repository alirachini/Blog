# 🪝 React Hooks Cheat Sheet

Master the most essential and advanced React hooks. Whether you're building a small component or an entire system, this guide keeps your hooks game tight.

---

<details>
<summary>🔁 useState – Track state</summary>

```js
import { useState } from 'react';

const Counter = () => {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
};
```
</details>

---

<details>
<summary>⚡ useEffect – Side effects, API calls, timers</summary>

```js
import { useEffect } from 'react';

useEffect(() => {
  console.log("Component mounted");

  return () => {
    console.log("Component unmounted");
  };
}, []); // dependency array
```
</details>

---

<details>
<summary>🎣 useRef – Mutable ref, no re-render</summary>

```js
import { useRef, useEffect } from 'react';

const Timer = () => {
  const intervalRef = useRef(null);

  useEffect(() => {
    intervalRef.current = setInterval(() => {
      console.log("Tick");
    }, 1000);

    return () => clearInterval(intervalRef.current);
  }, []);
};
```
</details>

---

<details>
<summary>🧠 useMemo – Memoize expensive calculation</summary>

```js
import { useMemo } from 'react';

const App = ({ items }) => {
  const expensiveCalc = useMemo(() => {
    return items.reduce((a, b) => a + b, 0);
  }, [items]);

  return <p>{expensiveCalc}</p>;
};
```
</details>

---

<details>
<summary>📦 useCallback – Memoize functions</summary>

```js
import { useCallback } from 'react';

const handleClick = useCallback(() => {
  console.log("Clicked!");
}, []);
```

Useful when passing functions to child components that rely on referential equality.
</details>

---

<details>
<summary>🔗 useContext – Global state (like theme, auth)</summary>

```js
const ThemeContext = createContext();

const App = () => (
  <ThemeContext.Provider value={"dark"}>
    <Child />
  </ThemeContext.Provider>
);

const Child = () => {
  const theme = useContext(ThemeContext);
  return <div>Current theme: {theme}</div>;
};
```
</details>

---

<details>
<summary>🧰 useReducer – Complex state logic</summary>

```js
const reducer = (state, action) => {
  switch(action.type) {
    case "INC": return { count: state.count + 1 };
    case "DEC": return { count: state.count - 1 };
    default: return state;
  }
};

const [state, dispatch] = useReducer(reducer, { count: 0 });

dispatch({ type: "INC" });
```

Use instead of `useState` when state logic gets complicated.
</details>

---

<details>
<summary>📞 useImperativeHandle – Expose functions to parent via ref</summary>

```js
const Child = forwardRef((props, ref) => {
  useImperativeHandle(ref, () => ({
    alertMessage() {
      alert("Called from parent");
    }
  }));
  return <div>Child</div>;
});

const Parent = () => {
  const childRef = useRef();
  return <button onClick={() => childRef.current.alertMessage()}>Call Child</button>;
};
```
</details>

---

<details>
<summary>🎯 useId (React 18+) – Unique IDs for accessibility</summary>

```js
const id = useId();

<label htmlFor={id}>Username</label>
<input id={id} />
```
</details>

---

<details>
<summary>🧬 Custom Hooks – Your own logic</summary>

```js
function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);
    window.addEventListener("resize", handleResize);
    return () => window.removeEventListener("resize", handleResize);
  }, []);

  return width;
}
```

Use like:

```js
const width = useWindowWidth();
```
</details>

---

> 💡 Pro Tip: Combine `useRef + useEffect + useCallback` for scroll, audio, or drag/drop handling.
>  
> ✨ Always name custom hooks like `useXyz` to keep the linter happy.

---

> Written with 💻 and ☕ by [AKR]
