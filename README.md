"This is my tech stack. There are many like it, but this one is mine."

# principles

## global
- data are event streams
- functions process data
- functions are pure
- functions are legible
- functions don't mutate data
- iteratively decompose complexity into simple pure functions
- separate reads from writes

## front
- should expect to be offline
- should be composed of pure components
- should manage state outside components
- should connect to a realtime API
- should look great on mobile, desktop and browser
- should be deep-linkable

## back
- should expose a realtime api
- should maintain an immutable event store as the single-source-of-truth
- should be composed of functions triggered by events
- each function should have its own exclusive datastore (table or database)
- should be observable through tracing

# Implementation

```javascript
const principles = Object.freeze({ ...global, ...front, ...back })

let implementation = []
```

In other words, the implementation of a principle should be viewed only as the best available approximation. Principles should change very little. Tools, frameworks and providers may change frequently.

## global
- javascript
- sanctuary
- fluture
- immutable
- immutable-ext

## front
- [cyclejs](https://cycle.js.org/)
- reactjs
- firebase
- service workers

## back
- google cloud firestore
- google cloud functions
- google cloud pub sub
- google cloud storage
- google cloud dataflow
- google cloud big query
- google cloud ml kit
