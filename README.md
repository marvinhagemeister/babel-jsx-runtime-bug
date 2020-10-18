# Babel jsx-runtime bug

Steps to reproduce:

1. Clone repo
2. Run `yarn install`
3. Run `yarn build`
4. Open file `dist/index.js`

Expected output:

```jsx
import { jsx as _jsx } from "preact/jsx-runtime";
export const foo = _jsx("div", {});
```

Actual output:

```jsx
import { jsx as _jsx } from "preact/jsx-runtime.js";
export const foo = _jsx("div", {});
```
