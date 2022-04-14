# CS20 Vue Template

This template should help get you started developing with Vue.

## Project Setup

- Clone the project to your computer
- navigate the terminal into the project folder
- install npm dependencies
- open project folder in VSCode

```sh
git clone <YOUR_PROJECT_URL_HERE>
cd <YOUR_PROJECT_FOLDER_NAME>
npm install
code .
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Get To Know the Setup

Explore the `src` folder to get a feel for how things are structured in VueJS as well as some of the functionality that Vue gives us.

#### File Structure

`main.js` is the entry point for the whole page. Unless you are installing additional libraries (eg. vue-router), you shouldn't need to edit this.

`App.vue` is the top-level Vue component, being used here to define the overall structure of the page by building together sub-components `MyHeader.vue` and `HelloWorld.vue`.

`MyHeader.vue` is just some HTML and CSS, nothing fancy here.

`HelloWorld.vue` makes up the rest of the page and demonstrates some of VueJS's handy tools. The `<script>` section defines some _reactive_ variables in the `data()` function, which lets us access these variables in the `<template>` HTML section.

#### Using Reactive Data

Reactive data can be _interpolated_ into the inner HTML of elements using double curly-brackets: `{{ myVar }}`

In fact, you can place any valid javascript expressions inside the {{ }} and the result will be rendered, eg `{{ !showIcons ? "Show" : "Hide" }} Icons` will render to "Show Icons" or "Hide Icons" depending on the state of the showIcons variable.

You can also use _reactive data_ as the value for HTML attributes (things like `src=".."` or `href="..."` ) using **v-bind** (eg `v-bind:src="myVar"` or using the shorthand `:href="myVar"`).

#### Binding Functions to Events

The button in `HelloWorld.vue` uses `v-on:click` to bind the `toggleIcons` function (defined in the `methods` option of the `<script>` section) to the **click** event of the button. This also has a shorthand version and can be replaced with `@click="toggleIcons"`.

`v-on` can be used to bind functions to any of the default HTML events (and custom events if you want to go down that rabbit hole...).

#### Looping

`HelloWorld.vue` uses the `v-for` attribute on the `<IconCard>` element to make an IconCard for each object in the `icons` array, and uses `v-bind` to pass the data for each icon into the `<IconCard>` component.

#### Sub Component Props

`IconCard.vue` defines an individual card and uses the `props` option in the `<script>` section to define the custom attributes `title` and `image`, so the parent component can pass in data.

### Additional Topics to Explore

This template includes examples of only a small slice of the functionality built into VueJS. Check the [official docs](https://vuejs.org/guide/introduction.html) for more details, but some useful things you may want to explore are:

- [Computed Properties](https://vuejs.org/guide/essentials/computed.html)
- [Binding Classes and Styles for Dynamic CSS](https://vuejs.org/guide/essentials/class-and-style.html)
- [2-Way Bindings for Input Elements](https://vuejs.org/guide/essentials/forms.html)
- [Lifecycle Hooks](https://vuejs.org/guide/essentials/lifecycle.html)
- [Animate Elements Entering & Leaving](https://vuejs.org/guide/built-ins/transition.html)
