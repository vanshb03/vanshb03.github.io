### Question 1. Describe the path an HTTP Request takes from a browser to your GitHub Pages site.

When you enter `vanshb03.github.io` into a browser, the system first uses DNS to translate the URL into an IP address and establishes a secure, encrypted TCP connection with GitHub’s servers. GitHub’s CDN then processes our request, retrieves the site's static files from the repository, and sends them back to our browser. Then the browser parses the HTML and downloads additional resources e.g `styles` and `images` to render the live page at `vanshb03.github.io`

### Question 2. We discussed Docker Containers in class. Explain how a Docker Container differs from the environment provided by GitHub Pages.

GitHub Pages are a static file hosting service where similar to our case we end up pushing HTML, CSS, and JavaScript to a repository and GitHub serves those files as-is over its CDN. while Docker Containers are more lightweight, isolated environment that packages an application together with its entire runtime going from dependencies, runtimes, libraries, and configurations.

### AI Attribution: 
Prompt: 
Given the font Inter not being fetched by default, what other methods do I have to use aside of when connecting to the CDN for the fonts.
```html 
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
``` 

Response: 
```html
<link rel="preconnect" href="https://fonts.googleapis.com"> <!-- Preconnect to the Google Fonts CDN to avoid FOUC -->
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin> <!-- Preconnect to the Google Fonts CDN to avoid FOUC -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```