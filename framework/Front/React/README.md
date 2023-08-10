# React

React est une libraire javascript, créée en 2011 par Facebook et c'est la librairie la plus utilisée du moment.

# Installation

il existe 2 façon d'installer React :

## React app

- `npx create-react-app my-app`

- cd `nom-du-projet`

- `npm start`

## Vite

- `Vite` npm create vite@latest

`vite` est plus rapide et viens avec des paquets plus léger

- `ok to proceed (y)`

- `Project name`

- `package name`

- `Select a framework` > React

- `Select a variant` > typescript ou javascript

Ensuite :

- cd `nom du projet`

- npm install

- npm run dev

# Router

- `npm install react-router-dom`

- Creation des dossiers `pages` avec Home.js / Contact.js / About.js et `components` avec Header.js

Dans Header.js faire l'import de `NavLink` puis ajouter les redirections (non fonctionelle pour le moment)

```js
export default function Header() {
  <>
    <h1>React: react router</h1>
    <NavLink to="/home">Home</NavLink>
    <NavLink to="/contact">Contact</NavLink>
    <NavLink to="/about">About</NavLink>
  </>;
}
```

Ensuite importer le Header dans toutes les pages nécessaires.

- dans `App.js` faire un import de BrowserRouter, Routes && Route

```js
import { BrowserRouter, Routes, Route } from "react-router-dom";
```

puis importer toutes les pages.

```js
import Home from "./pages/Home";
import Contact from "./pages/Contact";
import About from "./pages/About";
```

Une fois toutes les pages importées, il suffit de faire comme ci-dessous et le tour est joué.

```js
<BrowserRouter>
  <Routes>
    <Route index element={<Home />} />
    <Route path="/home" element={<Home />} />
    <Route path="/contact" element={<Contact />} />
    <Route path="/about" element={<About />} />
    <Route path="*" element={<Nopage />} />
  </Routes>
</BrowserRouter>
```
