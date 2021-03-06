# Counter Test Example

This is an example app that lets you display a number based on a step selector component value.

## Demo

You can use a deployed version of the app [right here](https://unjavascripter.github.io/laboratoria-mentoring-test/index.html)

![Demo](https://user-images.githubusercontent.com/7959823/143093883-f973bba6-42a1-486f-bfcf-66f105085344.png)

![Demo video](https://user-images.githubusercontent.com/7959823/143094202-fb85af6c-6cd1-4619-82d6-2d8203592055.gif)

## Usage

Open the `index.html` file in any browser, then interact with the step selector to see the value change.

## Interesting stuff

### Custom event emitting

A custom event is emitted whenever the user interacts with an action element of the component. The emitted value matches the internally selected value of the component. 

```js
emitValue(value) {
  // Custom event emitter
  const event = new CustomEvent('change', {
    detail: {
      value // selected value
    },
    bubbles: true // will continue emitting
  });

  // Dispatches the event to be emitted to the parent
  this.dispatchEvent(event);
}
```