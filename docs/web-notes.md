# freeCodeCamp Web Development Bootcamp course notes

## Read me first

[Responsive Web Design course on freeCodeCamp](https://www.freecodecamp.org/learn/2022/responsive-web-design/) | [Responsive Web Design (Beta)](https://www.youtube.com/playlist?list=PLU3RKvMpgrSEswU7f9pg6EYaO1s944CDI) | [HTML on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML) | [CSS on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)

## HTML Introduction:
### Parts of an HTML Element:
[MDN - Getting Started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)

HTML elements are the building blocks of displaying information on a web page. Often referred to as 'tags', many HTML elements will have an open tag and closing tag:

Most html elements, are structured as follows:
Open the tag with `<` and then the tag identifier is inside, and the tag is closed out with `>`. Then you want to close out the tag but adding a `/` in the `>`. So:
```
<p>Here is the element content</p>
```
#### Types of HTML elements
When working with HTML elements, there is types that require open and closing tags. However, there are elements that are considered to be **self-closing**. These tags do not need to have a second closing tag, some examples include:

|HTML element | Use  |
|-------------|------|
|`<hr />`     | Horizontal Rule|
|`<br />`     | Line Break|
|`<img />`    | Image |

---
### Starting structure of a HTML page:

```HTML
<!DOCTYPE lang=en>
  <html>
  <head>
    <title></title>
  </head>
  <body>
  </body>
  </html>
```
---
### Adding a comment in HTML:
[Comments on MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#comments)

Commenting in HTML (or any language) is helpful for two reasons:
+ Make notes on what the code does both for yourself but also if you are working on a team
+ To help with troubleshooting code that is not working as intended.

#### Comment in HTML:
```html
<!-- This is an HTML Comment -->
```
