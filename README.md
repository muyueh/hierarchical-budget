# Hierarchical bar chart

https://observablehq.com/@d3/hierarchical-bar-chart@369

View this notebook in your browser by running a web server in this folder. For
example:

~~~sh
npx http-server
~~~

Or, use the [Observable Runtime](https://github.com/observablehq/runtime) to
import this module directly into your application. To npm install:

~~~sh
npm install @observablehq/runtime@5
npm install https://api.observablehq.com/d/0b07c3790ae4af2c@369.tgz?v=3
~~~

Then, import your notebook and the runtime as:

~~~js
import {Runtime, Inspector} from "@observablehq/runtime";
import define from "@d3/hierarchical-bar-chart";
~~~

To log the value of the cell named “foo”:

~~~js
const runtime = new Runtime();
const main = runtime.module(define);
main.value("foo").then(value => console.log(value));
~~~

## Deployment

This repository is set up to publish the static demo to GitHub Pages using
GitHub Actions:

- Pushing to the `main` branch runs the Pages workflow and publishes the
  contents of the repository root.
- You can also trigger the deployment manually from the Actions tab using the
  **Deploy static site to Pages** workflow.
- The deployment URL is exposed through the `github-pages` environment once the
  workflow finishes successfully.
