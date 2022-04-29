---
title: Bypass useEffect on Mount with useRef
date: '2022-04-29'
draft: false
author: Petri Huhtanen
tags:
  - React
  - Hooks
slug: react-useref
---

As the documentation of React states, [Hooks](https://reactjs.org/docs/hooks-intro.html) "let you use state and other React features without writing a class." The [useState](https://reactjs.org/docs/hooks-state.html) Hook is used to manage the state of a component. If you need to do some data fetching, the [useEffect](https://reactjs.org/docs/hooks-effect.html) Hook is the one to use. It's default behaviour for React to run the Effect Hooks after every render. This always includes the first render, too. There might be use cases, when one wants to fetch some data, but only after e.g. the user presses a button. How can this be handled in React?

Here is a solution that uses the [useRef](https://reactjs.org/docs/hooks-reference.html#useref) Hook on tracking the button press. This has an advantage over using `useState` as mutating the `current` property doesn't cause a re-render. This should be a minimal working solution to use in `App.js`. I'd like to point out that it was inspired by Caleb Benjamin's [post](https://dev.to/calebbenjin/how-to-prevent-useeffect-from-running-on-initial-render-in-react-22a8) that helped me figure out, how the useRef Hook works.

{{< highlight react >}}

import React, {
    useEffect,
    useRef,
    useState
  } from 'react';
  
  export default function App() {
    const [data, setData] = useState(null);
    const [id, setId] = useState(0);
    const pressedRef = useRef(false);
  
    const handleGetData = () => {
      pressedRef.current = true;
      setId(id + 1);
    };
  
    const handleHideData = () => {
      setData(null);
    };
  
    useEffect(() => {
      if (pressedRef.current) {
        fetch(`https://jsonplaceholder.typicode.com/todos/${id}`)
          .then(response => response.json())
          .then(json => {
            setData(json);
            pressedRef.current = false;
          })
          .catch(err => console.log(err))
      }
    }, [id]);
  
    return (
      <>
        <p>{data ? JSON.stringify(data) : ""}</p>
        <button onClick={handleGetData}>Get Next Todo</button>
        <button onClick={handleHideData}>Hide Todo</button>
      </>
    );
  }

{{< / highlight >}}
