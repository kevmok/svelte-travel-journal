# Travel Journal Built with Svelte

Small svelte app that takes in an "API" and generates components from the data retrieved.
In this project that API is just a file called "data.js" that export a list with 3 objects that contain the data for each prop.

## Overview

### The Goal

User should be able to:

-   [x] Change the "API" data and modify the components generated
-   [x] Add more travel locations

### Demo

[Website Demo](https://svelte-travel-journal.vercel.app/)

## Screenshot

![App Screenshot](https://i.imgur.com/2AIplBD.jpg)

## My process

### Built with

-   Sveltejs/template
-   HTML markup
-   CSS
-   Javascript

### What I learned

-   How to work with a "fake" API and objects with svelte
-   #each blocks
-   Manipulating data

Compared to react instead of doing mappings with arrays you can use #each blocks and #if blocks to perform logic in your html markup.

```jsx
// Imported data array with objects
<script>
    import data from './data';
    import Navbar from './components/navbar.svelte';
    import Main from './components/Main.svelte';
</script>

// How to do it in React
function App(){
const travelData = data.map((item) => {
        return <Main key={item.id} {...item} />;
    });

    return (
        <div>
            <Navbar />
            {travelData}
        </div>
    );
}

// Svelte allows the user to not use array.prototype.map with each blocks
// How to do it in Svelte - much more simple

<div>
    <Navbar />
    {#each data as item}
        <Main {...item} />
    {/each}
</div>

```

## Installation

Clone this repository and install the dependencies...

```bash
  git clone https://github.com/kevmok/svelte-developer-card.git my-app
  cd my-app
  npm install
```

To run locally then start [Rollup](https://rollupjs.org)

```bash
npm run dev
```

## Author

-   Website - [kevinmok.com](https://kevinmok.com)
-   GitHub - [@kevmok](https://www.github.com/Kevmok)
-   Twitter - [@lkBoxer](https://www.github.com/lkBoxer)

## Acknowledgements

-   [Scrimba](https://scrimba.com) - I converted your React project to Svelte
-   [Svelte](https://svelte.dev/) - For the great tutorial page
