
# SASS Import Once

  When included in a SASS module, sass-import-once will prevent the styles being duplicated if `@import` is called somewhere else. This is cool because it allows every SASS file to declare its own dependencies. This promotes encapulation and allows modules to standalone if need be.

## Installation

  Just copy the index.scss file somewhere into your project.

```
$ component install wilsonpage/sass-import-once
```

## Usage

```
$filename: 'defaults.scss';
@import 'sass-import-once';
@if not-imported($filename) {
/*******************************************/

html,
body {
  width: 100%;
  height: 100%;
}

body {
  background-color: #333;
}

/*******************************************/
}
```

## License

  MIT