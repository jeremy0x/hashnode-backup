# Building a Food Recipe App with Tailwind CSS and Vanilla JavaScript

### Introduction

I recently created a food recipe app using the Fetch API and Tailwind CSS. The project was inspired by a YouTube tutorial, which used vanilla CSS for styling. However, I wanted to challenge myself and use Tailwind CSS instead. Throughout the process, I encountered some issues that I had to troubleshoot, but overall, it was a great learning experience. If you're interested in learning more about how I built the app, read on! Additionally, I plan to build the same app with React.js in a few weeks, so stay tuned for that.

### Building the Project

I built the food recipe app using Tailwind CSS and Vanilla JavaScript. The purpose of this project was to create a platform where users can search for recipes based on ingredients while styling it with Tailwind CSS. You can view the project here - [**https://foodie-fetch.netlify.app/**](https://foodie-fetch.netlify.app/)

![website screenshot](https://github.com/jeremy0x/foodie-fetch/raw/main/src/img/project-screenshot.png align="left")

Styling the app with Tailwind CSS was pretty interesting, especially as someone who has always preferred vanilla CSS to Bootstrap. All through the process of building this app, I relied majorly on the Tailwind CSS documentation to style the project.

It was also an interesting challenge to use the Fetch API to search for recipes based on ingredients. This made me more confident in my JavaScript skills as I always thought I didn't know much about JavaScript, despite learning it for a long time.

### Challenges Faced

During the project's development, I faced several challenges that I had to overcome. One issue I encountered was with elements styled with Tailwind CSS that would be rendered from JavaScript. The selectors in the elements would not be included in the Tailwind build process, making the dynamically rendered elements look messy when they're rendered eventually.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677596487169/f2d3b745-6532-4d8b-a723-fb3bca2d31c7.png align="center")

The only fix I could think of for this was to include those elements in the default HTML and make them hidden so that the classes on the elements to be rendered would be on the Tailwind build process, and my elements would come out as expected.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677596719522/cb515f29-58aa-4503-852e-bec9a2e4fdf7.png align="center")

Another issue I faced was trying to store an array in a file and import it into another file. I wanted to use the `import` keyword in the file where the array would be used, but I got a syntax error because I initialized the app with npm, which by default uses CommonJS Modules. To try to fix the error (my knowledge of modules was limited at this point), I tried to follow the error fix recommendations by adding `"type": "module"` in my `package.json` file. However, this led to another issue where my Tailwind CSS wasn't applying the styles to the HTML file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677597037811/650035db-7f5f-4fb4-9018-8b2087dde20b.png align="center")

At first, I thought it was because of how I imported the CSS into the HTML, but it was all good. I double-checked my `tailwind.config.js` file, everything was okay there. I couldn't seem to make my Tailwind apply styles to my HTML.

So, I reinstalled Tailwind CSS and ran `npx tailwindcss init` again, which created a new config file but this time with the `cjs` file extension. I had no idea why the file extension was changed, but I eventually understood the difference between CommonJS Modules and ES6 Modules. I eventually converted my app back to a CommonJS module (I removed the `"type": "module"` from my `package.json`) and renamed my config file back to `tailwind.config.js`, and I was able to complete my project.

### Lessons Learned

While building this project, I learned several valuable lessons. I learned about the difference between CommonJS Modules and ES6 Modules and the importance of reading documentation and not relying solely on video tutorials. I also learned that sometimes, the best solution to a problem is to approach it from a different perspective.

### Conclusion

In conclusion, I was able to create a food recipe app with Tailwind CSS and Vanilla JavaScript. Through the challenges I faced during its development, I learned valuable lessons that have helped me grow as a developer. You can check out the project [here](**%5B%3Chttps://foodie-fetch.netlify.app/%3E%5D(%3Chttps://foodie-fetch.netlify.app/%3E)).

Thanks for reading!