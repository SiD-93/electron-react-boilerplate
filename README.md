# electron-react-boilerplate

Inspired by the [`electron-jsx-babel-boilerplate`](https://github.com/paulcbetts/electron-jsx-babel-boilerplate) by @paulcbetts.

I recently stumbled upon the [`electron-compile`](https://github.com/electron/electron-compile) and [`electron-prebuilt-compile`](https://github.com/paulcbetts/electron-prebuilt-compile) projects when I was looking for a quick way to get started with Electron.
These projects make developing Electron apps much easier. Do check these out if you haven't already!

## Installation and running

- Fork/clone/download this repo and place it wherever you like.
- Edit the `name` field of `package.json` to the name of your app.
- Run `npm install` and wait for it to finish.
- Provided everything installed alright, run the app with `npm start`.


## Code Structure

This rudimentary React+Electron app is structured like this:

```text
your-app-name/
├── node_modules/
├── package.json
├── src/
│   ├── components/
│   │   └── Main.js
│   ├── index.js
│   ├── index.html
│   └── app.js
├── .compilerc
└── README.md
```

(Phew! Took me quite a bit of copy-pasting to get that tree :joy: ).

## High-level walkthrough

- Alright, the `src/app.js` file is where all the magic begins. This file has the [Electron API](http://electron.atom.io/docs/api/) code and it kicks off the `main` process of the whole app. **[Basic info on Electron processes here](http://electron.atom.io/docs/tutorial/quick-start/).**


- The `src/index.html` file starts the `renderer` process.
  - You can include stylesheets, scripts and other stuff in here just like you would in a regular HTML file without the need for a separate cross-compilation step!  **[Why?!? How!?! Read this](https://github.com/electron/electron-compile).**


- The `src/index.js` file is where our React component is mounted. **Be sure to include this script in the HTML file of the renderer process.**


- The `components` directory inside `src/` is where all of the React code (JSX) lives.

- The `.compilerc` file in the topmost directory handles the compilation of our ES6 and other (LESS, Jade/Pug, etc.) files.

## Current state

In its current state, this boilerplate is sufficient to create small, _non-trivial_ apps using React and Electron without the hassle/benefits/headache/awesomeness of a tool such as `Webpack`.

I plan to evaluate some tools (~~React Router~~ (added), Express, etc.) to be able to make more complex apps and I'll add them to this when I get them working.
But some advanced boilerplates can already do this (one with the exact same name as this repo :sweat_smile:)

Let's see how it goes :smile:
