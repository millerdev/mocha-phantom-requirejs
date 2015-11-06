# A test for mocha-phantomjs with require.js

The issue: https://github.com/nathanboktae/mocha-phantomjs/issues/215

- Clone this repo
- Run `npm install`
- Open `index.html` in a browser and verify that the tests run.
- Run `./node_modules/.bin/mocha-phantomjs --bail index.html`
```
$ ./node_modules/.bin/mocha-phantomjs --bail index.html
mocha was not initialized before the page finished loading. Make sure to include mocha.js as a direct script and call `mocha.ui` or `mocha.setup`.
```

Uncomment `<script>mocha.setup('bdd');</script>` in `index.html` to make
`mocha-phantomjs` work as expected.
