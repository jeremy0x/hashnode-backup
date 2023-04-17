---
title: "React Dictionary App with TypeScript & Tailwind"
datePublished: Mon Apr 17 2023 23:17:35 GMT+0000 (Coordinated Universal Time)
cuid: clglghr1l000109l91fiahknn
slug: react-dictionary-app
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681390004973/af70eea7-9d75-4515-ab90-2ec977fe9af8.png
tags: sass, web-development, reactjs, tailwind-css, vite

---

## Introduction

Building a dictionary web app is an exciting project, not just because of its functionality but also its design. In this blog post, I'll document my experience building LingoLookup, a dictionary web app that allows users to search for word definitions.

The app was built using React with TypeScript, Tailwind CSS for styling, and sprinkles of SCSS.

To fetch the definitions of words, I used the [Free Dictionary API](https://dictionaryapi.dev). This API provides a rich source of word data, including definitions, pronunciations, and examples of how to use the word in a sentence. You can learn more about this API by visiting [dictionaryapi.dev](https://dictionaryapi.dev).

The project's look was inspired by a dribbble design I came across while looking for a good design to implement in my project. Check it out [here](https://dribbble.com/shots/7114674-Online-dictionary/attachments/117412?mode=media).

## Project Setup

This project was built using React with TypeScript, Tailwind CSS, and SCSS, and the React app was created with [Vite](https://tailwindcss.com/docs/guides/vite).

After setting up the repository, I removed the default files and codes I didn't need. To speed up the setup, I used my cleaned-up repository, which already had Tailwind CSS set up as a template. It also had the [prettier-plugin-tailwindcss](https://github.com/tailwindlabs/prettier-plugin-tailwindcss) package installed for automatic class sorting. Check out the repository [here](https://github.com/jeremy0x/vite-react-ts-scss-tailwind-boilerplate) and consider giving it a star if it helps.

## Building

The first step was to add a favicon that represented a dictionary app. I chose a search icon to reflect the app's search functionality. I used the [favicon.io](http://favicon.io) favicon generator to create the favicon with specific dimensions.

Next, I gathered the necessary assets, including animations for the loading state, unavailable word definitions, and error states. I found animations on [lottiefiles.com](http://lottiefiles.com), which offers numerous animations for websites, all for free.

![Error state of LingoLookup when a word definition isn't found.](https://cdn.hashnode.com/res/hashnode/image/upload/v1681768721200/5e2e3368-ecf8-4189-a1bb-3e4404ec9a1e.gif align="center")

You can check out the project for the search animation and error animation. I get these animations from this amazing website - [https://lottiefiles.com/](https://lottiefiles.com/). Here, you can get tons of animations for your website all for free.

### Functionality

I focused on getting the functionality working first before moving on to the design. I implemented fetching and ensured it was properly set up by logging out the data to the console. Once set up, I proceeded to display the data.

I stored the data in a state to make it available throughout the component. I used states to handle when the data was fetching, when there was an error, or when the definition couldn't be found. I used the [logical AND](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND) operator to display different elements/contents depending on the status.

To display the word details, I used the map function for words with more than one definition or other similar properties. I also used the [logical AND](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND) operator to check if a property existed for a word to avoid displaying empty elements on the page.

### Design

Designing the app was the most time-consuming aspect of the project. I aimed to create an aesthetically pleasing app with a cool and interesting look. Building the layout like a table and ensuring mobile responsiveness was the most challenging part of the project.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681770640796/637dc63d-7d70-4903-b149-556053c61be6.png align="center")

I used Tailwind CSS to style the project, which helped me learn more about the framework. My first project with Tailwind CSS was a [Food Recipe App](https://foodie-fetch.netlify.app), and I have improved at writing Tailwind CSS while building these projects.

## Conclusion

Building LingoLookup was an enjoyable and challenging experience aimed at creating a visually appealing and user-friendly dictionary web app. The source code for the project can be found on GitHub at [github.com/jeremy0x/lingo-lookup/](https://github.com/jeremy0x/lingo-lookup/).

In this post, I have included links to MDN Web Docs where necessary to explain certain concepts. Additionally, after receiving feedback from [Daniil Molodkov](https://adplist.org/mentors/daniil-molodkov), an amazing mentor I met on ADPList, I plan to optimize the codebase by separating the contents of the \`Main.tsx\` component into smaller components. This will make the code more organized and easier to maintain.

Thank you for reading!