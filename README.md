[<img src="http://rabble-rouser.github.io/Healthspek-WebSpeks/header.png" width="300">](http://www.healthspek.com)
# Web Spek Developer's Guide <br/> & Quick-Start Template

Healthspek Web Speks are web pages embedded into the Healthspek iPad and Web Apps.  Web Speks open the opportunity for you, as a developer, to create a Spek to be available for all Healthspek users.  After your Spek is approved, it can be added by Healthspek users to their Healthspek Dashboards alongside all of their other Speks.

Learn more about the Healthspek Apps at [Healthspek.com](http://www.healthspek.com/).

## Getting Started

A Web Spek is simply a web page that you host and manage.  It is viewable in Healthspek Apps in a web view.  HTML, CSS and Javascript can be used as desired.  We provide a Web Spek API so that your Spek can interact with the Healthspek App for optional functionality.

Download our Web Spek template as a starting point for your first Spek: http://github.com/rabble-rouser/Healthspek-WebSpeks/archive/gh-pages.zip


## Testing Web Speks

- **Testing your Web Spek on the Healthspek Web App:**

    See your Web Spek as it will appear in the web application at http://app.healthspek.com/api/webspek/preview

    Enter your Spek’s name and URL and click “Test”.

- **Testing your Web Spek on the Healthspek iPad App:**

    For access to our iPad Web Spek test application, “InSpektor”, send your email address to [nshaw@rabbleandrouser.com](mailto:nshaw@rabbleandrouser.com?subject=Web%20Spek%20TestFlight%20Request).  You will be sent an email with instructions for installing the iPad InSpektor application.


## Submitting Your Web Spek to Healthspek

Your Web Spek must be approved by Healthspek before it is added to the Healthspek Apps.  Send an email to [nshaw@rabbleandrouser.com](mailto:nshaw@rabbleandrouser.com?subject=Web%20Spek%20Submission) with your Web Spek name and URL to have it reviewed and added to the Healthspek Apps.


## Web Spek Files

- **/ (root)** : Accessing the root of your Spek URL must return the default Spek content.  Your server might automatically load a file named *index.html* or similar.
- **header.png** : If there is a file named `header.png` located in your Spek directory then it will be used as your Spek header.  If this image is missing, a default header design with your Spek name will be displayed instead.  We recommend that `header.png` be 320 pixels wide by 40 pixels tall and have a transparent background.  This image will be displayed over light gray and white backgrounds.


## Web Spek API

Load this Javascript in your Spek HTML page to access the Web Spek API:
```html
<script type="text/javascript" src="http://app.healthspek.com/api/webspek/">
```

### API Actions:

**open** – open a full-screen web view
- HTML: `<a href="fullscreen.html" target="open">`
- Javascript: `window.open('fullscreen.html', 'open');`

**modal** – open a modal web view
- HTML: `<a href="modal.html" target="modal">`
- Javascript: `window.open('modal.html', 'modal');`

**close** – close the current full-screen or model web view
- HTML: `<a target="close">`
- Javascript: `window.close();`

_You can optionally load (or reload) a page in the parent web view:_
- HTML: `<a href="home.html" target="close">`
- Javascript: `window.close('home.html');`
