# My Safari Compatibility Experience: Solving Text Gradient and Image Height Issues

As a front-end developer, I've had my fair share of challenges with browser compatibility. One browser, in particular, has given me some unexpected issues Safari. In this post, I want to share two specific issues I encountered while developing websites and the solutions I found to resolve them.

### The Issue with Text Gradients

The first issue I encountered was with text gradients. I was using `webkit-text-fill-color: transparent;` to create a gradient effect, but the output on Safari was unexpected and hilarious. I later discovered that in mobile Safari, the keyword `transparent` doesn't work, and `rgba(255, 255, 255, 0)` should be used instead (more info [here](https://stackoverflow.com/a/27118826)). It was a small change, but it made a big difference in getting the expected result.

The image below shows what I expected and the output on other devices, where everything looked perfect.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676761335081/34e623ad-d26a-4efa-ae8e-8f57d1913fbe.png align="center")

However, when I opened the website on an iPhone's Safari browser, I was in for a shock.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676761381830/a5bc79d8-5a59-4f47-b796-6ef2acee5fe3.png align="center")

### Unexpected and Hilarious Image Height Issues

The second issue I encountered was with the height of an image in a slider. I was using `height: 100%;` which worked fine on most devices, but not on iOS. After some thought, I discovered changing the `height` to `auto` could resolve the issue, and it did.

[![Git commit diff showing change from `height: 100%;` to `height: auto;`.](https://cdn.hashnode.com/res/hashnode/image/upload/v1676762168680/914672da-a69a-4142-abfd-e7c82e64f35e.png align="center")](https://github.com/VictorJoey/Sesshin/pull/25/commits/ed9025654b2853911653532a7bac07aec90659e2)

The image below shows what I expected to see, and the output on other devices where everything looked perfect.

![Expected output of how the images should look](https://cdn.hashnode.com/res/hashnode/image/upload/v1676762356612/77fd164f-c405-4c59-bc35-8f0230f74c1d.png align="center")

However, when I opened the website on iOS mobile devices, I was in for a surprise. What I saw was pretty hilarious and shocking.

![Unexpected result on an iOS device](https://cdn.hashnode.com/res/hashnode/image/upload/v1676762428307/e85a578e-4db4-433c-a4fa-a12efba4adf3.jpeg align="center")

### Conclusion

Overall, my experience with Safari compatibility issues has taught me the importance of thoroughly testing websites on different browsers and devices.

Thanks for reading!