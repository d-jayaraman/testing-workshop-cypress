# testing-workshop-cypress

> A 3-4 hour testing workshop complete with application, exercise tests and speaker slides

## Requirements

- any computer: Mac, Windows, Linux
- Node 6+
- git

## Application

Vue.js + Vuex + REST server application we are going to test is in folder `todomvc`. This application and its full testing was described in [this blog post](https://www.cypress.io/blog/2017/11/28/testing-vue-web-application-with-vuex-data-store-and-rest-backend/)

## Slides

[https://gitpitch.com/cypress-io/testing-workshop-cypress][presentation] with the starting file in [PITCHME.md](PITCHME.md) presented using [GitPitch](https://gitpitch.com/). The pitch file includes files from the [slides](slides) folder. Students should open the [presentation slides][presentation] and follow along.

[presentation]: https://gitpitch.com/cypress-io/testing-workshop-cypress

## Content

| topics                                 | folder                                                                                   | slides                                                        |
| -------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| introduction, TodoMVC application      | [todomvc](todomvc)                                                                       | [intro.md](slides/intro.md)                                   |
| loading page                           | [00-start](00-start)                                                                     | [00-start.md](slides/00-start.md)                             |
| `cypress open` vs `cypress run`        | [cypress/integration/01-basic](cypress/integration/01-basic)                             | [01-basic.md](slides/01-basic.md)                             |
| adding items test, `cypress.json` file | [cypress/integration/02-adding-items](cypress/integration/02-adding-items)               | [02-adding-items.md](slides/02-adding-items.md)               |
| selector playground                    | [cypress/integration/03-selector-playground](cypress/integration/03-selector-playground) | [03-selector-playground.md](slides/03-selector-playground.md) |
| reset database using `cy.request`      | [cypress/integration/04-reset-state](cypress/integration/04-reset-state)                 | [04-reset-state.md](slides/04-reset-state.md)                 |
| spy and stub XHR requests, fixtures    | [cypress/integration/05-xhr](cypress/integration/05-xhr)                                 | [05-xhr.md](slides/05-xhr.md)                                 |
| access application code and data       | [cypress/integration/06-app-data-store](cypress/integration/06-app-data-store)           | [06-app-data-store.md](slides/06-app-data-store.md)           |
| setting up E2E tests on CI             | [cypress/integration/07-ci](cypress/integration/07-ci)                                   | [07-ci.md](slides/07-ci.md)                                   |
| setting up Cypress dashboard           | [cypress/integration/07-ci](cypress/integration/07-ci)                                   | [08-dashboard.md](slides/08-dashboard.md)                     |
| the end                                | -                                                                                        | [end.md](slides/end.md)                                       |

## For speakers

During a testing workshop in Boston I have covered this material in 3 hours (with 25 minute lunch break). Everyone worked or coded for the most part, except for CI and the Cypress dashboard sections, which I simply showed via slides and actual sites.

During the workshop, keep `todomvc` app running in one shell, while each section `01-basic`, `02-...`, `03-...` etc. has its own Cypress and specs subfolders `cypress/integration/...`. Usually a spec has several tests with placeholder comments. The workshop attendees are expected to make the tests pass using the knowledge from slides and hints (and Cypress documentation). Note that most folders have prepared `spec.js` file and `answer.js` file. The `answer.js` file is ignored by Cypress using a setting in `cypress.json`.

The only exception is the folder `00-start`. This is a folder for students to see how Cypress scaffolds example specs when you open Cypress the very first time. In this folder students should execute

```
cd 00-start
npm run cy:open
```

and see the list of created example specs.

The slides can be shown directly via the [presentation link][presentation] above. The Markdown files in [slides](slides) folder also has a little bit of speaker notes.
