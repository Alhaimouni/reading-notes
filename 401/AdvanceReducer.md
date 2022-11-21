# Compined Reducers
<pre>Reducer is a pure function that takes the previous state and an action and returns the next state.

the action is an object that contains a type and a payload.

the state in a reducer is immutable and can’t be directly modified. </pre>

**immutable state**
---
If something is “immutable”, it can never be changed. State is immutable in that it can’t be changed directly but can be copied and changed.

**time travel in redux**
---
The Redux DevTools records dispatched actions and the state of the Redux store at every point in time.
This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app.

**action creator**
---
The only way to change the state is to dispatch an action, an object that describes what happened.

**reducer**
---
Reducers are pure functions that take the previous state and an action,
and return the next state. Like any other functions, you can split reducers into smaller functions to help do the work,
or write reusable reducers for common tasks.

**dispatch**
---
he Redux store has a method called dispatch. The only way to update the state is to call store.dispatch() and pass in an action object.

**Redux** 
---
Combined Reducers** -Is simply a utility function to simplify the most common use case when writing Redux reducers.
You are not required to use it in your own application, and it does not handle every possible scenario.

### There are several important ideas to be aware of when using combineReducers:

- First and foremost, combineReducers is simply a utility function to simplify the most common use case when writing Redux reducers. You are not required to use it in your own application, and it does not handle every possible scenario. It is entirely possible to write reducer logic without using it, and it is quite common to need to write custom reducer logic for cases that combineReducer does not handle. (See Beyond combineReducers for examples and suggestions.)

- While Redux itself is not opinionated about how your state is organized, combineReducers enforces several rules to help users avoid common errors. (See combineReducers for details.)

- One frequently asked question is whether Redux “calls all reducers” when dispatching an action. Since there really is only one root reducer function, the default answer is “no, it does not”. However, combineReducers has specific behavior that does work that way. In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. So, in that sense, using combineReducers does “call all reducers”, or at least all of the slice reducers it is wrapping.

- You can use it at all levels of your reducer structure, not just to create the root reducer. It’s very common to have multiple combined reducers in various places, which are composed together to create the root reducer.

### Any reducer passed to combineReducers must satisfy these rules:

- For any action that is not recognized, it must return the state given to it as the first argument.

- It must never return undefined. It is too easy to do this by mistake via an early return statement, so combineReducers throws if you do that instead of letting the error manifest itself somewhere else.

- If the state given to it is undefined, it must return the initial state for this specific reducer. According to the previous rule, the initial state must not be undefined either. It is handy to specify it with ES6 optional arguments syntax, but you can also explicitly check the first argument for being undefined.
