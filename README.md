## Demo


## Install

```sh
npm install qr-code

或者

yarn add qr-code
```

## Usage

```js
import 'qrcode-puge'
```

```html
<qr-code data="hello world!"></qr-code>
```

## Options

Attribute       | Options                   | Default             | Description
---             | ---                       | ---                 | ---
`data`          | *string*                  | `null`              | The information encoded by the QR code.
`format`        | `png`, `html`, `svg`      | `png`               | Format of the QR code rendered inside the component.
`modulesize`    | *int*                     | `5`                 | Size of the modules in *pixels*.
`margin`        | *int*                     | `4`                 | Margin of the QR code in *modules*.