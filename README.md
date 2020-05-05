## AppRun Example for IE 11


To use AppRun for applications that support IE 11, you will need:

1. Polyfills for _Promise_ and _string.startsWith_ , e.g., using https://polyfill.io
```
  <script src="https://polyfill.io/v3/polyfill.min.js?features=String.prototype.startsWith%2CPromise"></script>
```

2. Use _window.onhashchange_ in main.tsx
```
if (!window.onpopstate) window.onhashchange = () => app.route(location.hash);
```

* Use _npm start_ to start the dev server
* Use _npm run build_ to build for production

This is an application built with [AppRun](https://github.com/yysun/apprun).