# Workshop

A simple, light, JS library to simplify your life.

## Extensions

### `DOM`

#### `#getElementsByAttribute(attribute, type)`

Gets all DOM elements which attribute `attribute` equals `type`.

#### `#getElementsByAttributeName(name, type)`

Gets all DOM elements which have an attribute named `name` and are of type `type`, (EG: 'div').

### `Object`

#### `Object.equals(obj1, obj2)`

Checks if two objects are equal, checks are performed on both senses (obj1 == obj2 and obj2 == obj1);

#### `Object.isStrictlyEqual(obj1, obj2)`

Checks if two objects are strictly equal, checks are performed on both senses (obj1 === obj2 and obj2 === obj1). Does not check recurrently

#### `Object.duplicate(obj)`

Returns a copy of an object.

#### `Object.compare(obj1, obj2, fiels)`

Compares two objects only on the given fields.

#### `Object.sort(obj)`

Returns a new object with the keys sorted.

### `Array`

#### `#findObjectsByProperty(prop, value)`

Searches in an array of objects for objects which `prop` equals `value`

#### `#lastIndexByProperty(prop, value)`

Searches in an array of objects for the last object which `prop` equals `value`

#### `#firstIndexByProperty(prop, value)`

Searches in an array of objects for the first object which `prop` equals `value`

#### GETTER / SETTER `#last`

Returns/Sets the last object of an array

#### `#isUnique()`

Checks for duplicates in array. Returns true if no duplicates are found

#### `#duplicate()`

Returns an identical array

### `Workshop`

#### `Workshop.ajax(params, callback)`

Performs an HTTP request. Params are: `url`, `method`, `data`, `headers`. Callback is of the type `function(err, res, xhr)`, where `xhr` is the `XMLHttpRequest` object generated.

#### `Workshop.getDeviceOrientation(callback)`

Sets a listener for changes on device orientation. Please check MDNs documentation for the `deviceorientation` event.

#### `Workshop.getDeviceMotion(callback)`

Sets a listener for changes on device motion. Please check MDNs documentation for the `devicemotion` event.

#### `Workshop.getDeviceMovement(callback)`

Adds listeners for both device orientation and motion. Callback takes an object which can be one of both:

```
{
	alpha:,
	beta:,
	gamma
}
```
or
```
{
	acceleration:,
	gravity
}
```

#### `Workshop.getGeolocation(callback, error)`

Gets device geolocation an passes it to callback. If an error, executes the `error` function.

### `Events`

Objects are now equipped with a utility function `onWSEvent`

#### `Object#onWSEvent(events, callback)`

Sets a listener on given object for `events`, which can be an array of named events, or a single string for a single event. Passes the result to `callback` whenever the event is triggered.

#### `Workshop.events.add(event, force)`

Adds an event to the list of possible events. Force overwrites an event if already present.


#### `Workshop.events.emit(event, data)`

Emits an event with given data. Triggered event will be passed to listeners.










