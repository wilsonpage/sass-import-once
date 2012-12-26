
# SASS Import Once

  When included in a SASS module, sass-import-once will prevent the styles being duplicated if `@import` is called somewhere else. This is cool because it allows every SASS file to declare its own dependencies. This promotes encapulation and allows modules to standalone if need be.

## Installation

  Just copy the index.scss file somewhere into your project.

  OR

```
$ component install wilsonpage/sass-import-once
```

## Usage

defaults.scss
```
$filename: 'defaults.scss';
@import 'sass-import-once';
@if not-imported($filename) {
/* ------------------------------------- */

h1 {
  color: red;
}

/* ------------------------------------- */
}
```

my-module.scss
```
@import 'defaults';

.my-module h1 {
  font-size: 40px;
}

```

another-module.scss
```
@import 'defaults';

.another-module h1 {
  font-size: 20px;
}
```

## License

  MIT