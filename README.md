# Repro
[issue-693](https://github.com/facebook/Docusaurus/issues/693)

## Quick Start

1. Clone the repository with `git clone git@github.com:joshuaalpuerto/repro-docusaurus.git`
2. `npm install`
2. `npm start`
3. will load `http://localhost:3000/docs/doc1.html`
4. change `website/siteConfig.js`

```js
const siteConfig = {
  baseUrl: '/project1/' // <-- change this from / to anything
  ...
}
```
5. stop `cmd + c` || `ctrl + c` and `npm start` again.

## UPDATE

It now works after changes to [Docusaurus](https://github.com/joshuaalpuerto/Docusaurus/tree/fix/base-url-broken-link)

1. Updated `website/package.json` point to my fork repo

```js
"docusaurus": "https://github.com/joshuaalpuerto/Docusaurus/tarball/fix/base-url-broken-link"
```

2. Updated `website/static/index.html` added `/project1/` to url

```html
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="refresh" content="0; url=/project1/docs/doc1.html">
    <script type="text/javascript">
      window.location.href = '/project1/docs/doc1.html';
    </script>
    <title>Test Repro issue</title>
  </head>
  <body>
    If you are not redirected automatically, follow this <a href="/project1/docs/doc1.html">link</a>.
  </body>
</html>
```


