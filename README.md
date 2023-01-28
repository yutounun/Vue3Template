# Vue3TemplateWithFireBase

This is a template repository which I can utilize when I create an app using Vue3 with TypeScript, Firebase, Tailwind css, CI/CD with github actions...

## ※Caution

You do need to change some configs on `.firebaserc`and `firebase/init.ts` to connect with a new project on Firebase.

## Design

Use Figma.

## Project Setup

```sh
git clone https://github.com/team-agile-div/toyota-wg3trip.git
npm ci
```

### Compile and Hot-Reload for Local Enviroment

```sh
npm run local
```

Also, you can do it by running a build task with `cmd + shift + b`

### Confirm on a mobile

Make sure to utilize the same Wifi as PC does

```sh
npm run local
```

1. Take a note the url coming after `Network: ...`
2. type the url including a port number on the address bar.

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Run Unit Tests with [Vitest](https://vitest.dev/)

```sh
npm run test:unit
```

### Run End-to-End Tests with [Playwright](https://playwright.dev)

```sh
# Install browsers for the first run
npx playwright install

# When testing on CI, must build the project first
npm run build

# Runs the end-to-end tests
npm run test:e2e
# Runs the tests only on Chromium
npm run test:e2e -- --project=chromium
# Runs the tests of a specific file
npm run test:e2e -- tests/example.spec.ts
# Runs the tests in debug mode
npm run test:e2e -- --debug
```

## Coding guide

### direcotry structure

Use Atomic design which helps developers to read code easily and also not to lose where to create component files and direcories.

#### Atoms

Represent the basic building blocks of a design system. An example is a button or a text style.

#### Molecules

A group of atoms working together as a unit. Molecules are tangible UI elements. For example, a button and text field can be grouped to create a search form.

##### Organisms

Atoms and molecules working together in a complex structure. A search field grouped with a navigation bar forms a header organism on a website.
Only this component can inherit from a same level of a organism component.

##### Templates

Page-level objects placing components into a layout that defines the content structure. For example, taking a header organism and placing it on a homepage template.

##### Pages

Instances of templates that represent the final product.

## Deploy

Run by [GitHub Actions](https://github.com/staqct/ssap-partner-portal-fo-frontend/actions)

## Style check and Build check

Run by [GitHub Actions](https://github.com/staqct/ssap-partner-portal-fo-frontend/actions)
