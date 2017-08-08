## Redux is a predictable state container for JavaScript apps.
Basic principles:
  - hide logic from the components
  - provide a solution for the Model vs View Model gap

Main principles:
  1. everything that changes in the application AND the ui state is stored into the *state object/state tree*
  2. the state tree is read only
    - to modify the data, one dispatches an *action* (the minimal representation of the data change)
  3. state mutations need to be described as a pure function (called *reducer*)
    - newState = f(prevState, action)

Best practices:
  - make use of *presentational components*
  - make use of *functional components*



## Reducer
Is a pure update function, which describes how the next state should be calculated.

Conventions:
  - if the reducer receives an unknown/undefined action, it should return the current state
  - if the reducer receives an undefined state, it should return what it considers to be the initial state
  - use object literals shorthand notation for combined reducers

Best practices:

  - extract different reducers to smaller single purpose reducers (*reducer composition*)
  - use combineReducers() to combine reducers *duh*

## Store
Conventions:
  - must be initialized with a reducer function

Main functions:
  - getState() -> retrieves the current state
  - dispatch() -> dispatch actions to change the state
  - subscribe() -> register a callback listener called each time the state changes


## Best practices

Avoid array mutations in state:
  - use concat instead of push
  - use two slices instead of the splice method

and return a new array treating the old one as immutable

Use object property overwriting with Object.assign to change only the needed fields.

Credits, sources and some links of interest for further reading:
--
* https://egghead.io/lessons/javascript-redux-describing-state-changes-with-actions
* http://redux.js.org/docs/basics/
