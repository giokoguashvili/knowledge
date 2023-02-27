# Chrome Extensions Architecture
![chrome-extension-architecture](https://user-images.githubusercontent.com/8178412/221682612-2036a8fa-9b10-40e5-8759-b8533e27e6f6.png)

### Posts:
- [How we captured AJAX requests from a website tab with a Chrome Extension](https://www.moesif.com/blog/technical/apirequest/How-We-Captured-AJAX-Requests-with-a-Chrome-Extension/)
- [Adding Web Interception Abilities to Your Chrome Extension](https://gilfink.medium.com/adding-web-interception-abilities-to-your-chrome-extension-fb42366df425)
- [Architecture of Chrome Extension](https://medium.com/@yoshi2586/architecture-of-chrome-extension-9188c026c069)
- [Chrome Extension: Reading the BODY of an HTTP response object](https://betterprogramming.pub/chrome-extension-intercepting-and-reading-the-body-of-http-requests-dd9ebdf2348b)
- [Chrome Extensions and iFrames](http://www.natewillard.com/blog/chrome/javascript/iframes/2015/10/20/chrome-communication/)
- [Architecture of Chrome Extension](https://medium.com/@yoshi2586/architecture-of-chrome-extension-9188c026c069)
- [Chome Extensions: Modifying the DOM from an Extension popup (Message Passing)](https://blog.amussey.com/post/86223835583/chome-extensions-modifying-the-dom-from-an)
- [How to Send Data Between Chrome Extension Scripts](https://plainenglish.io/blog/how-to-send-data-between-chrome-extension-scripts-1182ce67b659)
- [Chrome Extension Tutorial: How to Pass Messages from a Page's Context](https://www.freecodecamp.org/news/chrome-extension-message-passing-essentials/)
- [Let's build a Chrome extension that steals everything](https://mattfrisbie.substack.com/p/spy-chrome-extension)
- [Пишем расширение Chrome, которое ворует вообще всё](https://habr.com/ru/post/718644/)

### Stackoverflow
- [Chrome content scripts aren't working: DOMContentLoaded listener does not execute](https://stackoverflow.com/questions/43233115/chrome-content-scripts-arent-working-domcontentloaded-listener-does-not-execut)
- [How to get a content script to load AFTER a page's Javascript has executed?](https://stackoverflow.com/questions/13917047/how-to-get-a-content-script-to-load-after-a-pages-javascript-has-executed)
- [How to execute content script after the page is loaded completely](https://stackoverflow.com/questions/28202736/how-to-execute-content-script-after-the-page-is-loaded-completely)
- [Inject javascript from content script with a chrome extension v3](https://stackoverflow.com/questions/70474845/inject-javascript-from-content-script-with-a-chrome-extension-v3)
- [Access variables and functions defined in page context using a content script](https://stackoverflow.com/questions/9515704/access-variables-and-functions-defined-in-page-context-using-a-content-script/9517879#9517879)

### Github
- [Rufflewind/chrome_cspmod](https://github.com/Rufflewind/chrome_cspmod)
- [PhilGrayson/chrome-csp-disable](https://github.com/PhilGrayson/chrome-csp-disable)
- [ahuigo/chrome-ext](https://github.com/ahuigo/chrome-ext/blob/3629262ae6884489e4b8489606e6651eb5bde1d8/demo/document_start.js)

# Security 

- **SOP** - Same-Origin Policy <br/>
web browser permits scripts contained in a first web page to access data in a second web page, but only if both web pages have the same origin
- **CORS** - Cross-Origin Resource Sharing <br/>
is a mechanism that allows restricted resources on a web page to be requested from another domain outside the domain from which the first resource was served

- **CSRF** - Cross-Site Request Forgery <br/>
is a type of malicious exploit of a website or web application where unauthorized commands are submitted from a user that the web application trusts
    - one-click attack
    - session riding
    - XSRF/CSRF attacks
- **HSTS** - HTTP Strict Transport Security  <br/>
It allows web servers to declare that web browsers should automatically interact with it using only HTTPS connections
    - protect websites against man-in-the-middle attacks
    - protocol downgrade attacks
    - Cookie Hijacking / Session Hijacking
- **CSP** - Content Security Policy <br/>
provides a standard method for website owners to declare approved origins of content that browsers should be allowed to load on that website
    - clickjacking
    - XSS - Cross Site Scripting



- **Web crawling** <br/>
is an Internet bot that systematically browses the World Wide Web and that is typically operated by search engines for the purpose of Web indexing

- **Web scraping** <br/>
used for extracting data from websites

### Posts:
- [Clickjacking Attacks and How to Prevent Them](https://auth0.com/blog/preventing-clickjacking-attacks/)
- [Web security](https://developer.mozilla.org/en-US/docs/Web/Security)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/index.html)
- [Content security policy](https://web.dev/csp/)