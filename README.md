# [demo] Web Fonts

There are number of ways web fonts can be added to your website. 

1. Web-safe fonts
2. Third-party fonts such as Google or Adobe Fonts
  - your fonts are hosted on their servers
3. Self-hosted fonts.

## Web Safe Fonts:
Web safe fonts or system fonts are fonts that typically come with your system (pc, mac, linux, etc.). Not all web-safe fonts are compataible with each system, however there are plenty that work for both. Web Safe fonts have the lowest impact to your site speed, as they are not coming from a third party resource or being hosted within your website structure. 

## Third-party or Cloud-based Fonts

Thrid-party or cloud-based fonts such as Google or Adobe fonts can be fun, exciting to use, and not to mention easy to use. That being said, we still have to be mindful of how many fonts and font-styles are being loaded. The more you load, the more load you are putting your website. Third-party fonts can cause "render-blocking" issues (the browser needs to render and parse all html and css files). 

If your fonts are taking foooorreeeevvvveeeerrrrr to load you or the user could experience FOUT/FOIT (Flash of Unstyled Text). As of now, Google has a done a pretty decent job of helping with that. 

See here for more information: 
- https://css-tricks.com/how-to-load-fonts-in-a-way-that-fights-fout-and-makes-lighthouse-happy/
- https://csswizardry.com/2020/05/the-fastest-google-fonts/
- https://css-tricks.com/almanac/properties/f/font-display/

## Self-hosted Fonts

Self-hosted fonts are fonts that are embedded into your project folder. Self-hosted fonts use the ```css @font-face``` rule, allowing the custom fonts to be loaded on a webpage. Self-hosted fonts can also can render-blocking. If using self-hosted font's make sure you are using a fallback font, and a font-display. 

example:
```css
    @font-face {
      font-family: 'bloodynormal';
      src: url('../fonts/bloody-webfont.woff2') format('woff2'),
           url('../fonts/bloody-webfont.woff') format('woff');
      font-weight: normal;
      font-style: normal;
      font-display: swap;
  }

```
See here for more details: 
- https://css-tricks.com/snippets/css/using-font-face/

Remember to always check Google Lighthouse to if you can help your site become faster! 

