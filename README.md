# Repro
[issue-693](https://github.com/facebook/Docusaurus/issues/693)

## Quick Start

1. Clone the repository with `git clone --depth=1 https://github.com/joshuaalpuerto/repro-docusaurus.git`
2. `npm install`
3. will load `http://localhost:3000/docs/doc1.html`
4. change `website/siteConfig.js`

```js
const siteConfig = {
  baseUrl: '/project1/' // <-- change this from / to anything
  ...
}
```

5. stop `cmd + c` || `ctrl + c` and `npm start` again.