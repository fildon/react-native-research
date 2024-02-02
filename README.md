# React Native Research

A simple "hello world" for react-native, to identify obstacles and opportunities.

## Prerequisites

- Node
- Project dependencies
    - > npm i

## Running Locally

> npx expo start

When terminal is ready, press `w` to open the web app.

HMR is enabled, so you should see code changes reflected in the browser instantly.

## Findings So Far

🔶 `react-native` styling is unit-less. This will limit capabilities for spacing and layout of web designs.

🟥 `react-native-web` handles mapping `react-native` components into HTML DOM elements. However most of the time this appears to only output `div`s. This is antithetical to HTML semantics. We can claw back some semantics thanks to [react-native-web | Semantic HTML](https://necolas.github.io/react-native-web/docs/accessibility/#semantic-html), however this is very limited. There are over 150 different HTML elements but `react-native-web` supports mapping to only about 20 of them: [GitHub | propsToAccessibilityComponent](https://github.com/necolas/react-native-web/blob/e8a0cbc60af40bdac6505704ffe34764267cd77f/packages/react-native-web/src/modules/AccessibilityUtil/propsToAccessibilityComponent.js#L12). It is unlikely for this to ever improve, since cross-compatibility requires that any given component within `react-native` must have a way to render on all platforms. For example there is no `react-native` `table` component, because there is no sensible render target for mobile apps. Citation: [GitHub issues | Rejected support for `table` element](https://github.com/necolas/react-native-web/issues/2511#issuecomment-1514844650)

## Open Questions

- [ ] What is TypeScript support like?
