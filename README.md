# Captcha Image Generator

A simple captcha image generator.

## Install

Use `npm run captcha-image` or `yarn captcha-image` to install the package

## Usage

### React

```js
import Captcha from './Captcha';

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

## Options

You can pass following parameters to Captcha instance in order to generate custom Captcha image

- [font](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/font): '35px Arial'
- [align](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/textAlign): 'center'
- [baseline](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/textBaseline): 'middle
- width: 300
- height: 150
- bgColor: #eee
- color: #222

## Events

- createImage() method return HTML element parsed as String
