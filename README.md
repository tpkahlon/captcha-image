# Captcha Image Generator

A simple captcha image generator.

## Install

- `npm install captcha-image`
- `yarn add captcha-image`

## Example

Play with sandbox example here: [Demo](https://codesandbox.io/s/focused-butterfly-qv2go?file=/src/App.js)

## Options

You can pass following parameters to Captcha instance in order to generate custom Captcha image

| Attributes                                                                                                  | Values       |
| ----------------------------------------------------------------------------------------------------------- | ------------ |
| [font](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/font) / String             | '35px Arial' |
| [align](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/textAlign) / String       | 'center'     |
| [baseline](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/textBaseline) / String | 'middle      |
| width / Number                                                                                              | 300          |
| height / Number                                                                                             | 150          |
| bgColor / String                                                                                            | #eee         |
| color / String                                                                                              | #222         |

## Events

- createImage() method return HTML element parsed as String

## Output

Final outcome looks like this:

```html
<img src="..." data-key="..." />
```

## Demo Usage

### React

```js
import Captcha from 'captcha-image';

const captchaImage = new Captcha(
  '35px Arial',
  'center',
  'middle',
  300,
  150,
  '#eee',
  '#111'
).createImage();

function createMarkup(source) {
  return { __html: source };
}

function MyCaptcha() {
  return <div dangerouslySetInnerHTML={createMarkup(captchaImage)} />;
}

function App() {
  return (
    <div className='App'>
      <MyCaptcha />
    </div>
  );
}

export default App;
```
